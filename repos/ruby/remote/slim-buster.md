## `ruby:slim-buster`

```console
$ docker pull ruby@sha256:12be3973e46af94795c0c4304c4f5e4f41bf589a9ca892d2e09c997a08a0b684
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `ruby:slim-buster` - linux; amd64

```console
$ docker pull ruby@sha256:dadb99921e4d6f95322bb74ea9988ab4b8cbade0ca3195c0ee84a9e5026245e5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.9 MB (70884402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5247bd27595c29bd13c99b72d49d6f06ffee77fc2d12c841ea01788ecd268614`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 11 Jan 2023 02:35:07 GMT
ADD file:67ceb946e54c26c505b5f9f393d77befbd5e9b3b5c069ca301e314ecc74456b0 in / 
# Wed, 11 Jan 2023 02:35:07 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 09:40:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 09:40:42 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 11 Jan 2023 09:40:42 GMT
ENV LANG=C.UTF-8
# Wed, 11 Jan 2023 09:40:42 GMT
ENV RUBY_MAJOR=3.2
# Wed, 11 Jan 2023 09:40:42 GMT
ENV RUBY_VERSION=3.2.0
# Wed, 11 Jan 2023 09:40:42 GMT
ENV RUBY_DOWNLOAD_SHA256=d2f4577306e6dd932259693233141e5c3ec13622c95b75996541b8d5b68b28b4
# Wed, 11 Jan 2023 09:43:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 11 Jan 2023 09:43:15 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 11 Jan 2023 09:43:15 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 11 Jan 2023 09:43:16 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Jan 2023 09:43:16 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 11 Jan 2023 09:43:16 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:548fcab5fe888f589dd092c68b813bfd65359878bd1950d6b753f749e82ebd7c`  
		Last Modified: Wed, 11 Jan 2023 02:39:48 GMT  
		Size: 27.1 MB (27140352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fd0e234eb1adfea452a0d649e361aaa03cadf63c532b7124ae83f6db64d3823`  
		Last Modified: Wed, 11 Jan 2023 10:12:42 GMT  
		Size: 12.6 MB (12577230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cf1a224abf2fff0ae7c97213301969fd671f19d4d42c2896a839d8057308682`  
		Last Modified: Wed, 11 Jan 2023 10:12:39 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92ea0d6209805d2c7a18e9203db8310d28267f55ad73a5a91e5f2f24bfa6e749`  
		Last Modified: Wed, 11 Jan 2023 10:12:43 GMT  
		Size: 31.2 MB (31166445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7acb5e909633dbd0a0afa15c1a0d4b6b1da02dced77ab62f669b57d9d4b5c0b`  
		Last Modified: Wed, 11 Jan 2023 10:12:39 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:slim-buster` - linux; arm variant v7

```console
$ docker pull ruby@sha256:c2275d5e2fe8aaad3b43ab0a678157aeb2a54afb5ae00f5a99ef9033db4ab031
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.8 MB (62752431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4756e7033a96fe157f2366293cc928e780e1402c6690b3b89ca7dae71f88547b`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 21 Dec 2022 01:58:52 GMT
ADD file:4f66da36432e21f879e146a8c03acd32dcf70e420621fea284314700458fb6a3 in / 
# Wed, 21 Dec 2022 01:58:52 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 16:07:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 16:07:46 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 21 Dec 2022 16:07:46 GMT
ENV LANG=C.UTF-8
# Tue, 27 Dec 2022 18:28:05 GMT
ENV RUBY_MAJOR=3.2
# Tue, 27 Dec 2022 18:28:05 GMT
ENV RUBY_VERSION=3.2.0
# Tue, 27 Dec 2022 18:28:05 GMT
ENV RUBY_DOWNLOAD_SHA256=d2f4577306e6dd932259693233141e5c3ec13622c95b75996541b8d5b68b28b4
# Tue, 27 Dec 2022 18:30:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 27 Dec 2022 18:30:19 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 27 Dec 2022 18:30:19 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 27 Dec 2022 18:30:19 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 Dec 2022 18:30:20 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 27 Dec 2022 18:30:20 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:0bfa76d00e8a959cfee85f6be4f8577bd6e02735facad069e2f7896fe4e472f3`  
		Last Modified: Wed, 21 Dec 2022 02:06:02 GMT  
		Size: 22.7 MB (22748857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a52f4a66875328245719834fc90379f4d89d219789cdb2129a12c0550299d5c`  
		Last Modified: Wed, 21 Dec 2022 16:40:51 GMT  
		Size: 9.9 MB (9876943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6099e18e3ee097d28dc5dbe47ac8e40f3209314408c198e4547858fb1ce42f8`  
		Last Modified: Wed, 21 Dec 2022 16:40:48 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2c06e34c1947f389f9c15b4dc64fd6cda7aae4e586c663b338628d14c93b92f`  
		Last Modified: Tue, 27 Dec 2022 18:42:22 GMT  
		Size: 30.1 MB (30126287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba6c76fd0d39438e35d404b52c29593b83a9ad67e6af71eb0e13039592dc3e53`  
		Last Modified: Tue, 27 Dec 2022 18:42:18 GMT  
		Size: 144.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:slim-buster` - linux; arm64 variant v8

```console
$ docker pull ruby@sha256:4bae4dc61f28308722317809f63ebca518184bd604a68b4737f7f91d31db22d9
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.2 MB (68175732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d9f38f2298715c8c7c0e11fbf1399cc3917eeffe5d503167a753538405c1055`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 11 Jan 2023 02:57:52 GMT
ADD file:08addf73dde8bf5ac64e0d9bdd1997ce5f406976c19da431616783c14fdb36ac in / 
# Wed, 11 Jan 2023 02:57:52 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 14:08:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 14:08:43 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 11 Jan 2023 14:08:43 GMT
ENV LANG=C.UTF-8
# Wed, 11 Jan 2023 14:08:43 GMT
ENV RUBY_MAJOR=3.2
# Wed, 11 Jan 2023 14:08:43 GMT
ENV RUBY_VERSION=3.2.0
# Wed, 11 Jan 2023 14:08:43 GMT
ENV RUBY_DOWNLOAD_SHA256=d2f4577306e6dd932259693233141e5c3ec13622c95b75996541b8d5b68b28b4
# Wed, 11 Jan 2023 14:10:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 11 Jan 2023 14:10:31 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 11 Jan 2023 14:10:31 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 11 Jan 2023 14:10:31 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Jan 2023 14:10:32 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 11 Jan 2023 14:10:32 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:7fac02f4cd2bcf681b9e156a67009cf4609f45447818b52327d93553bfeb2965`  
		Last Modified: Wed, 11 Jan 2023 03:01:58 GMT  
		Size: 25.9 MB (25914925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b14447d9072809caa4a5a10047a9062a81f7a2d33695ca8de86de436046cbb04`  
		Last Modified: Wed, 11 Jan 2023 14:33:12 GMT  
		Size: 11.3 MB (11281731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e71c0b06ae40e96120abb750e32d448b691c107ea74ac826dd42f16b75a07c0f`  
		Last Modified: Wed, 11 Jan 2023 14:33:11 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f581eb3a0830ab3c8c86449039a59618a33ad2330620dd2224acbb6a830811f`  
		Last Modified: Wed, 11 Jan 2023 14:33:13 GMT  
		Size: 31.0 MB (30978703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:573e2efacad55cfcfee0bd3481c02c90762ccdc9a1a73e12440cb89562bb9bea`  
		Last Modified: Wed, 11 Jan 2023 14:33:11 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:slim-buster` - linux; 386

```console
$ docker pull ruby@sha256:343d0daa1cc03ce4c2b0287882fade8f7518c90ee7387f68fe676b08a4ed8b9d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.2 MB (75232586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7220b91e2adb51253171fbe0af869bd9c45e73463b7b2e0fd1c4a99ff1b2ccff`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 21 Dec 2022 01:39:45 GMT
ADD file:48a2a0e6cb166df412bb4f6ad30537c66bc6be97ce4c8fc582fd5ac8c6129b5a in / 
# Wed, 21 Dec 2022 01:39:46 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 06:46:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 06:46:40 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 21 Dec 2022 06:46:41 GMT
ENV LANG=C.UTF-8
# Tue, 27 Dec 2022 18:00:15 GMT
ENV RUBY_MAJOR=3.2
# Tue, 27 Dec 2022 18:00:16 GMT
ENV RUBY_VERSION=3.2.0
# Tue, 27 Dec 2022 18:00:17 GMT
ENV RUBY_DOWNLOAD_SHA256=d2f4577306e6dd932259693233141e5c3ec13622c95b75996541b8d5b68b28b4
# Tue, 27 Dec 2022 18:02:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 27 Dec 2022 18:02:33 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 27 Dec 2022 18:02:33 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 27 Dec 2022 18:02:34 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 Dec 2022 18:02:35 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 27 Dec 2022 18:02:36 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:9099d8a02dc0a7901931d2811fa3078b18ecd3a40a156cbcfd91629126463f80`  
		Last Modified: Wed, 21 Dec 2022 01:45:34 GMT  
		Size: 27.8 MB (27798412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08d81f06faaaa5c3748d9a1bc50ee0d30fd8158ba214b2670ffa0f44a7464618`  
		Last Modified: Wed, 21 Dec 2022 07:07:09 GMT  
		Size: 17.2 MB (17238286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9f1cfcc30ecb2465e850f75f09d4547488a1e5a190387b2b01ce1939c594f89`  
		Last Modified: Wed, 21 Dec 2022 07:07:06 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb3d746778a1ea49a98e82a55d1a92a77d9c808106fa09532ecf88c2c221c88c`  
		Last Modified: Tue, 27 Dec 2022 18:13:26 GMT  
		Size: 30.2 MB (30195542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7313697220039b7c86ddfcdc544f9716e1e806577b7358be00cfd2825262d7d3`  
		Last Modified: Tue, 27 Dec 2022 18:13:22 GMT  
		Size: 145.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
