## `ruby:buster`

```console
$ docker pull ruby@sha256:bd2dded2da075d6461b9c0e565a835b095bd6b476a572cb32712f7a0c06ddb32
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

### `ruby:buster` - linux; amd64

```console
$ docker pull ruby@sha256:0a8c4717fd992795875f0c434d497c6a708fa0bbc0e9534c04fbf26909e37d30
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.8 MB (344779948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e9456de932a0909b227b29bb9866c17e66d0db0151c0a261aa580f37fe8984c`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 12 Jul 2022 01:20:20 GMT
ADD file:d738977543f4afc4c3040c6fca3e3f15388ec3b7263a29a6aa83f9a4bf05fed1 in / 
# Tue, 12 Jul 2022 01:20:21 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 02:49:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 02:49:29 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Jul 2022 02:49:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 02:50:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 13:39:22 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 12 Jul 2022 13:39:22 GMT
ENV LANG=C.UTF-8
# Tue, 12 Jul 2022 13:49:43 GMT
ENV RUBY_MAJOR=3.1
# Tue, 12 Jul 2022 13:49:43 GMT
ENV RUBY_VERSION=3.1.2
# Tue, 12 Jul 2022 13:49:43 GMT
ENV RUBY_DOWNLOAD_SHA256=ca10d017f8a1b6d247556622c841fc56b90c03b1803f87198da1e4fd3ec3bf2a
# Tue, 12 Jul 2022 13:51:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 12 Jul 2022 13:51:50 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 12 Jul 2022 13:51:50 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 12 Jul 2022 13:51:50 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Jul 2022 13:51:51 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 12 Jul 2022 13:51:51 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:80b89a2b88b24e7be7c8038e2cbff99ad4fd2f07ad914da4bab80dabaadf8a99`  
		Last Modified: Tue, 12 Jul 2022 01:24:55 GMT  
		Size: 50.4 MB (50440555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b0405f798f5b335d83b02371187f3be0ce2092aa0c6b6178ff11290ee6a14c9`  
		Last Modified: Tue, 12 Jul 2022 02:56:14 GMT  
		Size: 7.9 MB (7856888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab80b2b0494ab26b41941fb73a028292e2e5d2070c56b3488e890eda20e04641`  
		Last Modified: Tue, 12 Jul 2022 02:56:14 GMT  
		Size: 10.0 MB (9998095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb827974c1cb152eae96a7b67abce3afa75353dec7790c0c07fdbb8906925921`  
		Last Modified: Tue, 12 Jul 2022 02:56:31 GMT  
		Size: 51.8 MB (51843739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be554c4b061a316448883bc617e51c7659c6659d4ac8ce2bb4d4ea3d338a6f04`  
		Last Modified: Tue, 12 Jul 2022 02:57:06 GMT  
		Size: 192.5 MB (192503721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11aaf40e8c446dae0fb73603196937599dabc50cf59f05f2b82656c53494dae8`  
		Last Modified: Tue, 12 Jul 2022 14:14:04 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c586d8b76ff2ab47edd3ea1bd81cf8c3c48a86d99a29de1137d108102bec8cc`  
		Last Modified: Tue, 12 Jul 2022 14:15:32 GMT  
		Size: 32.1 MB (32136576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6587c58d6e118439e5d872ce2e037293f9f4cd05bfead92b1cc08cb2e10e25cb`  
		Last Modified: Tue, 12 Jul 2022 14:15:28 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:buster` - linux; arm variant v5

```console
$ docker pull ruby@sha256:dacd251876d1c216186494038edb39eea2a0fc7cea499d2c75db89c7126e7868
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.0 MB (317044100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2197dd317ca323633f0ed6b95287a3be7938af8637533af6334480c3dac76e4e`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 23 Jun 2022 00:51:06 GMT
ADD file:29a86a4b70e0fb7454a1325b875ec05d02fe02c2dd72a61a0b9476e7f1f3fb78 in / 
# Thu, 23 Jun 2022 00:51:07 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 01:41:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:41:37 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Jun 2022 01:42:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:45:13 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 22:08:59 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 23 Jun 2022 22:08:59 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jun 2022 22:30:29 GMT
ENV RUBY_MAJOR=3.1
# Thu, 23 Jun 2022 22:30:29 GMT
ENV RUBY_VERSION=3.1.2
# Thu, 23 Jun 2022 22:30:30 GMT
ENV RUBY_DOWNLOAD_SHA256=ca10d017f8a1b6d247556622c841fc56b90c03b1803f87198da1e4fd3ec3bf2a
# Thu, 23 Jun 2022 22:35:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 23 Jun 2022 22:35:01 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 23 Jun 2022 22:35:01 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 23 Jun 2022 22:35:02 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Jun 2022 22:35:03 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 23 Jun 2022 22:35:04 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:dad2005e84922efa5686f4921c83f828452891153e5fad381514bbdbd3b2b8fa`  
		Last Modified: Thu, 23 Jun 2022 01:06:27 GMT  
		Size: 48.2 MB (48160705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:540e32e30ed2717efe58bd73d7a7469de69e97c528d2402897d3f6d326ca6af4`  
		Last Modified: Thu, 23 Jun 2022 02:04:39 GMT  
		Size: 7.4 MB (7400800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd283a4314a89d71392745ece238ed63888f508f2dd55f513099cfe5d8748eeb`  
		Last Modified: Thu, 23 Jun 2022 02:04:39 GMT  
		Size: 9.7 MB (9687650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8287fbf741a3acfdcc7dae55783cb6450c99e052448a3e31549e333a036e58d`  
		Last Modified: Thu, 23 Jun 2022 02:05:28 GMT  
		Size: 49.6 MB (49584208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68bb322c614ad37b396dba51871f5c11d8a7861abe552cc770c617d31cc10c22`  
		Last Modified: Thu, 23 Jun 2022 02:07:24 GMT  
		Size: 171.4 MB (171424914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e5342e1cb730f7372fa4f7c08093825609928b82a486a6fd73036f945c68bb9`  
		Last Modified: Thu, 23 Jun 2022 23:23:48 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:308fb24e59714953686d51cc76ef0e222d400f5d7651b817aa0427987fce5683`  
		Last Modified: Thu, 23 Jun 2022 23:26:36 GMT  
		Size: 30.8 MB (30785448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e24752def195197b1820166571ceda322c600200d22efbef7cc28b0e901fd5e5`  
		Last Modified: Thu, 23 Jun 2022 23:26:22 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:buster` - linux; arm variant v7

```console
$ docker pull ruby@sha256:bdc52fad03760f658d7b7c63090a26de5bccba79ffdd85074ac55b972d056e23
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.1 MB (309124088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77ec50c9d733bb3d6812a2810a1de8d9d1ceb3bff22df8a25d39b9335b028e60`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 23 Jun 2022 01:00:14 GMT
ADD file:b8401862d74ac67a61f764c5dcc54fde231623bf55d2299665eab35dccd25114 in / 
# Thu, 23 Jun 2022 01:00:15 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 01:50:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:50:43 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Jun 2022 01:51:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:53:49 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Jun 2022 12:04:36 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Fri, 24 Jun 2022 12:04:36 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jun 2022 12:25:26 GMT
ENV RUBY_MAJOR=3.1
# Fri, 24 Jun 2022 12:25:26 GMT
ENV RUBY_VERSION=3.1.2
# Fri, 24 Jun 2022 12:25:27 GMT
ENV RUBY_DOWNLOAD_SHA256=ca10d017f8a1b6d247556622c841fc56b90c03b1803f87198da1e4fd3ec3bf2a
# Fri, 24 Jun 2022 12:29:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Fri, 24 Jun 2022 12:29:45 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 24 Jun 2022 12:29:45 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 24 Jun 2022 12:29:46 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 24 Jun 2022 12:29:47 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 24 Jun 2022 12:29:48 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:0555d003e6ef528480fa5625ca8ff9a45d899a62b5c20ab7547a42c64d7c1d4c`  
		Last Modified: Thu, 23 Jun 2022 01:16:07 GMT  
		Size: 45.9 MB (45915761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d67b659cf86b06bd457cf205d2cfded55fd9654e275d3ec128f15fb94099c21f`  
		Last Modified: Thu, 23 Jun 2022 02:16:11 GMT  
		Size: 7.1 MB (7145400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6da167dadbe348ebfc7cbe4152eae80fb72e14b28b417ffa2bc6adf87034179`  
		Last Modified: Thu, 23 Jun 2022 02:16:12 GMT  
		Size: 9.3 MB (9343917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:034ac9bc2920b12499948ed10c17ffdc5b34b7e5bff76a6b5735dbddcd25233f`  
		Last Modified: Thu, 23 Jun 2022 02:16:49 GMT  
		Size: 47.4 MB (47359583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:460fa2a517792e189f8bcf5c8720fcc36670999648783f68e21e0aa3dfc2a43e`  
		Last Modified: Thu, 23 Jun 2022 02:18:27 GMT  
		Size: 168.7 MB (168685649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a86bef3dbdd8ef5e788aa6c41cf71836c99adfbf1468de851fd16c38ebdaa47`  
		Last Modified: Fri, 24 Jun 2022 13:20:07 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26966333c80d147f1fd780e76f293215d543b64fece95dd791af887e6d91da97`  
		Last Modified: Fri, 24 Jun 2022 13:23:00 GMT  
		Size: 30.7 MB (30673403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:179fcf293e4798c5f431f0ac1f06bd59a9a8e4920bdfe1c0bff3e719ec687e6b`  
		Last Modified: Fri, 24 Jun 2022 13:22:46 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:buster` - linux; arm64 variant v8

```console
$ docker pull ruby@sha256:c4ccea7e67829020afac09f2d271da3e5bedc61be1316878a394efc67c3a57cc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.3 MB (334326630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:024e85ab6006c0a1c02465e53a1d469ef5458afef54371925243b7949f1e314c`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 23 Jun 2022 00:40:54 GMT
ADD file:a5e3c0ffa9f9754a6d77fafd8288e699a70f7f6ff7c5912a065f1c69f1393e99 in / 
# Thu, 23 Jun 2022 00:40:55 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 01:12:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:12:52 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Jun 2022 01:13:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:14:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 13:32:38 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 23 Jun 2022 13:32:39 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jun 2022 13:42:17 GMT
ENV RUBY_MAJOR=3.1
# Thu, 23 Jun 2022 13:42:18 GMT
ENV RUBY_VERSION=3.1.2
# Thu, 23 Jun 2022 13:42:19 GMT
ENV RUBY_DOWNLOAD_SHA256=ca10d017f8a1b6d247556622c841fc56b90c03b1803f87198da1e4fd3ec3bf2a
# Thu, 23 Jun 2022 13:44:09 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 23 Jun 2022 13:44:10 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 23 Jun 2022 13:44:11 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 23 Jun 2022 13:44:12 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Jun 2022 13:44:13 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 23 Jun 2022 13:44:14 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:8d6f1451981514e25c21542f5c7ee9bb90052b8856b484ce47294cbf1fd5a234`  
		Last Modified: Thu, 23 Jun 2022 00:47:46 GMT  
		Size: 49.2 MB (49229092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ccc9fb4baf6e7f2e6ee18ed689c8ee1171c6751c8bbd317d580a193da27a5f1`  
		Last Modified: Thu, 23 Jun 2022 01:23:09 GMT  
		Size: 7.7 MB (7719858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:620d55693ed5943ab298346d9ccafefdd6d6f33994e6820a857737df89b65f3a`  
		Last Modified: Thu, 23 Jun 2022 01:23:08 GMT  
		Size: 9.8 MB (9767307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82dcb0fa2b6020cd95c3972ec0fe03da38862f57574fe03a49360713d6f415d6`  
		Last Modified: Thu, 23 Jun 2022 01:23:28 GMT  
		Size: 52.2 MB (52174988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d75d85ab89337b32fb8b4e0454a157fa71a765a1daf512255323edd5f3f0afe7`  
		Last Modified: Thu, 23 Jun 2022 01:24:03 GMT  
		Size: 184.1 MB (184065123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:686fa7275adfc1b6a17a09b7fdc9b84f2a95657a7cc31c67f4af91cb10195405`  
		Last Modified: Thu, 23 Jun 2022 14:06:48 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0dba185cb53e562abf4c35bc9f06f2fb173adbefa9d47fe34ad9d04781282b4`  
		Last Modified: Thu, 23 Jun 2022 14:08:33 GMT  
		Size: 31.4 MB (31369921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40255f9c17c21b7421143aa6cc24fee304c8a3b8fc0e89363527078056cdae60`  
		Last Modified: Thu, 23 Jun 2022 14:08:30 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:buster` - linux; 386

```console
$ docker pull ruby@sha256:d51bd64f78acd2f98558f66069366060fe3010b534b029e57ed3221d9ab9572d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.6 MB (352561296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:808f270903106fd882418ef25bc4521e7be01a3212bac41518408cb10191efc1`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 12 Jul 2022 00:39:39 GMT
ADD file:0f1020fa1fb5b3518ec765b21180056cc802ac9258d1eed5e109edd83e0038d9 in / 
# Tue, 12 Jul 2022 00:39:40 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 04:28:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 04:28:34 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Jul 2022 04:29:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 04:30:29 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 10:25:54 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 12 Jul 2022 10:25:55 GMT
ENV LANG=C.UTF-8
# Tue, 12 Jul 2022 10:35:35 GMT
ENV RUBY_MAJOR=3.1
# Tue, 12 Jul 2022 10:35:36 GMT
ENV RUBY_VERSION=3.1.2
# Tue, 12 Jul 2022 10:35:36 GMT
ENV RUBY_DOWNLOAD_SHA256=ca10d017f8a1b6d247556622c841fc56b90c03b1803f87198da1e4fd3ec3bf2a
# Tue, 12 Jul 2022 10:37:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 12 Jul 2022 10:37:28 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 12 Jul 2022 10:37:29 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 12 Jul 2022 10:37:30 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Jul 2022 10:37:31 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 12 Jul 2022 10:37:32 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:87a13c20a9000f48185a3819712d2a14a8ddd6111bd1392856609aa18a233847`  
		Last Modified: Tue, 12 Jul 2022 00:45:40 GMT  
		Size: 51.2 MB (51204001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:798a6241824db4c4cb7e4997fe37c17a97c4d76bf1fb544730ccdbbbc9aaf8e0`  
		Last Modified: Tue, 12 Jul 2022 04:37:13 GMT  
		Size: 8.0 MB (8022957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a99684560fe738e37dc34fae618fb12d6be36f03ccc22266fe649cb7bbb61c4`  
		Last Modified: Tue, 12 Jul 2022 04:37:14 GMT  
		Size: 10.1 MB (10123633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1585b0c9e22a13d5d87725ff1930fdb45614aee7c6e4e100407baf92a6bf7511`  
		Last Modified: Tue, 12 Jul 2022 04:37:36 GMT  
		Size: 53.4 MB (53443224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:137681546c9b52e9e1c2ee24b932a6600610c3d3954315c5fbdfc983b4f04a03`  
		Last Modified: Tue, 12 Jul 2022 04:38:14 GMT  
		Size: 199.0 MB (199032786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f55e238a6b79726db77cb7301221b0ee4647f93013bb2d47e271a62801c09df`  
		Last Modified: Tue, 12 Jul 2022 11:00:55 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5335ee38987d1fc56e1f59b48b4e5a4e21268932cbb6003406fff2898fd21f9d`  
		Last Modified: Tue, 12 Jul 2022 11:02:40 GMT  
		Size: 30.7 MB (30734352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b469b318e171678799a230e105afe767d9b67feeb6148c5203c16258c7d00605`  
		Last Modified: Tue, 12 Jul 2022 11:02:35 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:buster` - linux; mips64le

```console
$ docker pull ruby@sha256:d1325a8d5d7cec1c466066d5220b55fe0397e6a4b533e6372a32b6c069bc7067
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.9 MB (328915273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6a72d3a158ea1170561ee56993c4f1a9688149ec8e66bf486b3b80b95ff8612`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 23 Jun 2022 01:10:55 GMT
ADD file:e97021cb9347cc6233316e4e1f31dc6728791c819d5c4f472c2e9009df33ed64 in / 
# Thu, 23 Jun 2022 01:10:58 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 02:00:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 02:00:57 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Jun 2022 02:02:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 02:07:54 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Jun 2022 16:08:56 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Fri, 24 Jun 2022 16:09:02 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jun 2022 17:00:27 GMT
ENV RUBY_MAJOR=3.1
# Fri, 24 Jun 2022 17:00:33 GMT
ENV RUBY_VERSION=3.1.2
# Fri, 24 Jun 2022 17:00:39 GMT
ENV RUBY_DOWNLOAD_SHA256=ca10d017f8a1b6d247556622c841fc56b90c03b1803f87198da1e4fd3ec3bf2a
# Fri, 24 Jun 2022 17:11:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Fri, 24 Jun 2022 17:11:08 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 24 Jun 2022 17:11:14 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 24 Jun 2022 17:11:20 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 24 Jun 2022 17:11:30 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 24 Jun 2022 17:11:37 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:c69f93f35e40f60566a2c787b9d7a1e4ae3c026d480bd089de24eaaa432ffab6`  
		Last Modified: Thu, 23 Jun 2022 01:21:04 GMT  
		Size: 49.1 MB (49073169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8064d03bf4d62d6d286faab208b26248a41ff122c53e3a1cc34d98fff9698faa`  
		Last Modified: Thu, 23 Jun 2022 02:23:21 GMT  
		Size: 7.3 MB (7272853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e11d44e638ac6c53724b0eefa08dde59c4fe2c7cb51801bb214ab56c4f8634a5`  
		Last Modified: Thu, 23 Jun 2022 02:23:22 GMT  
		Size: 9.8 MB (9800300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e0c8148d6586ab0843c3316210a98b1355a7b90e58c7f09e81feee93e27bcd0`  
		Last Modified: Thu, 23 Jun 2022 02:24:08 GMT  
		Size: 50.9 MB (50862080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:709fbe1cd666dac5a125c19c825efc54bfae83acc5d33cecd0326c2a23a7ff8e`  
		Last Modified: Thu, 23 Jun 2022 02:26:11 GMT  
		Size: 180.0 MB (180015118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8f62a45864ed8fa911991307387b6823d204c7a4aa865f5d1cc3fa0913f64db`  
		Last Modified: Fri, 24 Jun 2022 18:51:44 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8f9536fd6332b32d4c9ae7389d82264322429da3d1f0f354d535af09044d3a4`  
		Last Modified: Fri, 24 Jun 2022 18:54:07 GMT  
		Size: 31.9 MB (31891411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa0d3192b606bf9501fe482b8d6c5b6e421ccd188a019668e029d564d571c6e1`  
		Last Modified: Fri, 24 Jun 2022 18:53:53 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:buster` - linux; ppc64le

```console
$ docker pull ruby@sha256:43f8e18d0747a78240d0caea8765c18e2e04443c336b93403c7d142912323d93
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.4 MB (366367511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02c112de4d1b5d47a88808b8be3fc42bbf6cbe08d9e7b82b9a0c39a5c05bb7fc`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 12 Jul 2022 01:25:48 GMT
ADD file:2148d05c090aaf9547831ad92d0e8afca3df183ef38c21db2a5b8962fcc3bfa0 in / 
# Tue, 12 Jul 2022 01:25:53 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 04:36:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 04:36:58 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Jul 2022 04:38:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 04:47:36 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 11:49:54 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 12 Jul 2022 11:49:58 GMT
ENV LANG=C.UTF-8
# Tue, 12 Jul 2022 12:21:54 GMT
ENV RUBY_MAJOR=3.1
# Tue, 12 Jul 2022 12:21:56 GMT
ENV RUBY_VERSION=3.1.2
# Tue, 12 Jul 2022 12:21:58 GMT
ENV RUBY_DOWNLOAD_SHA256=ca10d017f8a1b6d247556622c841fc56b90c03b1803f87198da1e4fd3ec3bf2a
# Tue, 12 Jul 2022 12:25:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 12 Jul 2022 12:25:33 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 12 Jul 2022 12:25:42 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 12 Jul 2022 12:25:48 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Jul 2022 12:25:59 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 12 Jul 2022 12:26:01 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:985c65736f23a90bf354a992729a4278b1841d9385b35f881ba5b8293ce58b29`  
		Last Modified: Tue, 12 Jul 2022 01:36:56 GMT  
		Size: 54.2 MB (54177075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7867ac0933d69f010391d4bc1d61ba133b54f64f19167f167107f1a1d2580d35`  
		Last Modified: Tue, 12 Jul 2022 05:04:05 GMT  
		Size: 8.3 MB (8293786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd9756f1bd01e760e999cc8470fac737056aba35f6271de8e2275e608a0ad971`  
		Last Modified: Tue, 12 Jul 2022 05:04:05 GMT  
		Size: 10.7 MB (10728937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f13af069748c93f05bcfe96ab4d965d4cf693be9546b9d5247fb5bde8bed6d7c`  
		Last Modified: Tue, 12 Jul 2022 05:04:29 GMT  
		Size: 57.5 MB (57458013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5aaaa1e4228f48336c68735476cf2490488735d87d9ba2fca89022dfe10048a`  
		Last Modified: Tue, 12 Jul 2022 05:05:13 GMT  
		Size: 203.4 MB (203400169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b0958fb740b1f4ffb4ed3f8afcd00f8cb8bfe3420e21b234520987e11a32b5a`  
		Last Modified: Tue, 12 Jul 2022 13:48:07 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51037f063b915300cbc9373a1c3ce246dc102133d56f539f18438fbb8926bbe0`  
		Last Modified: Tue, 12 Jul 2022 13:50:02 GMT  
		Size: 32.3 MB (32309156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c313e4eea06a40513fdb935ac26bfd5797776be54976a8777d7a5292768b2825`  
		Last Modified: Tue, 12 Jul 2022 13:49:58 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:buster` - linux; s390x

```console
$ docker pull ruby@sha256:fab4a8124b5865baca2be5b725feeef4e3b0d513582bd676ce1a2a658cf29643
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.7 MB (326735712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be36e0af3dec35686a6c2570e14830dd4a68ac4559dfe16cb62fbd743afd0b71`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 23 Jun 2022 00:43:34 GMT
ADD file:2fe0c2724221ad2af3b740e4e2da8c4e883777f2e4466804951aaacc7472f0b5 in / 
# Thu, 23 Jun 2022 00:43:41 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 01:20:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:20:35 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Jun 2022 01:21:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:24:13 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 13:06:30 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 23 Jun 2022 13:06:30 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jun 2022 13:15:03 GMT
ENV RUBY_MAJOR=3.1
# Thu, 23 Jun 2022 13:15:03 GMT
ENV RUBY_VERSION=3.1.2
# Thu, 23 Jun 2022 13:15:03 GMT
ENV RUBY_DOWNLOAD_SHA256=ca10d017f8a1b6d247556622c841fc56b90c03b1803f87198da1e4fd3ec3bf2a
# Thu, 23 Jun 2022 13:16:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 23 Jun 2022 13:16:42 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 23 Jun 2022 13:16:42 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 23 Jun 2022 13:16:42 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Jun 2022 13:16:42 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 23 Jun 2022 13:16:43 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:977fe4047366375c4e256a32fd8e196b4ce6a283da397aa1ef2dafa150c30190`  
		Last Modified: Thu, 23 Jun 2022 00:52:15 GMT  
		Size: 49.0 MB (49007215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3205fcf3ff7eff52355fbdc242f38950a2bb1e025c8c3f0d6c952e2a36295f60`  
		Last Modified: Thu, 23 Jun 2022 01:35:59 GMT  
		Size: 7.4 MB (7423836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6d1428cca6d47f3c2edded7af8b465dc3457d6b8231f1f691b2e5b7517fcf31`  
		Last Modified: Thu, 23 Jun 2022 01:36:00 GMT  
		Size: 9.9 MB (9883348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:692a5bd2de9979006c276a4aeb1301534893d7d38e77ed09cc3084b5b0569e60`  
		Last Modified: Thu, 23 Jun 2022 01:36:15 GMT  
		Size: 51.4 MB (51384085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e36e764f0a052c49f9bb5a9c5850ea48f067614ab25e05778a29c545f2a0deef`  
		Last Modified: Thu, 23 Jun 2022 01:36:44 GMT  
		Size: 177.0 MB (176967120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b2bdbf5a8bf1bdc4ce1fb5d95450b5775446d3059f5d0e6ae2c1c455742ca04`  
		Last Modified: Thu, 23 Jun 2022 13:36:40 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43c2f52b324330bc6ac09a10ce32f044728dcfda29423aaacc099598e6e3783b`  
		Last Modified: Thu, 23 Jun 2022 13:37:48 GMT  
		Size: 32.1 MB (32069734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:668ed56a7e765d4c68d11b49e5f25ca33647f517bc7da3e1ce0aa4eba0dadf90`  
		Last Modified: Thu, 23 Jun 2022 13:37:46 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
