## `ruby:latest`

```console
$ docker pull ruby@sha256:a67dcbc840ad773775c250f0caef2554a0c6f487289c6b113e1fa4aa1e175887
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `ruby:latest` - linux; amd64

```console
$ docker pull ruby@sha256:57d8acc4c18f9736f728ade0cdeccf5968adc08f66004ce586d9ef366a4d2b12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **385.4 MB (385397232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddebdf046ee9f42de6755a25f67c4d7625deebd2612ec51ce5b4882ffc5d4b32`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 14 May 2024 01:27:51 GMT
ADD file:b9a9fc37b874060c713002ae1ac220f097edd7c6576116c22bb15aad8229b1b3 in / 
# Tue, 14 May 2024 01:27:51 GMT
CMD ["bash"]
# Tue, 14 May 2024 02:54:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 02:54:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 02:55:51 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 30 May 2024 05:03:18 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Thu, 30 May 2024 05:03:18 GMT
ENV LANG=C.UTF-8
# Thu, 30 May 2024 05:03:18 GMT
ENV RUBY_VERSION=3.3.2
# Thu, 30 May 2024 05:03:18 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.2.tar.xz
# Thu, 30 May 2024 05:03:18 GMT
ENV RUBY_DOWNLOAD_SHA256=b5e8a8ed4a47cdd9a3358b5bdd998c37bd9e971ca63766a37d5ae5933fdb69f1
# Thu, 30 May 2024 05:03:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 30 May 2024 05:03:18 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 30 May 2024 05:03:18 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 30 May 2024 05:03:18 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 May 2024 05:03:18 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Thu, 30 May 2024 05:03:18 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:c6cf28de8a067787ee0d08f8b01d7f1566a508b56f6e549687b41dfd375f12c7`  
		Last Modified: Tue, 14 May 2024 01:32:07 GMT  
		Size: 49.6 MB (49576390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:891494355808bdd3db5552f0d3723fd0fa826675f774853796fafa221d850d42`  
		Last Modified: Tue, 14 May 2024 03:04:06 GMT  
		Size: 24.1 MB (24050100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6582c62583ef22717db8d306b1d6a0c288089ff607d9c0d2d81c4f8973cbfee3`  
		Last Modified: Tue, 14 May 2024 03:04:25 GMT  
		Size: 64.1 MB (64142371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf2c3e352f3d2eed4eda4feeed44a1022a881058df20ac0584db70c138b041e2`  
		Last Modified: Tue, 14 May 2024 03:05:02 GMT  
		Size: 211.2 MB (211207185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccbe3f7225498af347d77418d8b8e251b834bcc593fb81df95d6517f90537280`  
		Last Modified: Thu, 30 May 2024 23:59:53 GMT  
		Size: 200.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2102701ed4c44498218ae2deb328bafcc425f30543a4f4f5acbb58bb2804d167`  
		Last Modified: Thu, 30 May 2024 23:59:54 GMT  
		Size: 36.4 MB (36420843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa696053400d802f63d6c9d9d98f67f52894df7872c1d1a060952e73028a64f2`  
		Last Modified: Thu, 30 May 2024 23:59:35 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:latest` - unknown; unknown

```console
$ docker pull ruby@sha256:2aff27de16fa1498fb71ce37dcbc7a8a67539c3a4ebafdb4607696fa8a18cb54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15485599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05ce092826bee9c6bf9e0fc912a0cd854ca5c43bfda0bc8636e6c61d676a4059`

```dockerfile
```

-	Layers:
	-	`sha256:ac2a5cff9a281df81a0f4c485752ee8b686cd9cffc53d91a076e85afe864eb58`  
		Last Modified: Thu, 30 May 2024 23:59:54 GMT  
		Size: 15.5 MB (15462257 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e476b89abd998435387a6665e2a85013a955c41171a0a13c5210d19ffb2460a`  
		Last Modified: Thu, 30 May 2024 23:59:53 GMT  
		Size: 23.3 KB (23342 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:latest` - linux; arm variant v5

```console
$ docker pull ruby@sha256:22f5af25936f2e0620f14fc8585f7805c6a0d083e683920b2380c047e9d2c820
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.0 MB (348964166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c41e871a3f8a2e346dfa2e4982c4085d9c057230e5ab7617273b892ccab621c8`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 14 May 2024 00:48:25 GMT
ADD file:cd62e5a70676cac6ab9314bf7583f7ed4056908c492f302f1243edbd35066bfd in / 
# Tue, 14 May 2024 00:48:26 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:11:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 01:11:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 01:13:15 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 30 May 2024 05:03:18 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Thu, 30 May 2024 05:03:18 GMT
ENV LANG=C.UTF-8
# Thu, 30 May 2024 05:03:18 GMT
ENV RUBY_VERSION=3.3.2
# Thu, 30 May 2024 05:03:18 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.2.tar.xz
# Thu, 30 May 2024 05:03:18 GMT
ENV RUBY_DOWNLOAD_SHA256=b5e8a8ed4a47cdd9a3358b5bdd998c37bd9e971ca63766a37d5ae5933fdb69f1
# Thu, 30 May 2024 05:03:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 30 May 2024 05:03:18 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 30 May 2024 05:03:18 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 30 May 2024 05:03:18 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 May 2024 05:03:18 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Thu, 30 May 2024 05:03:18 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:ec3129b1f3b893a7412a0ac12044f811ed32ddf7028d374141819005f9d4699f`  
		Last Modified: Tue, 14 May 2024 00:51:10 GMT  
		Size: 47.3 MB (47338294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c8516852dedc6ef6e011322d36853e449786d3c2d43553864edbb79abbe0ca5`  
		Last Modified: Tue, 14 May 2024 01:21:47 GMT  
		Size: 22.7 MB (22728407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90f71408c4e77f143b3e9d4c1401b7c778766c63dc79d80a05870500825e7c8c`  
		Last Modified: Tue, 14 May 2024 01:22:09 GMT  
		Size: 61.5 MB (61517869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:779bb0cc1f42107df5966cbf82ca7be2fb113ac0edf35633f10fbd5d5cce3ada`  
		Last Modified: Tue, 14 May 2024 01:22:47 GMT  
		Size: 184.5 MB (184522613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28460b1de5cc26916603b21591b29b2b35c97ad046e8172354d4ad893fe51c46`  
		Last Modified: Wed, 29 May 2024 23:13:11 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9f8759d5ae983e9abdc941edd5a4534cea3c16d7056ee539747776faef142c7`  
		Last Modified: Fri, 31 May 2024 00:04:29 GMT  
		Size: 32.9 MB (32856642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01e74d893017b2e377960afc0d4075c7a5c2205d110d45a077a0f974fe896a2c`  
		Last Modified: Fri, 31 May 2024 00:04:27 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:latest` - unknown; unknown

```console
$ docker pull ruby@sha256:8d8bcd7ca1cc8e988940565bbdb75068f7073b2bf5d53920e7689ee06be0033f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15286121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a91bd0bda56a000cbda0151780d90ef0b497ef999bfc9b387cbb4b9f0a7da0a`

```dockerfile
```

-	Layers:
	-	`sha256:7b200689c93b79544a161566076366592cb83e031ba4fdfb4c44119d7b002e15`  
		Last Modified: Fri, 31 May 2024 00:04:28 GMT  
		Size: 15.3 MB (15262651 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6476c2734c369471f75d35fc17000e400b13cc5ae8e8a6ff3c438ac7d0a9126`  
		Last Modified: Fri, 31 May 2024 00:04:27 GMT  
		Size: 23.5 KB (23470 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:latest` - linux; arm variant v7

```console
$ docker pull ruby@sha256:76473628ef0932b442195099f4faff06b67841ee205d98db580f7abc13028568
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.3 MB (334253353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26e68a0b1497894303aff76fb65f160828fc30c7107a096bbdf1f5ff6b2ff295`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 14 May 2024 01:08:35 GMT
ADD file:1e106a38a0e44ca74d4d29c6d797780e7a29ffe249e473c48ee2aea553fc013b in / 
# Tue, 14 May 2024 01:08:36 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:35:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 01:35:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 01:36:53 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 30 May 2024 05:03:18 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Thu, 30 May 2024 05:03:18 GMT
ENV LANG=C.UTF-8
# Thu, 30 May 2024 05:03:18 GMT
ENV RUBY_VERSION=3.3.2
# Thu, 30 May 2024 05:03:18 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.2.tar.xz
# Thu, 30 May 2024 05:03:18 GMT
ENV RUBY_DOWNLOAD_SHA256=b5e8a8ed4a47cdd9a3358b5bdd998c37bd9e971ca63766a37d5ae5933fdb69f1
# Thu, 30 May 2024 05:03:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 30 May 2024 05:03:18 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 30 May 2024 05:03:18 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 30 May 2024 05:03:18 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 May 2024 05:03:18 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Thu, 30 May 2024 05:03:18 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:dfc3b4ca62816a9cbf2bdfbdd78bf692a522e7f48a280492b9f87d55b2f4aa2e`  
		Last Modified: Tue, 14 May 2024 01:12:21 GMT  
		Size: 45.2 MB (45174745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:641d6443415d538c3bf0e0d6ecc0f6b7603b4caf6c79708d0670bc082e9721c5`  
		Last Modified: Tue, 14 May 2024 01:46:47 GMT  
		Size: 22.0 MB (21953893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94dd085f2eef9c35615ce8d6f2e7b6340a6bcadb37fe8fd6698911eab87e371c`  
		Last Modified: Tue, 14 May 2024 01:47:09 GMT  
		Size: 59.2 MB (59217124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb1ddacc8c148925155abdd912bfb78a553326599c4da7b21c01a76f7616a464`  
		Last Modified: Tue, 14 May 2024 01:47:48 GMT  
		Size: 175.2 MB (175175139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea464db56a44988078f222929ba4d9866461099cb11f15d994d11e20e0d654b4`  
		Last Modified: Thu, 30 May 2024 03:37:33 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6795d987a7850e820d5fc3ae49e05e5f9c9a774f6eae38bf9230d1282fe890ec`  
		Last Modified: Fri, 31 May 2024 00:41:53 GMT  
		Size: 32.7 MB (32732111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4182d9b9e70b27624c1e4f8c6b62407fce2794b48fd11f8b1b460ee99f223a20`  
		Last Modified: Fri, 31 May 2024 00:41:52 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:latest` - unknown; unknown

```console
$ docker pull ruby@sha256:16e2ed7af327ccefbcbea91eb364eceac491411ea164be8b3cf4d4ca184c81e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15291594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3c1477c9aeebcbf0ddb64e46f706d83b1c146ef3b3a67d4f8178c50a21fec41`

```dockerfile
```

-	Layers:
	-	`sha256:c29a5eb869227db4e93ec7120ec6932640d10bc811cd38f05cb3bcd898d13bce`  
		Last Modified: Fri, 31 May 2024 00:41:52 GMT  
		Size: 15.3 MB (15268124 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7de38d965d61443f65ab95c61f2d562cf58ee6731e40673bcb2a48f67a7888f6`  
		Last Modified: Fri, 31 May 2024 00:41:52 GMT  
		Size: 23.5 KB (23470 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:latest` - linux; arm64 variant v8

```console
$ docker pull ruby@sha256:43c9d2004d9c99f092ac676ccde80cfe600ecc459d02ad6e51a31cae318b81aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **376.3 MB (376253796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f12d583e97c46f66b5efea35d1cc72972246dd439f4d761e4be42589c9e3610`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 14 May 2024 00:39:32 GMT
ADD file:b7c55dda8ded4219a7cdc9fbd91dfb5996c4886d4394b85751c2f956defe3287 in / 
# Tue, 14 May 2024 00:39:33 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:44:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 01:44:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 01:45:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 30 May 2024 05:03:18 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Thu, 30 May 2024 05:03:18 GMT
ENV LANG=C.UTF-8
# Thu, 30 May 2024 05:03:18 GMT
ENV RUBY_VERSION=3.3.2
# Thu, 30 May 2024 05:03:18 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.2.tar.xz
# Thu, 30 May 2024 05:03:18 GMT
ENV RUBY_DOWNLOAD_SHA256=b5e8a8ed4a47cdd9a3358b5bdd998c37bd9e971ca63766a37d5ae5933fdb69f1
# Thu, 30 May 2024 05:03:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 30 May 2024 05:03:18 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 30 May 2024 05:03:18 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 30 May 2024 05:03:18 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 May 2024 05:03:18 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Thu, 30 May 2024 05:03:18 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:91e301773f03e9e0fabc5c177fe6bfe8daf14e992ab816f151692b814ddc462c`  
		Last Modified: Tue, 14 May 2024 00:42:35 GMT  
		Size: 49.6 MB (49613388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15856ca26414127b85cee6d10acbc4cee6eba9070f3f5a04b9cc72ce95abfa7f`  
		Last Modified: Tue, 14 May 2024 01:52:50 GMT  
		Size: 23.6 MB (23586610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30ed4c12791345d3f20f66024e1f22275ce507868c508509b83dcf231b1c9adc`  
		Last Modified: Tue, 14 May 2024 01:53:09 GMT  
		Size: 64.0 MB (63994370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feb30c5ba2d151512d29ff4b92109a740559509ef6f3072a86c5006a1379397b`  
		Last Modified: Tue, 14 May 2024 01:53:41 GMT  
		Size: 202.6 MB (202593312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:209f61c6c95124a58aac28f46f366148e10076a70df20ea359478476f1cc5771`  
		Last Modified: Fri, 31 May 2024 16:34:32 GMT  
		Size: 199.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68c3814b5573e411d648d9e36caca3d557351ed53100aad4a2711889788c2183`  
		Last Modified: Fri, 31 May 2024 16:34:34 GMT  
		Size: 36.5 MB (36465775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:105e5f925accbffca3afe0617f05a20e8d53d13409d501c82a22ac73891151be`  
		Last Modified: Fri, 31 May 2024 16:34:32 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:latest` - unknown; unknown

```console
$ docker pull ruby@sha256:3ab58e3bfe703951686d3f3f10918b210b134b4520dff6d4d08663c4e95ce5ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15514561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8d6704f130c08bfa286ba56f4161322b6835a1dc924509ace9fa74f53518a0f`

```dockerfile
```

-	Layers:
	-	`sha256:081acbbbd1e92b97a0c69714d95609ed9426039976ef4206f1b9cb318f2252c3`  
		Last Modified: Fri, 31 May 2024 16:34:33 GMT  
		Size: 15.5 MB (15490860 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f0d29c55c6e9414cb2a48dded4cdf0636b60822d88add10c5b5b40c1026b6e6`  
		Last Modified: Fri, 31 May 2024 16:34:32 GMT  
		Size: 23.7 KB (23701 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:latest` - linux; 386

```console
$ docker pull ruby@sha256:7b3a40f533dcc10ce371b36c52b648beba554da6d2cdb00c7d1018977b18e7ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.3 MB (384268006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:503266eeb94c9a1e06344cf8ec3e45c8dc90d78f671b617607aaf7f35ec8400d`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 14 May 2024 00:47:00 GMT
ADD file:35709674a3b845511a896af16ea37a6022e7d48992d3198d0760c0c3208fe4ed in / 
# Tue, 14 May 2024 00:47:01 GMT
CMD ["bash"]
# Tue, 14 May 2024 09:01:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 09:01:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 09:02:47 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 30 May 2024 05:03:18 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Thu, 30 May 2024 05:03:18 GMT
ENV LANG=C.UTF-8
# Thu, 30 May 2024 05:03:18 GMT
ENV RUBY_VERSION=3.3.2
# Thu, 30 May 2024 05:03:18 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.2.tar.xz
# Thu, 30 May 2024 05:03:18 GMT
ENV RUBY_DOWNLOAD_SHA256=b5e8a8ed4a47cdd9a3358b5bdd998c37bd9e971ca63766a37d5ae5933fdb69f1
# Thu, 30 May 2024 05:03:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 30 May 2024 05:03:18 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 30 May 2024 05:03:18 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 30 May 2024 05:03:18 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 May 2024 05:03:18 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Thu, 30 May 2024 05:03:18 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:4f2f2f6205661e555e772749ae7fd294fb04fc0d06cbc67a50a11fbb4ef44242`  
		Last Modified: Tue, 14 May 2024 00:51:31 GMT  
		Size: 50.6 MB (50602424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d849fa81a6965e2bbc8dd9af462f55a46b59aeb701fb0a26992522fd43ce5c03`  
		Last Modified: Tue, 14 May 2024 09:13:04 GMT  
		Size: 24.9 MB (24888551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5d6250e2e75fd4f1cdc533096df2c601817950e8c3f1096f46dfeea2b609cee`  
		Last Modified: Tue, 14 May 2024 09:13:29 GMT  
		Size: 66.0 MB (65988940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54e0a2d5e90c1a7093dbeeaddbb7c833c828015d2e8991c1721c4a269c4faf42`  
		Last Modified: Tue, 14 May 2024 09:14:20 GMT  
		Size: 210.1 MB (210128367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de3ba48d13d75103693be542ec0284b2602b4828d82904262eaebce3ee92c455`  
		Last Modified: Thu, 30 May 2024 23:59:42 GMT  
		Size: 199.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:448e34053f4d770451f62ddaa365d0622ca27c029fc956f19f1d65fc31a4fdde`  
		Last Modified: Thu, 30 May 2024 23:59:43 GMT  
		Size: 32.7 MB (32659382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad5afd28062ac11f31e19b3719baee1f588043578cf6e145e45e045a1c02d469`  
		Last Modified: Thu, 30 May 2024 23:59:42 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:latest` - unknown; unknown

```console
$ docker pull ruby@sha256:160845f774e49594f7666ce16b864ab7e2f4ee52e64834693d7fc8e73a56eab1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15464593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed3ffc3a71bab9ed08fee6a13a78e2124a5bb465330b9003ae30c6c121644392`

```dockerfile
```

-	Layers:
	-	`sha256:0af6a7fbbb7418ad0af9bdc7b92c3eadbb1f04a67ea464fc769866e936047fbb`  
		Last Modified: Thu, 30 May 2024 23:59:42 GMT  
		Size: 15.4 MB (15441304 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9763aac85d6581748e54f3e02609a6c4b38cd9afb48a645228304112ae42c01c`  
		Last Modified: Thu, 30 May 2024 23:59:42 GMT  
		Size: 23.3 KB (23289 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:latest` - linux; mips64le

```console
$ docker pull ruby@sha256:1846a3e9289314a04f182cd9dad0f80187bd50c10574ec9106650e0cb9a9159a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.6 MB (359631625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f58811f8ed8139f13a9aeb686c55d67ef8bd82c87a47f73d1c36ab1d025c428c`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 14 May 2024 01:10:23 GMT
ADD file:95717416297a85e0b38d171b3bf8d2b48e941bd725e476ee4f88033fed4ffee2 in / 
# Tue, 14 May 2024 01:10:29 GMT
CMD ["bash"]
# Tue, 14 May 2024 10:59:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 11:01:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 11:07:30 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 30 May 2024 05:03:18 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Thu, 30 May 2024 05:03:18 GMT
ENV LANG=C.UTF-8
# Thu, 30 May 2024 05:03:18 GMT
ENV RUBY_VERSION=3.3.2
# Thu, 30 May 2024 05:03:18 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.2.tar.xz
# Thu, 30 May 2024 05:03:18 GMT
ENV RUBY_DOWNLOAD_SHA256=b5e8a8ed4a47cdd9a3358b5bdd998c37bd9e971ca63766a37d5ae5933fdb69f1
# Thu, 30 May 2024 05:03:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 30 May 2024 05:03:18 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 30 May 2024 05:03:18 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 30 May 2024 05:03:18 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 May 2024 05:03:18 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Thu, 30 May 2024 05:03:18 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:0fd7e383bbed45ca14b36b1e22f1591a0b2bddc34b2b6e2b34d4cd54b528e75f`  
		Last Modified: Tue, 14 May 2024 01:21:36 GMT  
		Size: 49.6 MB (49582338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5ce1d8a69726b5d3330ae01a246efbb18fb60d54fb0d08b741a960e37d8b115`  
		Last Modified: Tue, 14 May 2024 11:37:05 GMT  
		Size: 23.4 MB (23438164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e3667485c8dcf18ff23740eff9103874ec0aba9a4d45bade2f98f9f85fe0f63`  
		Last Modified: Tue, 14 May 2024 11:37:57 GMT  
		Size: 63.0 MB (62968511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb3514ef59a25de65d0663fc4a360de7a712214c493290dd77858247edbd0dac`  
		Last Modified: Tue, 14 May 2024 11:40:05 GMT  
		Size: 189.8 MB (189771182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7210d7f5f868d0b86d1d7732255e8b50eff8544dba9ab1860171be554ba6851c`  
		Last Modified: Fri, 31 May 2024 02:12:57 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3d202d8b1fd26a6a3352b15c72a19c1ec62d05abee4b24d3614bde5bb38804b`  
		Last Modified: Fri, 31 May 2024 02:13:10 GMT  
		Size: 33.9 MB (33871089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6ebd272f43297a4a9c8254b39c23c0dd0f78f69f987c82a051ec8be32b73a12`  
		Last Modified: Fri, 31 May 2024 02:12:58 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:latest` - unknown; unknown

```console
$ docker pull ruby@sha256:6b9f242c0addc1b162447fc156512149193eff9ad5fee9a13e4a805db49ee67d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.2 KB (23222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94ac948388b799dd3312b530d9764cf8d9345939ed3a333de6065d533b314da6`

```dockerfile
```

-	Layers:
	-	`sha256:7912568d1bf9e1e2a9b2d0f7160459a0c331615db07b1625351290d8f419ed80`  
		Last Modified: Fri, 31 May 2024 02:12:57 GMT  
		Size: 23.2 KB (23222 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:latest` - linux; ppc64le

```console
$ docker pull ruby@sha256:367775d7154d42879fad0d6164afb5e2f9b09817be0433cdc9dfd20b2c7edc48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **397.3 MB (397349127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29c1c5b3d49d1a015327fd3773981bf8a9ca024cd33b41759ccb8a5eeeaab9d1`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 14 May 2024 01:19:48 GMT
ADD file:fdb5c89e2970bd3b21a7b4e39491c1719b957f54babefd52ad455ea72a77bd3f in / 
# Tue, 14 May 2024 01:19:50 GMT
CMD ["bash"]
# Tue, 14 May 2024 06:55:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 06:55:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 06:57:32 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 30 May 2024 05:03:18 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Thu, 30 May 2024 05:03:18 GMT
ENV LANG=C.UTF-8
# Thu, 30 May 2024 05:03:18 GMT
ENV RUBY_VERSION=3.3.2
# Thu, 30 May 2024 05:03:18 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.2.tar.xz
# Thu, 30 May 2024 05:03:18 GMT
ENV RUBY_DOWNLOAD_SHA256=b5e8a8ed4a47cdd9a3358b5bdd998c37bd9e971ca63766a37d5ae5933fdb69f1
# Thu, 30 May 2024 05:03:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 30 May 2024 05:03:18 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 30 May 2024 05:03:18 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 30 May 2024 05:03:18 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 May 2024 05:03:18 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Thu, 30 May 2024 05:03:18 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:9027b64136d8b1ece1ad24cca3199e496689a33f47b8d112dbdd112c682e665f`  
		Last Modified: Tue, 14 May 2024 01:23:40 GMT  
		Size: 53.6 MB (53579748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18e147daa0a988c77940b565d177a661a73270a0e821c65283b9e531ae38ebc4`  
		Last Modified: Tue, 14 May 2024 07:10:25 GMT  
		Size: 25.7 MB (25699676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b88d9ff0405bb000dedfa15a3a34739370c3daa10367599bff02a57fd19a3564`  
		Last Modified: Tue, 14 May 2024 07:10:47 GMT  
		Size: 69.6 MB (69584088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b80be54620660eb7b908f8c79a7ad14bedcac29ae46f620f4ede820441dc65d`  
		Last Modified: Tue, 14 May 2024 07:11:29 GMT  
		Size: 214.2 MB (214234653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40cb77ee6ba0b5f0c4ecfe2b04d71b00d9dbc72410a931ada6d8ecd22c23503b`  
		Last Modified: Thu, 30 May 2024 03:20:27 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:117b815bdc1c3fdd717b19096dfe346acc561bbef54c3d8ce1d5c6c34779864b`  
		Last Modified: Fri, 31 May 2024 01:41:50 GMT  
		Size: 34.3 MB (34250623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16d616fe491d20367467d83b3a720139cf77fe862008d920b8ec08f5d1ee1aa1`  
		Last Modified: Fri, 31 May 2024 01:41:48 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:latest` - unknown; unknown

```console
$ docker pull ruby@sha256:38a74315f2d622e49b3cf13c68b84d9677193c253ba8330df0657228a2867530
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15462362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bdccde7c903eb1771caf3167f3c586e6358dabb30b6223ec18517575b702a0e`

```dockerfile
```

-	Layers:
	-	`sha256:83b3878e8592dc681908ab87b7fdb901612485710d2f4c060ab858e0b78144e5`  
		Last Modified: Fri, 31 May 2024 01:41:49 GMT  
		Size: 15.4 MB (15438954 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50cf5ac37a8b0fd4d0f46ebb5c590cd96a3947fb653f52b885a59d66e3b479b4`  
		Last Modified: Fri, 31 May 2024 01:41:48 GMT  
		Size: 23.4 KB (23408 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:latest` - linux; s390x

```console
$ docker pull ruby@sha256:cbd156fbfe825d22cf87ca40dbae2fbcc389604eb849dfdaf1284a935f570c7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.9 MB (351858563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8adefd70c895ce3ff49d4fbb9f97965427484e458696e2ba0e85de5f5b372bf7`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 14 May 2024 00:42:19 GMT
ADD file:d24c16f113416f94273813df324360fe934245f0f7f2973b6def2799e5605f1f in / 
# Tue, 14 May 2024 00:42:21 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:19:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 01:20:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 01:21:16 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 30 May 2024 05:03:18 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Thu, 30 May 2024 05:03:18 GMT
ENV LANG=C.UTF-8
# Thu, 30 May 2024 05:03:18 GMT
ENV RUBY_VERSION=3.3.2
# Thu, 30 May 2024 05:03:18 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.2.tar.xz
# Thu, 30 May 2024 05:03:18 GMT
ENV RUBY_DOWNLOAD_SHA256=b5e8a8ed4a47cdd9a3358b5bdd998c37bd9e971ca63766a37d5ae5933fdb69f1
# Thu, 30 May 2024 05:03:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 30 May 2024 05:03:18 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 30 May 2024 05:03:18 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 30 May 2024 05:03:18 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 May 2024 05:03:18 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Thu, 30 May 2024 05:03:18 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:b9285660d64168cd1c05bdfee5186da3634a289a06300d8ea12e57df80e4648b`  
		Last Modified: Tue, 14 May 2024 00:47:17 GMT  
		Size: 47.9 MB (47942190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c304d55d9ae47fcef54a6044634995ffbdbd5e4d3e409198127615b4043fa8b`  
		Last Modified: Tue, 14 May 2024 01:29:23 GMT  
		Size: 24.0 MB (24046857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:943219d44d0b66fa3c53413ccd4b689951925725722eba1e47eec984778d3640`  
		Last Modified: Tue, 14 May 2024 01:29:39 GMT  
		Size: 63.1 MB (63130182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57dd19c695c401ade3f0a1af6a11007c474b68b17b925095492dbfc5a8f2a538`  
		Last Modified: Tue, 14 May 2024 01:30:07 GMT  
		Size: 183.2 MB (183236787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ead26fdd125c6435c78734df6dc35063c1bb6bde6fdcd465ea3f4c8ba2d27eaf`  
		Last Modified: Thu, 30 May 2024 01:36:07 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3887303fb32e8045ba11c21195de82b07f96bdae907eb33613398054fd6fb09`  
		Last Modified: Fri, 31 May 2024 00:49:41 GMT  
		Size: 33.5 MB (33502206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a268db3ee5ab81939da4015efe100b94f0e39472fd5d5a4bf34f631237bc6e2`  
		Last Modified: Fri, 31 May 2024 00:49:40 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:latest` - unknown; unknown

```console
$ docker pull ruby@sha256:651a37fb5c91de5bf16bce85a5c366d1bb1885adbd0d08ac93234cb190f26e70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15300280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b254a8a1910470d0f05ca2c799cc646d6500abf8a97cf0e6723a623baaecf7b1`

```dockerfile
```

-	Layers:
	-	`sha256:876e1a826ce31d2f9567efb15a7fedec47fa9ad7e5f51e2e26ed896f59a61c7a`  
		Last Modified: Fri, 31 May 2024 00:49:41 GMT  
		Size: 15.3 MB (15276938 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d01303463e21cc2214db0c668492394b0372fc4803e6e33a654237eaf77cd876`  
		Last Modified: Fri, 31 May 2024 00:49:41 GMT  
		Size: 23.3 KB (23342 bytes)  
		MIME: application/vnd.in-toto+json
