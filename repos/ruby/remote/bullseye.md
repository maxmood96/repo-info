## `ruby:bullseye`

```console
$ docker pull ruby@sha256:625306cc41faab441c5e414daccd94aad0c43ea33fbdc175e2defa865441b536
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

### `ruby:bullseye` - linux; amd64

```console
$ docker pull ruby@sha256:a177d317adf31ca481048435d148233f58a57e9ffcfcf82447fd884356e1ea61
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **356.8 MB (356807891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:884e07bb5d3992ed252d8857a5530b878a60291d34a9fd07ef29cba691a51bd3`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 27 Jul 2023 23:24:55 GMT
ADD file:b493776b6d91132ce50735e2d82076620774a1e0a690cf96777ddd6b85f513ef in / 
# Thu, 27 Jul 2023 23:24:55 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 03:02:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 03:02:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 03:03:33 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 14:43:50 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Fri, 28 Jul 2023 14:43:50 GMT
ENV LANG=C.UTF-8
# Fri, 28 Jul 2023 14:54:45 GMT
ENV RUBY_MAJOR=3.2
# Fri, 28 Jul 2023 14:54:45 GMT
ENV RUBY_VERSION=3.2.2
# Fri, 28 Jul 2023 14:54:45 GMT
ENV RUBY_DOWNLOAD_SHA256=4b352d0f7ec384e332e3e44cdbfdcd5ff2d594af3c8296b5636c710975149e23
# Fri, 28 Jul 2023 14:56:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.25.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='5cc9ffd1026e82e7fb2eec2121ad71f4b0f044e88bca39207b3f6b769aaa799c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.25.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e189948e396d47254103a49c987e7fb0e5dd8e34b200aa4481ecc4b8e41fb929' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.66.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Fri, 28 Jul 2023 14:56:59 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 28 Jul 2023 14:56:59 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 28 Jul 2023 14:56:59 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 28 Jul 2023 14:56:59 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME"
# Fri, 28 Jul 2023 14:56:59 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:9a9e034800a1747ea288f38f6087c036acac99dd3ec5255bf7798abd8c23a304`  
		Last Modified: Thu, 27 Jul 2023 23:29:45 GMT  
		Size: 55.1 MB (55055571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd91c1fad56dc2c387d016dbcaaecfbfb5e2b479f8dd644803dead02566f3479`  
		Last Modified: Fri, 28 Jul 2023 03:08:24 GMT  
		Size: 15.8 MB (15760585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dd6a2c0cfa3eb4e8012b3f2df526acc8711a4a9515e0e968419a8ab1e9899e4`  
		Last Modified: Fri, 28 Jul 2023 03:08:40 GMT  
		Size: 54.6 MB (54585034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83d4a6da525a13b128e2e4f41081a5af59d2dda8045d40b207510cc3fdc84e1a`  
		Last Modified: Fri, 28 Jul 2023 03:09:11 GMT  
		Size: 196.9 MB (196851463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:850b24fff20532b447981a19a32d9611e19b91b2258bb4ed69a13f096a04b150`  
		Last Modified: Fri, 28 Jul 2023 15:19:56 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b306f3270c46a74b6afdd991b25f2c451c4eaf7b3924052c2e29011d316913a5`  
		Last Modified: Fri, 28 Jul 2023 15:21:18 GMT  
		Size: 34.6 MB (34554862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd5bee43cb44af4904aaa7943de0257bdd3d919d9b39c25c3dd1c29b90533fe0`  
		Last Modified: Fri, 28 Jul 2023 15:21:14 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:bullseye` - linux; arm variant v5

```console
$ docker pull ruby@sha256:9188d5cd03d441626ced4da293b5c399ccde077d9c98f9a42203beccf4c894a0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.8 MB (325795886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac0ae47e4cd97cd5da00580b113b98707e93032df16130a7a70737f8b1036c9d`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 27 Jul 2023 23:48:37 GMT
ADD file:58d46c9e9d20ce33072df369a18845e23a2b275e65c9d7da000c45c336c9c660 in / 
# Thu, 27 Jul 2023 23:48:37 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 06:21:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 06:21:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 06:23:15 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 18:20:06 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Fri, 28 Jul 2023 18:20:06 GMT
ENV LANG=C.UTF-8
# Fri, 28 Jul 2023 18:24:25 GMT
ENV RUBY_MAJOR=3.2
# Fri, 28 Jul 2023 18:24:25 GMT
ENV RUBY_VERSION=3.2.2
# Fri, 28 Jul 2023 18:24:25 GMT
ENV RUBY_DOWNLOAD_SHA256=4b352d0f7ec384e332e3e44cdbfdcd5ff2d594af3c8296b5636c710975149e23
# Fri, 28 Jul 2023 18:26:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.25.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='5cc9ffd1026e82e7fb2eec2121ad71f4b0f044e88bca39207b3f6b769aaa799c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.25.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e189948e396d47254103a49c987e7fb0e5dd8e34b200aa4481ecc4b8e41fb929' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.66.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Fri, 28 Jul 2023 18:26:19 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 28 Jul 2023 18:26:19 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 28 Jul 2023 18:26:19 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 28 Jul 2023 18:26:19 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME"
# Fri, 28 Jul 2023 18:26:19 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:2d60a86478b61a7638bb5d1f275e9d6ae0ea994d53a8bb22fce9279ebe477749`  
		Last Modified: Thu, 27 Jul 2023 23:51:48 GMT  
		Size: 52.6 MB (52557094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81f9604556d022f6e4e1026e238e346fd3c2c68a047d7bd22ce614554e53ec7f`  
		Last Modified: Fri, 28 Jul 2023 06:26:20 GMT  
		Size: 15.4 MB (15369083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8694358714da9e346430366f87b195f504e0ffd802b60753eca6d435e91c1194`  
		Last Modified: Fri, 28 Jul 2023 06:26:38 GMT  
		Size: 52.3 MB (52340803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74366c4b606c5da81eb44061bf8c2c2c62d20818c5196961d98c373ca416cf71`  
		Last Modified: Fri, 28 Jul 2023 06:27:15 GMT  
		Size: 175.0 MB (175038754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7b051c7ceda15d848b8d99b058c2954bf7c471abe33ab961d19302c919fa243`  
		Last Modified: Fri, 28 Jul 2023 18:33:36 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7099cac781de274586360e6771f55acf46cb3bc851729a594a999b4aa7c85e2`  
		Last Modified: Fri, 28 Jul 2023 18:34:19 GMT  
		Size: 30.5 MB (30489776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65560d1298f9ea5d22ab48b88fdd91da577caa7c7857a6a8c0af039fb2f890bb`  
		Last Modified: Fri, 28 Jul 2023 18:34:16 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:bullseye` - linux; arm variant v7

```console
$ docker pull ruby@sha256:4eae8a60fdcc4af7e28b709857a8b3282bea93f4c8cc2d878200b7fcc9e7e021
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.2 MB (313173045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdaff82e4fe7ec3fd3d4903c9940dcb8181183c842e8c6abc496c2b6853131e7`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 27 Jul 2023 23:58:01 GMT
ADD file:3014d2ee0e0e882151b5295faeb81a24b4d6f9e0f92f3ba969ccffb2bd8a6d76 in / 
# Thu, 27 Jul 2023 23:58:03 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 01:59:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 02:00:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 02:01:34 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 15:28:48 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Fri, 28 Jul 2023 15:28:49 GMT
ENV LANG=C.UTF-8
# Fri, 28 Jul 2023 15:39:37 GMT
ENV RUBY_MAJOR=3.2
# Fri, 28 Jul 2023 15:39:37 GMT
ENV RUBY_VERSION=3.2.2
# Fri, 28 Jul 2023 15:39:37 GMT
ENV RUBY_DOWNLOAD_SHA256=4b352d0f7ec384e332e3e44cdbfdcd5ff2d594af3c8296b5636c710975149e23
# Fri, 28 Jul 2023 15:41:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.25.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='5cc9ffd1026e82e7fb2eec2121ad71f4b0f044e88bca39207b3f6b769aaa799c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.25.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e189948e396d47254103a49c987e7fb0e5dd8e34b200aa4481ecc4b8e41fb929' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.66.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Fri, 28 Jul 2023 15:41:26 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 28 Jul 2023 15:41:26 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 28 Jul 2023 15:41:26 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 28 Jul 2023 15:41:27 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME"
# Fri, 28 Jul 2023 15:41:27 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:e8dff7ada2c26d71087c5ec6294d1adc4dcf7d688824a079e89e3bedd9a34fa6`  
		Last Modified: Fri, 28 Jul 2023 00:03:32 GMT  
		Size: 50.2 MB (50218549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79aa87808c3418d080808a65b8798629209aa23ef6dd21a2495b3d99e8367242`  
		Last Modified: Fri, 28 Jul 2023 02:07:34 GMT  
		Size: 14.9 MB (14868822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:017eba29227541589419d3d28eb04fefe86aa7fa5ec809386432bedd612c979f`  
		Last Modified: Fri, 28 Jul 2023 02:07:51 GMT  
		Size: 50.4 MB (50355308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c6945de828a2eb1ee480a75a3c86b584d5eb7eb1d37bca07eccd5052961c49d`  
		Last Modified: Fri, 28 Jul 2023 02:08:20 GMT  
		Size: 167.3 MB (167332243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d07c2ddc36e80d211057c3a57a8508c4636e12f842623f2393766901609e7a7`  
		Last Modified: Fri, 28 Jul 2023 16:09:07 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c18db67bc12728d7d14948c76f74c10b97f1ee92d8a023cae4696d8281db98a`  
		Last Modified: Fri, 28 Jul 2023 16:10:28 GMT  
		Size: 30.4 MB (30397748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04d313a37862036ad23f383ebc5bb7b9f3d5eef939fb3f97bdbfc0407722987c`  
		Last Modified: Fri, 28 Jul 2023 16:10:24 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:bullseye` - linux; arm64 variant v8

```console
$ docker pull ruby@sha256:e4429dec60fa6e0dfc0c4784ede2331d7058ff48d404789934c28cbe871811ec
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.3 MB (348338037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baea98ef18e1a34fd34748971846aff205fc474a9575674c1bb1da700afb5ef9`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 15 Aug 2023 23:40:03 GMT
ADD file:8973cddb2d84a543b71001635599951bea6485a3526ae4ff916443b584864c83 in / 
# Tue, 15 Aug 2023 23:40:04 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:23:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 01:23:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 01:24:02 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 09:12:53 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 16 Aug 2023 09:12:53 GMT
ENV LANG=C.UTF-8
# Wed, 16 Aug 2023 09:21:12 GMT
ENV RUBY_MAJOR=3.2
# Wed, 16 Aug 2023 09:21:12 GMT
ENV RUBY_VERSION=3.2.2
# Wed, 16 Aug 2023 09:21:12 GMT
ENV RUBY_DOWNLOAD_SHA256=4b352d0f7ec384e332e3e44cdbfdcd5ff2d594af3c8296b5636c710975149e23
# Wed, 16 Aug 2023 09:22:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.25.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='5cc9ffd1026e82e7fb2eec2121ad71f4b0f044e88bca39207b3f6b769aaa799c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.25.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e189948e396d47254103a49c987e7fb0e5dd8e34b200aa4481ecc4b8e41fb929' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.66.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 16 Aug 2023 09:22:50 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 16 Aug 2023 09:22:50 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 16 Aug 2023 09:22:50 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Aug 2023 09:22:51 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME"
# Wed, 16 Aug 2023 09:22:51 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:e837d9f05c625de5b814b851adbc03559ba02ea7078f57c81a01e18fc65bf42b`  
		Last Modified: Tue, 15 Aug 2023 23:43:37 GMT  
		Size: 53.7 MB (53704779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9abd0588cbb35597a784666f0dc97746829b8b4b730b73e8781fb90678ffef22`  
		Last Modified: Wed, 16 Aug 2023 01:39:26 GMT  
		Size: 15.7 MB (15746520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85a8864a846a08e10fbf877e73678d1f0803227b00a1b16d9ba948070c6e58f6`  
		Last Modified: Wed, 16 Aug 2023 01:39:40 GMT  
		Size: 54.7 MB (54676094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0db5ec7e6673db06ba035c7c57c4c31b84c89e803ceeb3268a02b5175537b120`  
		Last Modified: Wed, 16 Aug 2023 01:40:04 GMT  
		Size: 189.8 MB (189777874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d40b9648569b951b6cecdb356d1dd662152c3b9f4668c4a6dc674523d453b0e7`  
		Last Modified: Wed, 16 Aug 2023 09:40:07 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ade77ecdc7f2e08c770129018636659ed9f52ed8bef352b90dc791d095a6d3a`  
		Last Modified: Wed, 16 Aug 2023 09:41:18 GMT  
		Size: 34.4 MB (34432394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35cf6c8edbbc18925a3921bb90f727412c04a5e8d06ce8012350ad83385cfffa`  
		Last Modified: Wed, 16 Aug 2023 09:41:15 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:bullseye` - linux; 386

```console
$ docker pull ruby@sha256:8d7c3e142753c7ba9beb7c0128f508744ca9b8c59be8e2c6294a71ce652a0794
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.4 MB (358430171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb1410397c94b9191da88c3150a8c51befb1c6a2b91cdafacc8c6fdfd1c9a50b`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 15 Aug 2023 23:39:11 GMT
ADD file:efc88a19b31e68ca41f555bcc51338b0f135cbbd72b90637d8c73969d53addd2 in / 
# Tue, 15 Aug 2023 23:39:12 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 00:27:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 00:28:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 00:29:18 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 08:10:05 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 16 Aug 2023 08:10:05 GMT
ENV LANG=C.UTF-8
# Wed, 16 Aug 2023 08:24:55 GMT
ENV RUBY_MAJOR=3.2
# Wed, 16 Aug 2023 08:24:55 GMT
ENV RUBY_VERSION=3.2.2
# Wed, 16 Aug 2023 08:24:55 GMT
ENV RUBY_DOWNLOAD_SHA256=4b352d0f7ec384e332e3e44cdbfdcd5ff2d594af3c8296b5636c710975149e23
# Wed, 16 Aug 2023 08:28:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.25.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='5cc9ffd1026e82e7fb2eec2121ad71f4b0f044e88bca39207b3f6b769aaa799c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.25.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e189948e396d47254103a49c987e7fb0e5dd8e34b200aa4481ecc4b8e41fb929' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.66.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 16 Aug 2023 08:28:03 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 16 Aug 2023 08:28:03 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 16 Aug 2023 08:28:04 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Aug 2023 08:28:04 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME"
# Wed, 16 Aug 2023 08:28:04 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:822e033fa7b169545d5890de01438a9dd87774ff938ff440e823a3ec3f73996d`  
		Last Modified: Tue, 15 Aug 2023 23:43:47 GMT  
		Size: 56.0 MB (56040520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52269d7973f191a6cedbd1545cfe71ec1c659072be43d51f8741b18f05423e2b`  
		Last Modified: Wed, 16 Aug 2023 00:36:01 GMT  
		Size: 16.3 MB (16263743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c16fc8bca4c44908804dd201eac5ad8d9316cffd0de391511a9da2fcb3fb48c0`  
		Last Modified: Wed, 16 Aug 2023 00:36:22 GMT  
		Size: 55.9 MB (55922930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1da0010c52f973a4d9c39043ad90ee5727579d72d1a34209b0ccc3f1f80515cc`  
		Last Modified: Wed, 16 Aug 2023 00:37:05 GMT  
		Size: 199.8 MB (199768301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73dbe03fcb563401bb09a640b7d7c1c171413b730006d7de2067cda2e0897276`  
		Last Modified: Wed, 16 Aug 2023 09:01:39 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beab688dadfb983565e5609e296745542baa2ff143e3b1f5281922245c64265e`  
		Last Modified: Wed, 16 Aug 2023 09:02:58 GMT  
		Size: 30.4 MB (30434301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:136ddea537c7ff00e1cb538637c8b3cda237d5128d8997ed28b5c7b89ea66f89`  
		Last Modified: Wed, 16 Aug 2023 09:02:54 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:bullseye` - linux; mips64le

```console
$ docker pull ruby@sha256:dd5ee982a9456a0f933f68dc1ed9ecebfd4796958f091078fcc33a0134b7d629
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.5 MB (332473983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:605746fa530be02ed8bb70c1ee119115d974bbe138c4ed4e6822da003a5b7729`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 27 Jul 2023 23:11:57 GMT
ADD file:ccccca3acf3759fd714159d3c3beff86d84a9751b947e148348d523272fc1bb9 in / 
# Thu, 27 Jul 2023 23:12:02 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 01:19:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 01:21:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 01:26:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 29 Jul 2023 02:58:13 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Sat, 29 Jul 2023 02:58:18 GMT
ENV LANG=C.UTF-8
# Sat, 29 Jul 2023 03:49:28 GMT
ENV RUBY_MAJOR=3.2
# Sat, 29 Jul 2023 03:49:34 GMT
ENV RUBY_VERSION=3.2.2
# Sat, 29 Jul 2023 03:49:40 GMT
ENV RUBY_DOWNLOAD_SHA256=4b352d0f7ec384e332e3e44cdbfdcd5ff2d594af3c8296b5636c710975149e23
# Sat, 29 Jul 2023 04:00:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.25.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='5cc9ffd1026e82e7fb2eec2121ad71f4b0f044e88bca39207b3f6b769aaa799c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.25.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e189948e396d47254103a49c987e7fb0e5dd8e34b200aa4481ecc4b8e41fb929' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.66.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Sat, 29 Jul 2023 04:00:15 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 29 Jul 2023 04:00:21 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 29 Jul 2023 04:00:28 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 29 Jul 2023 04:00:37 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME"
# Sat, 29 Jul 2023 04:00:43 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:9d9a0c35af83dc10b6307f02a48749b4d8024123530a89d5173f70981e00b9e3`  
		Last Modified: Thu, 27 Jul 2023 23:23:10 GMT  
		Size: 53.3 MB (53270927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f12aa6a7cf9a2dd39c4a36e47b26cc0ca1c9e8ad55d149bdf74bcbc866c92718`  
		Last Modified: Fri, 28 Jul 2023 01:34:45 GMT  
		Size: 15.5 MB (15520522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cedbdbe02029d723bc1414bf8094fe7b1ac71ed4460a31db174ac0e221fc1b3`  
		Last Modified: Fri, 28 Jul 2023 01:35:29 GMT  
		Size: 53.3 MB (53306734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcffa2b1acd2a62702740ee307e4ae143652253f14c589200b83dad48f46522f`  
		Last Modified: Fri, 28 Jul 2023 01:37:23 GMT  
		Size: 179.0 MB (178972969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:521285098e87d87068bab0486342b35accdcc6dbdfc21fcc98bc8b334fc93cbd`  
		Last Modified: Sat, 29 Jul 2023 05:30:19 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a56fb106276c78f40bea14a75e640acebed79e3937d0eab5fdc9765679abcc65`  
		Last Modified: Sat, 29 Jul 2023 05:32:27 GMT  
		Size: 31.4 MB (31402489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:690a25fedb998a3529527f7a12ad822356528f122fea1149147a4eb9966f4dd4`  
		Last Modified: Sat, 29 Jul 2023 05:32:14 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:bullseye` - linux; ppc64le

```console
$ docker pull ruby@sha256:44130d816503361d4564ece96f599395cb8b6befe696b4cdca7ea56f2cb70e94
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **362.7 MB (362746765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab4536a47545656dff04d429a6c852575fe4306b605b82f830b066f690557d5c`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 27 Jul 2023 23:23:20 GMT
ADD file:c9c051b70d4b5c059dc4dfc25c2ce056efb99058bbea4911c346eaf8c90ea938 in / 
# Thu, 27 Jul 2023 23:23:23 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 01:52:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 01:52:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 01:55:29 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 08:12:51 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Fri, 28 Jul 2023 08:12:53 GMT
ENV LANG=C.UTF-8
# Fri, 28 Jul 2023 08:39:48 GMT
ENV RUBY_MAJOR=3.2
# Fri, 28 Jul 2023 08:39:49 GMT
ENV RUBY_VERSION=3.2.2
# Fri, 28 Jul 2023 08:39:50 GMT
ENV RUBY_DOWNLOAD_SHA256=4b352d0f7ec384e332e3e44cdbfdcd5ff2d594af3c8296b5636c710975149e23
# Fri, 28 Jul 2023 08:43:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.25.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='5cc9ffd1026e82e7fb2eec2121ad71f4b0f044e88bca39207b3f6b769aaa799c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.25.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e189948e396d47254103a49c987e7fb0e5dd8e34b200aa4481ecc4b8e41fb929' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.66.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Fri, 28 Jul 2023 08:43:26 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 28 Jul 2023 08:43:26 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 28 Jul 2023 08:43:27 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 28 Jul 2023 08:43:28 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME"
# Fri, 28 Jul 2023 08:43:29 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:ba7a048f0d1295609b34eb062a51486e1f3e5831711b4569a3583b1e8ad30aff`  
		Last Modified: Thu, 27 Jul 2023 23:29:55 GMT  
		Size: 58.9 MB (58927464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e92f26dafc18fcd8118c1ad9dd5b1453a087cf7a240b62c35c083303f922a0c`  
		Last Modified: Fri, 28 Jul 2023 02:00:56 GMT  
		Size: 16.8 MB (16752895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7a0c9164ca3ed074af639cd3219d80005db64890c47bc0077c3d4b7dda542f5`  
		Last Modified: Fri, 28 Jul 2023 02:01:23 GMT  
		Size: 58.9 MB (58865128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a01e1f9aa5feb87e4bee1ff38a812aadb8e40dde7f1f19b76bd063fe938374b7`  
		Last Modified: Fri, 28 Jul 2023 02:02:20 GMT  
		Size: 196.2 MB (196197316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2c5fb21b25206761f75a45483a91b8c2a7228ce87a2808db5e636b0f440df95`  
		Last Modified: Fri, 28 Jul 2023 09:14:48 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb4934cbca212014e67f78cf3ef0e09c9018e36f43ba52388a7a5ff23635e666`  
		Last Modified: Fri, 28 Jul 2023 09:16:43 GMT  
		Size: 32.0 MB (32003585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:153d5d8d358e1e82b90c719a6af1f7339349a02bb3c2c4d6920f7867157b4889`  
		Last Modified: Fri, 28 Jul 2023 09:16:38 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:bullseye` - linux; s390x

```console
$ docker pull ruby@sha256:ed9073904e9f1606056d5123b81a8a77c054bc92bab6329c24c51f963c913781
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.5 MB (327478927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de6b1921e30b772222c9b5feee0ab8ace71d4cca85be37444e23e45f0073f205`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 27 Jul 2023 23:47:23 GMT
ADD file:6e134e7958a9106ced0feb988945d71421340aa36ed7d8ad28fe5e91ab70df62 in / 
# Thu, 27 Jul 2023 23:47:27 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 01:57:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 01:57:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 01:58:38 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 12:27:14 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Fri, 28 Jul 2023 12:27:14 GMT
ENV LANG=C.UTF-8
# Fri, 28 Jul 2023 12:36:14 GMT
ENV RUBY_MAJOR=3.2
# Fri, 28 Jul 2023 12:36:14 GMT
ENV RUBY_VERSION=3.2.2
# Fri, 28 Jul 2023 12:36:14 GMT
ENV RUBY_DOWNLOAD_SHA256=4b352d0f7ec384e332e3e44cdbfdcd5ff2d594af3c8296b5636c710975149e23
# Fri, 28 Jul 2023 12:37:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.25.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='5cc9ffd1026e82e7fb2eec2121ad71f4b0f044e88bca39207b3f6b769aaa799c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.25.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e189948e396d47254103a49c987e7fb0e5dd8e34b200aa4481ecc4b8e41fb929' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.66.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Fri, 28 Jul 2023 12:38:00 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 28 Jul 2023 12:38:00 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 28 Jul 2023 12:38:00 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 28 Jul 2023 12:38:00 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME"
# Fri, 28 Jul 2023 12:38:00 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:4909b03e906e0e2f8a83103a5b44c902afcad9d1bdcabcbc71058f3165c169e4`  
		Last Modified: Thu, 27 Jul 2023 23:52:31 GMT  
		Size: 53.3 MB (53289052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a34d5a08d4e924ca54ebe553088d1a5dd390793877e65057151e872097734087`  
		Last Modified: Fri, 28 Jul 2023 02:03:15 GMT  
		Size: 15.6 MB (15631928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a953dc6fcabca93bc35dfdfcc0839fa3005e0928d6f50e2992f3631f3a2ab280`  
		Last Modified: Fri, 28 Jul 2023 02:03:28 GMT  
		Size: 54.1 MB (54061236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff9b90cc57f3ee5c3609c0659205c6420bedb7231247a32635d21d70fb817e0a`  
		Last Modified: Fri, 28 Jul 2023 02:03:54 GMT  
		Size: 172.9 MB (172855749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8812407bbd60f31789990afeb15bb790a184bff372efa20c22bc5a23c2b948f9`  
		Last Modified: Fri, 28 Jul 2023 12:55:14 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39779ae27f14063959ec4f00dbd08dd7d3301e35f59addc49f7794b173448374`  
		Last Modified: Fri, 28 Jul 2023 12:56:07 GMT  
		Size: 31.6 MB (31640586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08ee214b1388eee3fc6e05a7bbdc13f253f56ae302ff75549032f73e0896f17d`  
		Last Modified: Fri, 28 Jul 2023 12:56:04 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
