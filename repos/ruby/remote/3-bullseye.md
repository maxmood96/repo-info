## `ruby:3-bullseye`

```console
$ docker pull ruby@sha256:5d4f7a70606b7da79a526369a4bd94d2518be1996faada98d0a220b5cbc7654f
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

### `ruby:3-bullseye` - linux; amd64

```console
$ docker pull ruby@sha256:60842e9e66d31a5117ef09ba4d1e7140e92e44fa3a00aa3fa5e6d345c4995694
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **354.9 MB (354927971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8869ff70dfeaf7f7c804bca09fdf1d29af594bc692adcb8989c836b1138f7be`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:18 GMT
ADD file:ff01c6dedb67cf22e9b0735e099b9b6367770c4880941862cc7ec0e979b4118b in / 
# Tue, 13 Sep 2022 00:56:19 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 03:43:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 03:43:18 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 13 Sep 2022 03:43:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 03:44:22 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 15:40:09 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 13 Sep 2022 15:40:10 GMT
ENV LANG=C.UTF-8
# Tue, 13 Sep 2022 15:44:34 GMT
ENV RUBY_MAJOR=3.1
# Tue, 13 Sep 2022 15:44:34 GMT
ENV RUBY_VERSION=3.1.2
# Tue, 13 Sep 2022 15:44:34 GMT
ENV RUBY_DOWNLOAD_SHA256=ca10d017f8a1b6d247556622c841fc56b90c03b1803f87198da1e4fd3ec3bf2a
# Tue, 13 Sep 2022 15:46:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 13 Sep 2022 15:46:33 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 13 Sep 2022 15:46:33 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 13 Sep 2022 15:46:33 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Sep 2022 15:46:34 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 13 Sep 2022 15:46:34 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:23858da423a6737f0467fab0014e5b53009ea7405d575636af0c3f100bbb2f10`  
		Last Modified: Tue, 13 Sep 2022 01:00:00 GMT  
		Size: 55.0 MB (55029732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:326f452ade5c33097eba4ba88a24bd77a93a3d994d4dc39b936482655e664857`  
		Last Modified: Tue, 13 Sep 2022 03:50:03 GMT  
		Size: 5.2 MB (5163200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a42821cd14fb31c4aa253203e7f8e34fc3b15d69ce370f1223fbbe4252a64202`  
		Last Modified: Tue, 13 Sep 2022 03:50:03 GMT  
		Size: 10.9 MB (10876384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8471b75885efc7790a16be5328e3b368567b76a60fc3feabd6869c15e175ee05`  
		Last Modified: Tue, 13 Sep 2022 03:50:26 GMT  
		Size: 54.6 MB (54584419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ffa7aaef4041744c03222b6b241a78a3b4ab9e8a8b99fb633a1f14b42f8bc56`  
		Last Modified: Tue, 13 Sep 2022 03:51:05 GMT  
		Size: 196.8 MB (196849089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ae7fdfb4968cec843e1e63b82662d078b469bc8bb3c7c7aa125ff7761235672`  
		Last Modified: Tue, 13 Sep 2022 15:58:12 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7df25a05a53f39e1013eebd405b1d01fd16b57f26bbfae6a41d19536c608c10a`  
		Last Modified: Tue, 13 Sep 2022 15:58:51 GMT  
		Size: 32.4 MB (32424771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cde0ff1c638a75efa5eaed9398cf9572535c0507c1761fcc4e92f0d7b72bbe2`  
		Last Modified: Tue, 13 Sep 2022 15:58:48 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:3-bullseye` - linux; arm variant v5

```console
$ docker pull ruby@sha256:0c1e0f1800d70c34bb0dcbaf5f0041c3674a4d3bb37bd40f05be726de575aeb7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.5 MB (326511380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40bcc91566cf561ebd72e6204509f48e0b8d01a8f1c538b90c2d1e4145ec2c34`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 13 Sep 2022 00:53:03 GMT
ADD file:ad560226d0aa0be51fbe1d98a8877aeb30110956b3a7c0f849a4331e99477ee4 in / 
# Tue, 13 Sep 2022 00:53:04 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 01:24:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 01:24:23 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 13 Sep 2022 01:25:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 01:26:34 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 16:09:31 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 13 Sep 2022 16:09:31 GMT
ENV LANG=C.UTF-8
# Tue, 13 Sep 2022 16:24:20 GMT
ENV RUBY_MAJOR=3.1
# Tue, 13 Sep 2022 16:24:20 GMT
ENV RUBY_VERSION=3.1.2
# Tue, 13 Sep 2022 16:24:20 GMT
ENV RUBY_DOWNLOAD_SHA256=ca10d017f8a1b6d247556622c841fc56b90c03b1803f87198da1e4fd3ec3bf2a
# Tue, 13 Sep 2022 16:31:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 13 Sep 2022 16:31:04 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 13 Sep 2022 16:31:05 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 13 Sep 2022 16:31:05 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Sep 2022 16:31:05 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 13 Sep 2022 16:31:06 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:f33103174415e8d15c8ebada62aae8327ecba6afa6035819128965eb1a64966e`  
		Last Modified: Tue, 13 Sep 2022 01:00:25 GMT  
		Size: 52.5 MB (52532200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b74e3dd9c2e4e29e0f4df5b3d5a6bb6b72260bbd689082c1a14fa9f93bb7356c`  
		Last Modified: Tue, 13 Sep 2022 01:31:25 GMT  
		Size: 5.1 MB (5070938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2ac23bd65f92366f98c6b75e0e91d6a10949d9f11f5c82875829dcc719266d2`  
		Last Modified: Tue, 13 Sep 2022 01:31:25 GMT  
		Size: 10.6 MB (10573721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b88b67ca98f8f48ca0cdb936b58bba7b8133804ce01e0e8b3f6b7c9894f01ed5`  
		Last Modified: Tue, 13 Sep 2022 01:31:54 GMT  
		Size: 52.3 MB (52321510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:453689f1385dde9166ee34ee9749cb1a1efa6f0c560b192dac4a0d47524eff54`  
		Last Modified: Tue, 13 Sep 2022 01:32:50 GMT  
		Size: 175.0 MB (175023501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9b4c6072955b2b0eb73cbc544ea11dff89b0e2b9a8a0e924f68a1ada5e5add2`  
		Last Modified: Tue, 13 Sep 2022 17:04:05 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10b29c2fa923d216786f52f68dd041b5675c6a728fc02b8240da45fbf26bc88e`  
		Last Modified: Tue, 13 Sep 2022 17:05:05 GMT  
		Size: 31.0 MB (30989133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a58574e9fa345d1207d93cc5bdf3c139d1ac3883ced07a2b5b1b2578f581e7b5`  
		Last Modified: Tue, 13 Sep 2022 17:04:59 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:3-bullseye` - linux; arm variant v7

```console
$ docker pull ruby@sha256:562f01957017abbf0e3584d5821742a9b39dc26d8dcae611aeb6da78ef2ffafe
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.9 MB (313859008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8bfcfa603132bdff1b44b85e68a1875105111c11ed108d6b415e3a38f4bef18`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 13 Sep 2022 03:42:17 GMT
ADD file:c60a3ffee6188f27e9b642109e01c6145bdbb8d4fc17475a2711795799597766 in / 
# Tue, 13 Sep 2022 03:42:18 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 07:31:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 07:32:00 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 13 Sep 2022 07:32:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 07:33:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Sep 2022 08:06:20 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 14 Sep 2022 08:06:20 GMT
ENV LANG=C.UTF-8
# Wed, 14 Sep 2022 08:22:09 GMT
ENV RUBY_MAJOR=3.1
# Wed, 14 Sep 2022 08:22:09 GMT
ENV RUBY_VERSION=3.1.2
# Wed, 14 Sep 2022 08:22:09 GMT
ENV RUBY_DOWNLOAD_SHA256=ca10d017f8a1b6d247556622c841fc56b90c03b1803f87198da1e4fd3ec3bf2a
# Wed, 14 Sep 2022 08:25:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 14 Sep 2022 08:25:31 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 14 Sep 2022 08:25:31 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 14 Sep 2022 08:25:31 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Sep 2022 08:25:31 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 14 Sep 2022 08:25:32 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:c0b863d4b31f0197ba7a7b6995cafb984dfbe6a0dcdedf88f2ce4a2f2c70b2cd`  
		Last Modified: Tue, 13 Sep 2022 03:49:09 GMT  
		Size: 50.2 MB (50195605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8418b877b4075c62cc53eb0d02b6b19d0d930a8e54ef2875bff8e9a948025c2a`  
		Last Modified: Tue, 13 Sep 2022 07:43:57 GMT  
		Size: 4.9 MB (4931269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae4d43cbe35130a47e93c66cb18df3b645f264e50e2d44ba95531a11148d4029`  
		Last Modified: Tue, 13 Sep 2022 07:43:57 GMT  
		Size: 10.2 MB (10217819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac653e751f5deb6b91cd5e0f6350d506b388ed88b8246ad86a39359c8a1a649d`  
		Last Modified: Tue, 13 Sep 2022 07:44:27 GMT  
		Size: 50.3 MB (50341630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61ba417daab3d8668a82f95060a31e0f183fb308d21cccd0e223d0b3226ca360`  
		Last Modified: Tue, 13 Sep 2022 07:45:18 GMT  
		Size: 167.3 MB (167303683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:127c72229893cae39596b2addc10d1c30d3a9eb8dcf843882e893c1776e1cbc9`  
		Last Modified: Wed, 14 Sep 2022 09:06:17 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:428202b49fac99d3e10920fd016a2c4fb184ba24c7e63fea68378e0891320923`  
		Last Modified: Wed, 14 Sep 2022 09:07:43 GMT  
		Size: 30.9 MB (30868628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d49fc0174e2d92917cb49fb60e6ea1102234c0d5a422be2fed59404547ad1d5`  
		Last Modified: Wed, 14 Sep 2022 09:07:37 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:3-bullseye` - linux; arm64 variant v8

```console
$ docker pull ruby@sha256:75ab10fab4a4fbbf9d3cbc2906ccc8565e4506b10dfbe1b7210bbd62e0e29add
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.4 MB (345446111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c329d1b0f25de8b981eaa7ff644f2523a46acf4d16296677844217f4bf9d3315`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 13 Sep 2022 02:10:41 GMT
ADD file:879fb0cd23107ac6f53581456074c7ff13c051aa262de3ca16ffa8475cf04dec in / 
# Tue, 13 Sep 2022 02:10:42 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 05:01:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 05:01:55 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 13 Sep 2022 05:02:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 05:02:56 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 17:23:41 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 13 Sep 2022 17:23:42 GMT
ENV LANG=C.UTF-8
# Tue, 13 Sep 2022 17:28:24 GMT
ENV RUBY_MAJOR=3.1
# Tue, 13 Sep 2022 17:28:25 GMT
ENV RUBY_VERSION=3.1.2
# Tue, 13 Sep 2022 17:28:26 GMT
ENV RUBY_DOWNLOAD_SHA256=ca10d017f8a1b6d247556622c841fc56b90c03b1803f87198da1e4fd3ec3bf2a
# Tue, 13 Sep 2022 17:30:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 13 Sep 2022 17:30:16 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 13 Sep 2022 17:30:17 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 13 Sep 2022 17:30:18 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Sep 2022 17:30:19 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 13 Sep 2022 17:30:20 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:10cff8997b4d4f243419e6bede830f1ac33f3d18c5200e5fb80e19333883ec2b`  
		Last Modified: Tue, 13 Sep 2022 02:15:49 GMT  
		Size: 53.7 MB (53691380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c9f2bf6f4deeb7ed2acd14f7997ec0a0cdf45b5b314051ddaab1911e22d997d`  
		Last Modified: Tue, 13 Sep 2022 05:09:57 GMT  
		Size: 5.1 MB (5148962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daa25dbffbabb85498e5d2c2d270f81ca67f9679617c9611bf18faf6ed4a09a0`  
		Last Modified: Tue, 13 Sep 2022 05:09:57 GMT  
		Size: 10.7 MB (10657461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9360b3024e18f921a2fcec8614f617312c87ea1a31b5c94c9c643535bde9775`  
		Last Modified: Tue, 13 Sep 2022 05:10:20 GMT  
		Size: 54.7 MB (54681497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9175ba771bff9348347af555b31874fcf715783d5265e9282369fbcb0f5048c5`  
		Last Modified: Tue, 13 Sep 2022 05:11:00 GMT  
		Size: 189.7 MB (189722604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ceb1e85177395604cdbfaa451635f0fce0553b17a87cb15ecb0cdb86a19537f4`  
		Last Modified: Tue, 13 Sep 2022 17:43:58 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd1bcb0fa9a08a7d9ba01dd024519c08cbca72f267324cef796140151fbab16a`  
		Last Modified: Tue, 13 Sep 2022 17:44:46 GMT  
		Size: 31.5 MB (31543865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe10e1769d82be8623777d70a37d662a105fc2cec48261fb6156a1251e27d9d5`  
		Last Modified: Tue, 13 Sep 2022 17:44:43 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:3-bullseye` - linux; 386

```console
$ docker pull ruby@sha256:c53b0016013e4ce42db55d9cb450a176e7abbd0e43f95988e49f8e7195fbedce
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.8 MB (358754718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adf1474d098489ae308aca2c7278b0f0d75f7c6ae3f971dff8b9f72bcd6938a1`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 13 Sep 2022 01:39:28 GMT
ADD file:7cd0a464573b537cf29f9a72bf3b895bfe96cce867ba3851402a98bca7272ca0 in / 
# Tue, 13 Sep 2022 01:39:28 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 04:49:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 04:49:20 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 13 Sep 2022 04:49:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 04:50:29 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 16:56:53 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 13 Sep 2022 16:56:54 GMT
ENV LANG=C.UTF-8
# Tue, 13 Sep 2022 17:01:36 GMT
ENV RUBY_MAJOR=3.1
# Tue, 13 Sep 2022 17:01:37 GMT
ENV RUBY_VERSION=3.1.2
# Tue, 13 Sep 2022 17:01:37 GMT
ENV RUBY_DOWNLOAD_SHA256=ca10d017f8a1b6d247556622c841fc56b90c03b1803f87198da1e4fd3ec3bf2a
# Tue, 13 Sep 2022 17:03:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 13 Sep 2022 17:03:32 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 13 Sep 2022 17:03:32 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 13 Sep 2022 17:03:33 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Sep 2022 17:03:35 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 13 Sep 2022 17:03:36 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:c56ebffcd7db97f938c62b9ad03478fefdde78fc8b85916da5d75054970df458`  
		Last Modified: Tue, 13 Sep 2022 01:44:50 GMT  
		Size: 56.0 MB (56009860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:415b2926e999b0f68db69f91ece9d0bb97c79da80699d3a387e1ac5681d01b1f`  
		Last Modified: Tue, 13 Sep 2022 04:57:05 GMT  
		Size: 5.3 MB (5290983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25017ef00a9bb56c10606c65882cf1a863cf50ae6da48809e67da77aad2607cc`  
		Last Modified: Tue, 13 Sep 2022 04:57:05 GMT  
		Size: 11.0 MB (11032776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7fcc67e3ad5b81078334e7e5fd41bc3736caa9c371ee3b620b5ba9dc06bb007`  
		Last Modified: Tue, 13 Sep 2022 04:57:28 GMT  
		Size: 55.9 MB (55923299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59a006a23cb4da6c14d11fa73e6fce2101a8361be662bee80773a324bc9fc426`  
		Last Modified: Tue, 13 Sep 2022 04:58:05 GMT  
		Size: 199.8 MB (199755008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca500ed6185bd2a49767d8acc6464bde22313667f58a02e813ded98a46b8c174`  
		Last Modified: Tue, 13 Sep 2022 17:17:43 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf03bdf09b2fd2b7e06d5a1a05e0c4663ce84e8af9d5f8fb6f9c85c3d8f7843c`  
		Last Modified: Tue, 13 Sep 2022 17:18:29 GMT  
		Size: 30.7 MB (30742448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce1c7006b1cfa18de8e39a01a22d60a214959fd8f27c915224b474f18100647c`  
		Last Modified: Tue, 13 Sep 2022 17:18:26 GMT  
		Size: 144.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:3-bullseye` - linux; mips64le

```console
$ docker pull ruby@sha256:ebf62295efb044eaf0165e33b697271309f341d356f635c0640d4ded19a60b26
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **333.4 MB (333389604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78fcdddd105127cb36225dba522e9bc0cc0e789bf3d263cc2f9bb88961787906`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 13 Sep 2022 01:10:24 GMT
ADD file:01a7dd1465cd33040941b52c4ec3699247b2ecf8c53533b3a234445013452157 in / 
# Tue, 13 Sep 2022 01:10:29 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 01:50:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 01:50:42 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 13 Sep 2022 01:52:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 01:57:47 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 22:41:38 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 13 Sep 2022 22:41:44 GMT
ENV LANG=C.UTF-8
# Tue, 13 Sep 2022 23:07:26 GMT
ENV RUBY_MAJOR=3.1
# Tue, 13 Sep 2022 23:07:32 GMT
ENV RUBY_VERSION=3.1.2
# Tue, 13 Sep 2022 23:07:37 GMT
ENV RUBY_DOWNLOAD_SHA256=ca10d017f8a1b6d247556622c841fc56b90c03b1803f87198da1e4fd3ec3bf2a
# Tue, 13 Sep 2022 23:18:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 13 Sep 2022 23:18:13 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 13 Sep 2022 23:18:19 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 13 Sep 2022 23:18:26 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Sep 2022 23:18:34 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 13 Sep 2022 23:18:41 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:ec9a494c35bfb06348155378649b8055458795ad2d004f471b887021323b94f2`  
		Last Modified: Tue, 13 Sep 2022 01:18:07 GMT  
		Size: 53.3 MB (53251789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ee02f93015f130da8dbe807a5b123a0f332fa75b55257f44d6a0f3c8fcc5da3`  
		Last Modified: Tue, 13 Sep 2022 02:05:49 GMT  
		Size: 5.1 MB (5123957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0f6f6b0c2dd6acd42de4af694f71bf39f08a8daf7243600350b63f5c4b85787`  
		Last Modified: Tue, 13 Sep 2022 02:05:50 GMT  
		Size: 10.7 MB (10660929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5830a306342df3564e840a58fd4c03e8813c294edba4954f0791454308788492`  
		Last Modified: Tue, 13 Sep 2022 02:06:39 GMT  
		Size: 53.3 MB (53304679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfd9b19e99fe0e23455f7bee784dfbba073d514c9d7b7b2d2fb287d2cb42cf2a`  
		Last Modified: Tue, 13 Sep 2022 02:08:43 GMT  
		Size: 179.0 MB (178963942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f2366ca0728d18f6da75a756bdb796941cbe709aa31f27f4907d0ac0389f367`  
		Last Modified: Wed, 14 Sep 2022 00:14:26 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f32617edeb034fb862671a693964f7cc7a64850cf1339133239e9a662ba51e7`  
		Last Modified: Wed, 14 Sep 2022 00:15:37 GMT  
		Size: 32.1 MB (32083965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5504e6a27259e242056dfd414e3a2e7dc334fdc30b439d5846126814497a7919`  
		Last Modified: Wed, 14 Sep 2022 00:15:23 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:3-bullseye` - linux; ppc64le

```console
$ docker pull ruby@sha256:3e45425cfea8096c8bb1736f3f1dc3534ba9a8058f5080094ba7fea5f271096f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.6 MB (363579901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d67234120c7caa98b971add160abb87d76f2b65a36a6136d54c175e1b2b39b8`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 13 Sep 2022 02:07:34 GMT
ADD file:01cdcbf6300ec08ebb8bff41970509b38aff6d26164dea3fb476a6254e441e9b in / 
# Tue, 13 Sep 2022 02:07:37 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 05:14:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 05:14:18 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 13 Sep 2022 05:14:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 05:16:47 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 14:00:54 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 13 Sep 2022 14:00:54 GMT
ENV LANG=C.UTF-8
# Tue, 13 Sep 2022 14:04:18 GMT
ENV RUBY_MAJOR=3.1
# Tue, 13 Sep 2022 14:04:18 GMT
ENV RUBY_VERSION=3.1.2
# Tue, 13 Sep 2022 14:04:18 GMT
ENV RUBY_DOWNLOAD_SHA256=ca10d017f8a1b6d247556622c841fc56b90c03b1803f87198da1e4fd3ec3bf2a
# Tue, 13 Sep 2022 14:07:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 13 Sep 2022 14:07:15 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 13 Sep 2022 14:07:15 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 13 Sep 2022 14:07:15 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Sep 2022 14:07:16 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 13 Sep 2022 14:07:17 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:7d6144dab736564be3fb6a092ba7b12047adae858b56388b2c30f57e044d7565`  
		Last Modified: Tue, 13 Sep 2022 02:13:01 GMT  
		Size: 58.9 MB (58902594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e7fa9a7ad3fd314802c655b3450a54569fcfa864dbfa0229721d8bc79f2a0b7`  
		Last Modified: Tue, 13 Sep 2022 05:24:55 GMT  
		Size: 5.4 MB (5412954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2712f6dbb2a2d0105245643b5cbd920b09c66574e06dba7618247607f8c8827b`  
		Last Modified: Tue, 13 Sep 2022 05:24:56 GMT  
		Size: 11.6 MB (11629060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eafe3c07d4e203ed51c77052a03bb7bf8728801864abea6cce0c4b15ec1e845`  
		Last Modified: Tue, 13 Sep 2022 05:25:28 GMT  
		Size: 58.9 MB (58866249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b447ed866efce197a7056139aac56bd68feee2b250a9ce18d4800c47d7fd60e`  
		Last Modified: Tue, 13 Sep 2022 05:26:29 GMT  
		Size: 196.2 MB (196194089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91d196d48a5a515632225e8015ac2347606287518b51255d972babc9907e72a6`  
		Last Modified: Tue, 13 Sep 2022 14:16:11 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:317df43675256704c332a4254986663c4bf30e9eac3278a0df36005afbd636cc`  
		Last Modified: Tue, 13 Sep 2022 14:16:47 GMT  
		Size: 32.6 MB (32574579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14064227cdfa4e26af3029f7f70ff20af4c551f7fd96094cfc04ab62e27f41e3`  
		Last Modified: Tue, 13 Sep 2022 14:16:42 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:3-bullseye` - linux; s390x

```console
$ docker pull ruby@sha256:f6fafc35dae74c47478c2f02f15290e43196e03fe5f92d37d32e0109c3ae8702
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.3 MB (328298605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8623434da0f62c47e6d4012c28d385e43f7fb7ab2e40dd77a612999286be48af`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 13 Sep 2022 00:47:47 GMT
ADD file:2965b342d27ea25d073bb5f216362150cb8ec0e05df43fae8e4ee6251006d17d in / 
# Tue, 13 Sep 2022 00:47:50 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 01:25:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 01:25:37 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 13 Sep 2022 01:26:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 01:27:13 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 07:32:36 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 13 Sep 2022 07:32:36 GMT
ENV LANG=C.UTF-8
# Tue, 13 Sep 2022 07:35:14 GMT
ENV RUBY_MAJOR=3.1
# Tue, 13 Sep 2022 07:35:14 GMT
ENV RUBY_VERSION=3.1.2
# Tue, 13 Sep 2022 07:35:14 GMT
ENV RUBY_DOWNLOAD_SHA256=ca10d017f8a1b6d247556622c841fc56b90c03b1803f87198da1e4fd3ec3bf2a
# Tue, 13 Sep 2022 07:37:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 13 Sep 2022 07:37:15 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 13 Sep 2022 07:37:15 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 13 Sep 2022 07:37:15 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Sep 2022 07:37:16 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 13 Sep 2022 07:37:17 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:cf58bfabf9fb5ab735277c32678e319fed106496e2f1070ac6bcf35a57d3870e`  
		Last Modified: Tue, 13 Sep 2022 00:52:18 GMT  
		Size: 53.3 MB (53264823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce515b66a74a291f416a7fb9b6e39594047957a72b0b2f38367f724790639590`  
		Last Modified: Tue, 13 Sep 2022 01:32:46 GMT  
		Size: 5.1 MB (5146951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36bf6be09afafe08d5aecef2a5a139e863d43fb30c9c5dd6aed8fe8bee2c15c7`  
		Last Modified: Tue, 13 Sep 2022 01:32:46 GMT  
		Size: 10.8 MB (10765828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff4c0b442ebbbf2a3574149920262648ea94715375d8db9298b73fd7de702ffc`  
		Last Modified: Tue, 13 Sep 2022 01:33:03 GMT  
		Size: 54.1 MB (54055046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b7dcf62b7dcab5e57c828202a74ebfd9b811dd6d4b14740d1d77f87028f8e95`  
		Last Modified: Tue, 13 Sep 2022 01:33:30 GMT  
		Size: 172.8 MB (172824389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31e815226da10212c06f81743927c6db24bc74a7041ea05434496fce15d7dc16`  
		Last Modified: Tue, 13 Sep 2022 07:45:04 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3ed3e57fa06ade2f84e9ea59e13ca339356fcaa869989d0a0966577c924ed53`  
		Last Modified: Tue, 13 Sep 2022 07:45:25 GMT  
		Size: 32.2 MB (32241193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87d8bec6ceb2c464bba6def485a2b835264e123b614e7a8cefbdc45c95291bc1`  
		Last Modified: Tue, 13 Sep 2022 07:45:23 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
