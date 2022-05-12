## `ruby:2-bullseye`

```console
$ docker pull ruby@sha256:d257e1005e8d21b5402f36c03138f854fbc2c7f0e1bbae1dc13feba88e396b3b
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

### `ruby:2-bullseye` - linux; amd64

```console
$ docker pull ruby@sha256:5d7f2eca55d40cb0451908140adbcfa1a6ec21e1e9af02026eebd08b26475147
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.7 MB (336670862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9ff7b1916e8621692c63166fe723ba1de03eba2aaff34e7b8180ee61a17d77b`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 11 May 2022 01:20:05 GMT
ADD file:68a5d7d0db592625159865110c1b7dcb15cf70ecf71b5fd541ef89584cd734ba in / 
# Wed, 11 May 2022 01:20:05 GMT
CMD ["bash"]
# Wed, 11 May 2022 01:49:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 01:49:10 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 11 May 2022 01:49:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 01:50:11 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 15:26:20 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 11 May 2022 15:26:20 GMT
ENV LANG=C.UTF-8
# Wed, 11 May 2022 15:54:22 GMT
ENV RUBY_MAJOR=2.7
# Wed, 11 May 2022 15:54:22 GMT
ENV RUBY_VERSION=2.7.6
# Wed, 11 May 2022 15:54:22 GMT
ENV RUBY_DOWNLOAD_SHA256=54dcd3044726c4ab75a9d4604720501442b229a3aed6a55fe909567da8807f24
# Wed, 11 May 2022 15:55:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 11 May 2022 15:55:49 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 11 May 2022 15:55:50 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 11 May 2022 15:55:50 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 May 2022 15:55:50 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 11 May 2022 15:55:50 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:67e8aa6c8bbc76b1f2bccb3864b0887671833b8667dc1f6c965fcb0eac7e6402`  
		Last Modified: Wed, 11 May 2022 01:24:45 GMT  
		Size: 54.9 MB (54945622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:627e6c1e105548ea4a08354eea581f137cf368d91aeb0ad47dcb706fca54fd8b`  
		Last Modified: Wed, 11 May 2022 01:57:17 GMT  
		Size: 5.2 MB (5155721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0670968926f6461e3135c82ba2c0ad3ebdedc0d0f41b18bda4a1e41104b8be8a`  
		Last Modified: Wed, 11 May 2022 01:57:18 GMT  
		Size: 10.9 MB (10875052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a8b0e20be4b4a332bc3d90b9903a5f3c0664b440fd9f1d2a1db0d4b7e6e826b`  
		Last Modified: Wed, 11 May 2022 01:57:38 GMT  
		Size: 54.6 MB (54578468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0b10a3a2784b06bfe0af1493ea2a0fa957ae5e0dc30fcfd1166d2558ba74e4d`  
		Last Modified: Wed, 11 May 2022 01:58:14 GMT  
		Size: 196.6 MB (196562669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2562c4ce4af44dec187feb596089b308c931bfed23a8698e26375f26d6969422`  
		Last Modified: Wed, 11 May 2022 16:02:55 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48a1553872940b26439aeafd8e90b25df24c1564b14724865fbd50dc857ce78c`  
		Last Modified: Wed, 11 May 2022 16:06:43 GMT  
		Size: 14.6 MB (14552956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a3e3ca7098bb410b3beb70a5affdc9d2dea2fdb0f297e63f43558ffc9563075`  
		Last Modified: Wed, 11 May 2022 16:06:41 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:2-bullseye` - linux; arm variant v5

```console
$ docker pull ruby@sha256:38f4903def034d732c74914262c11c4025311906eec5d37fdb2f7a2df3312103
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.1 MB (309109016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17643da9c3565c580abab83d5be79a811f9bf86652be036eca2475ea4b9cd925`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 11 May 2022 00:49:59 GMT
ADD file:b4fea5a360c5cca5abc5866da48126a30eeaf4e976d09c479958fe445dae8021 in / 
# Wed, 11 May 2022 00:49:59 GMT
CMD ["bash"]
# Wed, 11 May 2022 02:06:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 02:06:54 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 11 May 2022 02:07:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 02:10:09 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 12 May 2022 00:01:51 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 12 May 2022 00:01:52 GMT
ENV LANG=C.UTF-8
# Thu, 12 May 2022 01:04:03 GMT
ENV RUBY_MAJOR=2.7
# Thu, 12 May 2022 01:04:03 GMT
ENV RUBY_VERSION=2.7.6
# Thu, 12 May 2022 01:04:03 GMT
ENV RUBY_DOWNLOAD_SHA256=54dcd3044726c4ab75a9d4604720501442b229a3aed6a55fe909567da8807f24
# Thu, 12 May 2022 01:07:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 12 May 2022 01:07:39 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 12 May 2022 01:07:40 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 12 May 2022 01:07:40 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 12 May 2022 01:07:42 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 12 May 2022 01:07:42 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:0ca4fabca59ca0d617061b776745ff41fdc3968ce90dd2b9198717e0bae91d98`  
		Last Modified: Wed, 11 May 2022 01:05:03 GMT  
		Size: 52.5 MB (52476689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e8d2e3c89e648f74d8cba2be942f53fbcdf53c845d8180c2c93199322a0573f`  
		Last Modified: Wed, 11 May 2022 02:30:00 GMT  
		Size: 5.1 MB (5065455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01aff9f1fe546a28b9bdb7a85b87eaaa7c9c039d0e60a7372cdcc31f58842e25`  
		Last Modified: Wed, 11 May 2022 02:30:02 GMT  
		Size: 10.6 MB (10573055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10bfe50f7f2db6acb117a778b84c53664ce16ba884ae8de0447fbea2a07acea5`  
		Last Modified: Wed, 11 May 2022 02:30:56 GMT  
		Size: 52.3 MB (52315350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05269c666a9b2a1d1fdb5711a7b6010c64b428265414acf3c08eb268ae396ac5`  
		Last Modified: Wed, 11 May 2022 02:32:56 GMT  
		Size: 174.8 MB (174771880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6137fe7bd38f7826d1108adc82a0c596fe23ff451315138aa9ec42d5c475e301`  
		Last Modified: Thu, 12 May 2022 01:26:21 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bec1ad0df4d173c8f54decda861b867c4056e2fb6a4a48319ffbd203a36b044d`  
		Last Modified: Thu, 12 May 2022 01:33:09 GMT  
		Size: 13.9 MB (13906213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b912581ba6f249d5ee6065bee779e1e30c117e6d52ef3136d8fe4cda92f3feb`  
		Last Modified: Thu, 12 May 2022 01:33:01 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:2-bullseye` - linux; arm variant v7

```console
$ docker pull ruby@sha256:717e8fe91c5836bc316ccbafe17a2e5f7badc73c72067349fa3d659024d78314
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.4 MB (296444163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:485b48c900b260dc7b46107b67e6e2d69ced569e05c7b7b606c9dc7ef4a6f9f5`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 11 May 2022 01:48:30 GMT
ADD file:d6545064ea0f75166d59e4d4a2df1e41a3477ae468e558e31f29857336978c0e in / 
# Wed, 11 May 2022 01:48:31 GMT
CMD ["bash"]
# Wed, 11 May 2022 03:21:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 03:21:59 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 11 May 2022 03:22:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 03:24:51 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 12 May 2022 08:06:41 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 12 May 2022 08:06:41 GMT
ENV LANG=C.UTF-8
# Thu, 12 May 2022 09:07:08 GMT
ENV RUBY_MAJOR=2.7
# Thu, 12 May 2022 09:07:09 GMT
ENV RUBY_VERSION=2.7.6
# Thu, 12 May 2022 09:07:09 GMT
ENV RUBY_DOWNLOAD_SHA256=54dcd3044726c4ab75a9d4604720501442b229a3aed6a55fe909567da8807f24
# Thu, 12 May 2022 09:10:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 12 May 2022 09:10:34 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 12 May 2022 09:10:34 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 12 May 2022 09:10:34 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 12 May 2022 09:10:36 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 12 May 2022 09:10:36 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:ba38f9a6c66968e207a7ada348a2110e3be0ff117e621d9e10ddd7c4becc0d2a`  
		Last Modified: Wed, 11 May 2022 02:03:49 GMT  
		Size: 50.1 MB (50134069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f71423015d7b4f718e54ff1561cc06bb4c8357baedc23b49d25fe99cd4b0ae41`  
		Last Modified: Wed, 11 May 2022 03:46:39 GMT  
		Size: 4.9 MB (4924901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd8f92194faa0a66e5bd160b229941428f0b0387c6e313e4f1f903c678fbb17e`  
		Last Modified: Wed, 11 May 2022 03:46:41 GMT  
		Size: 10.2 MB (10217886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c410c75a05c2df4ed485cda22fd35206e0ea4b9fbc9f096b11ed5adc6f83fa1c`  
		Last Modified: Wed, 11 May 2022 03:47:32 GMT  
		Size: 50.3 MB (50329744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:767978ffc99a492ddd06d37b888a093595a05ac353ceefb2cc01a1322f34164a`  
		Last Modified: Wed, 11 May 2022 03:49:16 GMT  
		Size: 167.0 MB (167042139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cd18f5b4dced1d0eec829f060f10b6a009385df64df99223ff0774c0b8aa010`  
		Last Modified: Thu, 12 May 2022 09:30:55 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:619efb8d4a559c22a11611e5321263363338d6702862cdddc9965f719ce8b7a3`  
		Last Modified: Thu, 12 May 2022 09:38:07 GMT  
		Size: 13.8 MB (13795050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b398e6cf97d34da21dfb094a95af1fee2219a6892f55181e5285605d8246f58`  
		Last Modified: Thu, 12 May 2022 09:38:00 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:2-bullseye` - linux; arm64 variant v8

```console
$ docker pull ruby@sha256:86b9909f2f56eeac19a78e64224874d0eb10cf73cf451bddf7413323ba6838bd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.5 MB (327520996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cc9ae6643255d86e66da6e6a822310d966a19fabef010e1dc7faa8b3eaa497a`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 11 May 2022 00:46:44 GMT
ADD file:239aa42118877a929b2fbfc0d5793fee7815289280affa5286de2459385c0679 in / 
# Wed, 11 May 2022 00:46:44 GMT
CMD ["bash"]
# Wed, 11 May 2022 01:25:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 01:25:29 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 11 May 2022 01:25:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 01:26:38 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 14:49:27 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 11 May 2022 14:49:28 GMT
ENV LANG=C.UTF-8
# Wed, 11 May 2022 15:17:38 GMT
ENV RUBY_MAJOR=2.7
# Wed, 11 May 2022 15:17:39 GMT
ENV RUBY_VERSION=2.7.6
# Wed, 11 May 2022 15:17:40 GMT
ENV RUBY_DOWNLOAD_SHA256=54dcd3044726c4ab75a9d4604720501442b229a3aed6a55fe909567da8807f24
# Wed, 11 May 2022 15:19:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 11 May 2022 15:19:05 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 11 May 2022 15:19:06 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 11 May 2022 15:19:07 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 May 2022 15:19:09 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 11 May 2022 15:19:10 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:3a36574378e6cece2dd3a839e1c0220eaccc4063b61d7481d1a19d3990c1f2c2`  
		Last Modified: Wed, 11 May 2022 00:53:15 GMT  
		Size: 53.6 MB (53634337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a61d3345afba43846f3e638752cce2f0d1d47b21cc667ba08b00db10767a4702`  
		Last Modified: Wed, 11 May 2022 01:35:45 GMT  
		Size: 4.9 MB (4938615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e267d6aa58f93a513352a3b46c7addbf9335d7d43bfa4f1df4026d21785181c`  
		Last Modified: Wed, 11 May 2022 01:35:46 GMT  
		Size: 10.7 MB (10656992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f647907d26b879e0d43f6f4f0807f01e4dbdc034edcecbc988f6033cf401becf`  
		Last Modified: Wed, 11 May 2022 01:36:07 GMT  
		Size: 54.7 MB (54672822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f0b3e17bdee16cf8bf269a4474bf56713879991bf87ff3bd790aa96a6f00e3c`  
		Last Modified: Wed, 11 May 2022 01:36:46 GMT  
		Size: 189.5 MB (189482172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4af8c3b3dac0cc298a1ce03ed390cf56440757f2b626dd7977591b508b5bcefb`  
		Last Modified: Wed, 11 May 2022 15:28:11 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9534690870e2c03772b74c11ace55981c9332edf2a4ba8d7aa3e36c19990e3a9`  
		Last Modified: Wed, 11 May 2022 15:32:41 GMT  
		Size: 14.1 MB (14135717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa9b48faa4170da9c8516b39e465ae00804111d49e926f34aa511c3d73984399`  
		Last Modified: Wed, 11 May 2022 15:32:39 GMT  
		Size: 141.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:2-bullseye` - linux; 386

```console
$ docker pull ruby@sha256:da41dd03734f79fade0dc14cf075e8dfd6435c06a458c13ddefadf88e76ada69
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.1 MB (341077813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87b365063c649fe1e8f2f1446963ae51badd9d540fbb3e7e2e9f57c5bff6ea3d`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 11 May 2022 01:38:57 GMT
ADD file:dae3dc662d1327f461e95b84f6f9282f3c4fb51f16ac8f20a5f141951d8436a9 in / 
# Wed, 11 May 2022 01:38:58 GMT
CMD ["bash"]
# Wed, 11 May 2022 02:10:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 02:10:56 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 11 May 2022 02:11:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 02:12:18 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 14:58:53 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 11 May 2022 14:58:54 GMT
ENV LANG=C.UTF-8
# Wed, 11 May 2022 15:27:35 GMT
ENV RUBY_MAJOR=2.7
# Wed, 11 May 2022 15:27:36 GMT
ENV RUBY_VERSION=2.7.6
# Wed, 11 May 2022 15:27:37 GMT
ENV RUBY_DOWNLOAD_SHA256=54dcd3044726c4ab75a9d4604720501442b229a3aed6a55fe909567da8807f24
# Wed, 11 May 2022 15:29:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 11 May 2022 15:29:03 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 11 May 2022 15:29:04 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 11 May 2022 15:29:05 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 May 2022 15:29:06 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 11 May 2022 15:29:07 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:5ad4f92623738998bc77103ff64344255f842f6e5fe4a846df656351b3c4852f`  
		Last Modified: Wed, 11 May 2022 01:45:53 GMT  
		Size: 55.9 MB (55942833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:026e99ab0e4b1d3aec936d04cdf9c04ddc8074f2917b86c02e66d88fcae1e42f`  
		Last Modified: Wed, 11 May 2022 02:21:42 GMT  
		Size: 5.1 MB (5080245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66dba083f619f2a2c8cfef4a4e844cf6819c306e225029e62cf7c31c17b0d344`  
		Last Modified: Wed, 11 May 2022 02:21:43 GMT  
		Size: 11.0 MB (11033702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a5333a48696af9b52c4219f20b87c5cf9b05764b7c58cd19880e6c5730d1b75`  
		Last Modified: Wed, 11 May 2022 02:22:10 GMT  
		Size: 55.9 MB (55914622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:899f353e6896a6f03a5af06a01cea44badeac7062481c294a9d7c1da1859b823`  
		Last Modified: Wed, 11 May 2022 02:22:52 GMT  
		Size: 199.5 MB (199502725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b817f7a940469767dc8e9d6d7ee68d2c9cbba693886360f5b49bf5dc9ffda35f`  
		Last Modified: Wed, 11 May 2022 15:38:11 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14cae3fcbfa78e5492525ccbfa47413c56b8e698ef3a0c8eb22197f4a9aec4cf`  
		Last Modified: Wed, 11 May 2022 15:42:57 GMT  
		Size: 13.6 MB (13603344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b94da5a617528ff9dafbb2788a9c33094a1c2560310d0bb684d47ab76625da80`  
		Last Modified: Wed, 11 May 2022 15:42:55 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:2-bullseye` - linux; mips64le

```console
$ docker pull ruby@sha256:8d0d82af77ef2e6e3b0bacdef0838e1ae1df1068bff0d49c927e42743e7f84ad
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.2 MB (315222342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db5218d7e2b02b49345bb553811ce0179c8df37c843b79f4b6481838c704b695`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 20 Apr 2022 14:27:54 GMT
ADD file:8150012d71535a0807e6b7f0bb9f31dcef864730e1df2362a20fb269ccc902a2 in / 
# Wed, 20 Apr 2022 14:27:59 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 23:15:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 23:16:07 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 20 Apr 2022 23:17:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 23:22:14 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 21 Apr 2022 14:03:45 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 21 Apr 2022 14:03:51 GMT
ENV LANG=C.UTF-8
# Thu, 21 Apr 2022 16:30:54 GMT
ENV RUBY_MAJOR=2.7
# Thu, 21 Apr 2022 16:30:59 GMT
ENV RUBY_VERSION=2.7.6
# Thu, 21 Apr 2022 16:31:05 GMT
ENV RUBY_DOWNLOAD_SHA256=54dcd3044726c4ab75a9d4604720501442b229a3aed6a55fe909567da8807f24
# Thu, 21 Apr 2022 16:38:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 21 Apr 2022 16:38:36 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 21 Apr 2022 16:38:42 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 21 Apr 2022 16:38:48 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 21 Apr 2022 16:38:58 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 21 Apr 2022 16:39:04 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:774a3fd0175393ffcac86ec5a65f3f57dfe09f9c38a55812cb69c85281394d6a`  
		Last Modified: Wed, 20 Apr 2022 14:38:35 GMT  
		Size: 53.2 MB (53203304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:844a58a93488914047d6805e3dc9f4ae899bcbf99d6a7471f9317a6d3e1ec7e9`  
		Last Modified: Wed, 20 Apr 2022 23:42:13 GMT  
		Size: 4.9 MB (4912267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c8511d2f4e2a16a1f9fbd5a7f93cc0afb4c48d25ca3cb1384417a007f74ac71`  
		Last Modified: Wed, 20 Apr 2022 23:42:15 GMT  
		Size: 10.7 MB (10659994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03e7112f2cd88458dea8f1e982b213926be31a9f9afb0ab9ef3378b9eeb55417`  
		Last Modified: Wed, 20 Apr 2022 23:43:04 GMT  
		Size: 53.3 MB (53298644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:273deafb0e12003d98ab2b2b5ffb27d54b74a8192ee6d9049ec2cde62aa306ed`  
		Last Modified: Wed, 20 Apr 2022 23:45:10 GMT  
		Size: 178.8 MB (178779647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd5ade20b45628d6a1e16e87a511996e3935d9f23b75165fd4e6b3ab54b752d9`  
		Last Modified: Thu, 21 Apr 2022 17:49:52 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e0f64c3706efe260bd8b23142c64bcb44fe7a79c29912feb7d97df5035d098c`  
		Last Modified: Thu, 21 Apr 2022 17:55:48 GMT  
		Size: 14.4 MB (14368142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:364f287479a814e048e2a997588b14453df202e7d809629cb068f6277d5cdbbe`  
		Last Modified: Thu, 21 Apr 2022 17:55:39 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:2-bullseye` - linux; ppc64le

```console
$ docker pull ruby@sha256:f59bc686a73bd43391c0628e2e15fdcf62684c217812f8cc4f706b38963a18cb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.7 MB (345667873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a66407068bbd8aa62e148a878b4309c93f1b4e469230150031a2c62014c13d0`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 11 May 2022 01:31:46 GMT
ADD file:6d7393a3491f45287b6b9a4c97432db92f762fc320e7b4527fa0969250c7cda6 in / 
# Wed, 11 May 2022 01:31:53 GMT
CMD ["bash"]
# Wed, 11 May 2022 02:30:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 02:33:58 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 11 May 2022 02:37:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 02:52:39 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 12 May 2022 04:47:51 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 12 May 2022 04:47:53 GMT
ENV LANG=C.UTF-8
# Thu, 12 May 2022 06:17:32 GMT
ENV RUBY_MAJOR=2.7
# Thu, 12 May 2022 06:17:35 GMT
ENV RUBY_VERSION=2.7.6
# Thu, 12 May 2022 06:17:39 GMT
ENV RUBY_DOWNLOAD_SHA256=54dcd3044726c4ab75a9d4604720501442b229a3aed6a55fe909567da8807f24
# Thu, 12 May 2022 06:20:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 12 May 2022 06:20:36 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 12 May 2022 06:20:40 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 12 May 2022 06:20:45 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 12 May 2022 06:20:54 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 12 May 2022 06:20:57 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:8ad85695cd2aa86dcc7fc175edbdd1c94dbfa061000f3770d4e6f795df7d74c9`  
		Last Modified: Wed, 11 May 2022 01:42:22 GMT  
		Size: 58.8 MB (58836524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aab8b0050e0adc77a432c7431bddb52ffd7a7f6133ffec0b7f2766c951614fc6`  
		Last Modified: Wed, 11 May 2022 03:48:01 GMT  
		Size: 5.4 MB (5405221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8d47d2b8f433338bdfaa5388d0c010792ba3e0bc820e40cd2d316a1b0b6aab1`  
		Last Modified: Wed, 11 May 2022 03:48:01 GMT  
		Size: 11.6 MB (11627779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:093f433f2609e3f4f5695cf59234918a3e0d13ac7eedbe9323cdcd2acfb1ce52`  
		Last Modified: Wed, 11 May 2022 03:48:30 GMT  
		Size: 58.9 MB (58855572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8bc4e97f9eb6c89e59961459cedf106242c7fb053a8a926e6d078080df1eae8`  
		Last Modified: Wed, 11 May 2022 03:49:21 GMT  
		Size: 196.0 MB (195952606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00c4033d75ef7b37815a6e5f083be13afb62507d7adddefca0c2bdf4e027b01b`  
		Last Modified: Thu, 12 May 2022 06:43:07 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1505776e2b3d6990a9faa25182d8e891aff40c7203905cd5aa2ec917187eab7`  
		Last Modified: Thu, 12 May 2022 06:48:32 GMT  
		Size: 15.0 MB (14989795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35920ad64cabd1b2d81ec29d34a015736932762c662065d2ce273c8a5caefa6d`  
		Last Modified: Thu, 12 May 2022 06:48:30 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:2-bullseye` - linux; s390x

```console
$ docker pull ruby@sha256:b1fb326529a0da730e1a6fc57be88fe14629d288e6e4894b742f830a20daae4a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.4 MB (310366279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88e6465f277f006581fb7dcc946db346d93f44fa1f934b30d092b5b1b780a098`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 11 May 2022 00:43:58 GMT
ADD file:8b9cfb1e16e1c11cdc1f936ccd3dfdd2104ab85b0b9078b1fe3bca89f53e0682 in / 
# Wed, 11 May 2022 00:44:00 GMT
CMD ["bash"]
# Wed, 11 May 2022 01:15:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 01:15:23 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 11 May 2022 01:15:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 01:16:34 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 11:08:02 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 11 May 2022 11:08:02 GMT
ENV LANG=C.UTF-8
# Wed, 11 May 2022 11:34:25 GMT
ENV RUBY_MAJOR=2.7
# Wed, 11 May 2022 11:34:25 GMT
ENV RUBY_VERSION=2.7.6
# Wed, 11 May 2022 11:34:26 GMT
ENV RUBY_DOWNLOAD_SHA256=54dcd3044726c4ab75a9d4604720501442b229a3aed6a55fe909567da8807f24
# Wed, 11 May 2022 11:35:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 11 May 2022 11:35:36 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 11 May 2022 11:35:36 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 11 May 2022 11:35:37 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 May 2022 11:35:37 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 11 May 2022 11:35:37 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:f8313f715dc1cdd9f8a3da73eafca06dcb30dff4c078bee35a162247cae99c4d`  
		Last Modified: Wed, 11 May 2022 00:49:41 GMT  
		Size: 53.2 MB (53208696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c99502d0a4c52d58c73f967ad2c52204db08f01c6512da3a6dfd8d8ea18b3ae6`  
		Last Modified: Wed, 11 May 2022 01:24:43 GMT  
		Size: 5.1 MB (5140503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33ef0d35554dad3cfdd15fa175311fb6c20c545c9b04632039378e90a1666435`  
		Last Modified: Wed, 11 May 2022 01:24:43 GMT  
		Size: 10.8 MB (10765296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c36704bf1413eb96906c58893a7d4c74f7d88490eed870be03fe531302614745`  
		Last Modified: Wed, 11 May 2022 01:25:00 GMT  
		Size: 54.0 MB (54045195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9b12d26f79096a8ccb3b94ad468c2ae17af08aa0226a5de33c5292b25ae24d4`  
		Last Modified: Wed, 11 May 2022 01:25:31 GMT  
		Size: 172.6 MB (172581996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40ab0f34dd5bc21c503c0310b8776f5ac3a12779d415c107a5e14ff16be012f8`  
		Last Modified: Wed, 11 May 2022 11:43:21 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14a05cdf90d718409187ac90c59266eafd35a7ddac324ba52dd55be2f3f13ea0`  
		Last Modified: Wed, 11 May 2022 11:46:26 GMT  
		Size: 14.6 MB (14624220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37bb52ab96b6db4dab32b3ffc6fff613dc7c2c453f3e20eb571ef6070ad43cee`  
		Last Modified: Wed, 11 May 2022 11:46:24 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
