## `ruby:3-slim-buster`

```console
$ docker pull ruby@sha256:7d1f46822fcf4b47269d5421897ff835e5df8143946e24c37030d9de83fc332c
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

### `ruby:3-slim-buster` - linux; amd64

```console
$ docker pull ruby@sha256:432b2412f71bd9d039d39e9506d36cbdb8d6af28966cc45efb1143fa3c0e04dd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.8 MB (71827179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fca20aa12e64df2768bc077dfac7bace109e1e14ad591c9cf1c9b7d0f342e696`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 11 May 2022 01:20:37 GMT
ADD file:76b454ddb7dfe4d22afae844a7e67e7e5fb4570dae2e21bbd259a1f2e5839f33 in / 
# Wed, 11 May 2022 01:20:37 GMT
CMD ["bash"]
# Wed, 11 May 2022 15:33:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 15:33:21 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 11 May 2022 15:33:21 GMT
ENV LANG=C.UTF-8
# Wed, 11 May 2022 15:42:48 GMT
ENV RUBY_MAJOR=3.1
# Wed, 11 May 2022 15:42:48 GMT
ENV RUBY_VERSION=3.1.2
# Wed, 11 May 2022 15:42:48 GMT
ENV RUBY_DOWNLOAD_SHA256=ca10d017f8a1b6d247556622c841fc56b90c03b1803f87198da1e4fd3ec3bf2a
# Wed, 11 May 2022 15:45:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 11 May 2022 15:45:05 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 11 May 2022 15:45:05 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 11 May 2022 15:45:06 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 May 2022 15:45:06 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 11 May 2022 15:45:06 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:c32ce6654453d35d0b3dde45d195adeee586ffba0a683006ee06748c077c01fa`  
		Last Modified: Wed, 11 May 2022 01:25:58 GMT  
		Size: 27.1 MB (27140722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e6f8fac6772b28552ed711412fe28cae33542d35b15cadf55deb7883534dba8`  
		Last Modified: Wed, 11 May 2022 16:03:49 GMT  
		Size: 12.6 MB (12575281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d49973b700271d0dba13eba8390cbb6e75dfa08e75851d9ddc5ba9e67df71722`  
		Last Modified: Wed, 11 May 2022 16:03:47 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8915d27db11080b213c8ba36a73ff5b60ee85a28ec2f4de6afbb5621f8d47c56`  
		Last Modified: Wed, 11 May 2022 16:05:21 GMT  
		Size: 32.1 MB (32110802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59e11a64aadb955102357078c3dd1a0202cabb98f6e63ddbe4b15a15b01ae153`  
		Last Modified: Wed, 11 May 2022 16:05:18 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:3-slim-buster` - linux; arm variant v5

```console
$ docker pull ruby@sha256:d00c1a47b4d9df83ec059df995e921ee9b37baf558d94db9a55347a7991a2648
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.0 MB (65987494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc0c54e13ee60c9a28718b30c4007118ade70e1e2cee587db758f30cbcd877fa`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 11 May 2022 00:51:34 GMT
ADD file:c4087f224dff43064778eac76e711d30ca4882a1d3b571b1cd509089166abc0d in / 
# Wed, 11 May 2022 00:51:35 GMT
CMD ["bash"]
# Thu, 12 May 2022 00:17:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 12 May 2022 00:18:01 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 12 May 2022 00:18:01 GMT
ENV LANG=C.UTF-8
# Thu, 12 May 2022 00:38:50 GMT
ENV RUBY_MAJOR=3.1
# Thu, 12 May 2022 00:38:50 GMT
ENV RUBY_VERSION=3.1.2
# Thu, 12 May 2022 00:38:51 GMT
ENV RUBY_DOWNLOAD_SHA256=ca10d017f8a1b6d247556622c841fc56b90c03b1803f87198da1e4fd3ec3bf2a
# Thu, 12 May 2022 00:44:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 12 May 2022 00:44:04 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 12 May 2022 00:44:04 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 12 May 2022 00:44:05 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 12 May 2022 00:44:06 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 12 May 2022 00:44:07 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:69d6138017be389335ab570ff643096d0ea914f563d41f238e7ff3520fe8e93f`  
		Last Modified: Wed, 11 May 2022 01:07:20 GMT  
		Size: 24.9 MB (24889917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d2eaddc39ae0bfed160472592ee05f61563f42d805f79d3585b2dd247fd9d8b`  
		Last Modified: Thu, 12 May 2022 01:28:02 GMT  
		Size: 10.4 MB (10355804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ceea86702a9c6180675c1a666852d40e5c1f112281b7f434539d92691cdbf309`  
		Last Modified: Thu, 12 May 2022 01:27:55 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:476393bdd0cf875b897c3d8f42bb528a7e4cd8a3c94eb24d8ceb7300443d226e`  
		Last Modified: Thu, 12 May 2022 01:30:48 GMT  
		Size: 30.7 MB (30741398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:683f8535baef228bc105f2e5a631840504fcb531e0bc0374cab158242e20a4e9`  
		Last Modified: Thu, 12 May 2022 01:30:34 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:3-slim-buster` - linux; arm variant v7

```console
$ docker pull ruby@sha256:647736c655e81284a5ab15563b3ef4b565020fc786b06958fb54739b61d8b857
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.2 MB (63241140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7d51b6a242930d89e2cb5deb30a3a0a710d9cfe4cb2c1fbcd75bc5d5b73e5f9`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 11 May 2022 01:50:13 GMT
ADD file:bccd1898e72cc79621c20ba59061d318521fbd2a8f10806cc3a1561fcbc9daad in / 
# Wed, 11 May 2022 01:50:14 GMT
CMD ["bash"]
# Thu, 12 May 2022 08:21:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 12 May 2022 08:21:57 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 12 May 2022 08:21:57 GMT
ENV LANG=C.UTF-8
# Thu, 12 May 2022 08:42:08 GMT
ENV RUBY_MAJOR=3.1
# Thu, 12 May 2022 08:42:08 GMT
ENV RUBY_VERSION=3.1.2
# Thu, 12 May 2022 08:42:09 GMT
ENV RUBY_DOWNLOAD_SHA256=ca10d017f8a1b6d247556622c841fc56b90c03b1803f87198da1e4fd3ec3bf2a
# Thu, 12 May 2022 08:47:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 12 May 2022 08:47:08 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 12 May 2022 08:47:09 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 12 May 2022 08:47:09 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 12 May 2022 08:47:11 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 12 May 2022 08:47:11 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:8f4c08df22a944142862818447616fff8b15d3a7ba383d4eeab678af698c2c43`  
		Last Modified: Wed, 11 May 2022 02:06:00 GMT  
		Size: 22.7 MB (22747864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d21b333448558a5b1e9fd5897078cfbe48198f593ae0d863033ad2b25e4fee2c`  
		Last Modified: Thu, 12 May 2022 09:32:35 GMT  
		Size: 9.9 MB (9874574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8219d78234f37278f14f270ba3db6c85deb9166cd58bf6eabdbbaf38823781d`  
		Last Modified: Thu, 12 May 2022 09:32:27 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bb3a30da0045371f13085d8231e03aa21e7f347b3f635f1b959197d9fd202db`  
		Last Modified: Thu, 12 May 2022 09:35:26 GMT  
		Size: 30.6 MB (30618326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56d76c4182b7112621bf58b40e4fc9d762b5129f3ef047e0ea961f007c2daa87`  
		Last Modified: Thu, 12 May 2022 09:35:12 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:3-slim-buster` - linux; arm64 variant v8

```console
$ docker pull ruby@sha256:b84a57ef40ea471ddcae23e23cb3f384a0830fc2f215ef13e81579bb826c47ce
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.5 MB (68543100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79c4627c0e1553589d1a38ad7fd96d73e961ac20500dbc53201847b580ab74a1`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 11 May 2022 00:47:26 GMT
ADD file:2536146c773d09db1a8fbbff00933acc459d8929feb3cff5b93ca4c23b577845 in / 
# Wed, 11 May 2022 00:47:26 GMT
CMD ["bash"]
# Wed, 11 May 2022 14:56:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 14:56:40 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 11 May 2022 14:56:41 GMT
ENV LANG=C.UTF-8
# Wed, 11 May 2022 15:06:15 GMT
ENV RUBY_MAJOR=3.1
# Wed, 11 May 2022 15:06:15 GMT
ENV RUBY_VERSION=3.1.2
# Wed, 11 May 2022 15:06:16 GMT
ENV RUBY_DOWNLOAD_SHA256=ca10d017f8a1b6d247556622c841fc56b90c03b1803f87198da1e4fd3ec3bf2a
# Wed, 11 May 2022 15:08:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 11 May 2022 15:08:21 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 11 May 2022 15:08:22 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 11 May 2022 15:08:23 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 May 2022 15:08:24 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 11 May 2022 15:08:25 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:383d573fdcf2c6da56fdb61e120549d7bc200471208ca4c7c6605c57a0a87ef6`  
		Last Modified: Wed, 11 May 2022 00:54:36 GMT  
		Size: 25.9 MB (25909014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ba40eb33383dcb8fbca892a5bb4c3ddd3ea1a1f0fc4b2e0a9358608ff79240d`  
		Last Modified: Wed, 11 May 2022 15:29:12 GMT  
		Size: 11.3 MB (11274469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f4c7c74f65d52871c2e50fd4807615762b23172389c4be3fd6020e6da6fb454`  
		Last Modified: Wed, 11 May 2022 15:29:10 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:201521f0934c8ab36b027fe0722e936de88e229d216d0cedf23e1aae541a4054`  
		Last Modified: Wed, 11 May 2022 15:30:59 GMT  
		Size: 31.4 MB (31359277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4574068606a28e75b171371226fc8d81148611639ec7361823fbb9f616ae59a1`  
		Last Modified: Wed, 11 May 2022 15:30:55 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:3-slim-buster` - linux; 386

```console
$ docker pull ruby@sha256:5ab3255e999a54a919682ee3d8041a8acaaeb8e522c32ea5bc2e0e172adbbfeb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.8 MB (75776973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f85608b5a84dc70d572007214b10a6f7fb8db85971296ced99bcfd23b5115d27`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 11 May 2022 01:39:41 GMT
ADD file:fc7b00a8a5b0e703ac3ede5e2e51257f5ee709fcd35fee53e7b99d144cd873e4 in / 
# Wed, 11 May 2022 01:39:42 GMT
CMD ["bash"]
# Wed, 11 May 2022 15:06:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 15:06:09 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 11 May 2022 15:06:10 GMT
ENV LANG=C.UTF-8
# Wed, 11 May 2022 15:15:44 GMT
ENV RUBY_MAJOR=3.1
# Wed, 11 May 2022 15:15:44 GMT
ENV RUBY_VERSION=3.1.2
# Wed, 11 May 2022 15:15:45 GMT
ENV RUBY_DOWNLOAD_SHA256=ca10d017f8a1b6d247556622c841fc56b90c03b1803f87198da1e4fd3ec3bf2a
# Wed, 11 May 2022 15:17:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 11 May 2022 15:17:55 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 11 May 2022 15:17:56 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 11 May 2022 15:17:57 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 May 2022 15:17:58 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 11 May 2022 15:17:59 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:b1c376c64b69c16b8b035dfd04b99bb7769a5afdfb56a1241aa4ec8743e85aa7`  
		Last Modified: Wed, 11 May 2022 01:47:22 GMT  
		Size: 27.8 MB (27799149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:436b902314c6546fcb24a21f443bc08cf9f9f84f2bb28575ee17b8a717ab41fc`  
		Last Modified: Wed, 11 May 2022 15:39:18 GMT  
		Size: 17.2 MB (17232855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6be672d2b6a20b85ed2175f87e6e61c02a75c81e93727cb4c48c30d9bc036e4e`  
		Last Modified: Wed, 11 May 2022 15:39:14 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3b9d86ecbb25723a1a77557a59c9d3e66bc75167f81a56dcc85b0cfaff98d73`  
		Last Modified: Wed, 11 May 2022 15:41:09 GMT  
		Size: 30.7 MB (30744630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ab386fd45d0ae35aabf32bbc13b464d0f71f6a149dc02d47e2a659742bec888`  
		Last Modified: Wed, 11 May 2022 15:41:04 GMT  
		Size: 141.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:3-slim-buster` - linux; mips64le

```console
$ docker pull ruby@sha256:3ba0650125668d034792d1348b75fb572464ce0bd296bb486146f9d9aac4d9f2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.3 MB (69329999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae8a42154a274cb8251d3990396a5f94e1a6df1d4d1b38bee6f37db539477708`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 20 Apr 2022 14:29:43 GMT
ADD file:f2e428bca7429567876f4893eec93f98aea1a0ee0849fd6bf280981d6694f64f in / 
# Wed, 20 Apr 2022 14:29:46 GMT
CMD ["bash"]
# Thu, 21 Apr 2022 14:42:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 21 Apr 2022 14:42:25 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 21 Apr 2022 14:42:28 GMT
ENV LANG=C.UTF-8
# Thu, 21 Apr 2022 15:31:53 GMT
ENV RUBY_MAJOR=3.1
# Thu, 21 Apr 2022 15:31:56 GMT
ENV RUBY_VERSION=3.1.2
# Thu, 21 Apr 2022 15:31:58 GMT
ENV RUBY_DOWNLOAD_SHA256=ca10d017f8a1b6d247556622c841fc56b90c03b1803f87198da1e4fd3ec3bf2a
# Thu, 21 Apr 2022 15:44:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 21 Apr 2022 15:44:14 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 21 Apr 2022 15:44:17 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 21 Apr 2022 15:44:20 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 21 Apr 2022 15:44:27 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 21 Apr 2022 15:44:30 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:25982b91f9e34cb3f19df99420412fa9ac9e10dbe2916296c21fedef3d255b2d`  
		Last Modified: Wed, 20 Apr 2022 14:40:38 GMT  
		Size: 25.8 MB (25814321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f36388a1ad056d54c040d86048858788baaecae60d6cea066c022fd67dbd7a30`  
		Last Modified: Thu, 21 Apr 2022 17:51:28 GMT  
		Size: 11.6 MB (11635131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4da20569991f31ac34752b6bd1b156a991e2303e5029850dfba3ba7508fab52`  
		Last Modified: Thu, 21 Apr 2022 17:51:17 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d95c61d0b2330c08728c7ec7fa6636af8f083287ef046282a500c12b81ea7e3`  
		Last Modified: Thu, 21 Apr 2022 17:53:44 GMT  
		Size: 31.9 MB (31880205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b43f58239f5d36eaac3ebaf74708232699a5b83e45b43f6477ca076ac135b05`  
		Last Modified: Thu, 21 Apr 2022 17:53:30 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:3-slim-buster` - linux; ppc64le

```console
$ docker pull ruby@sha256:cea5e7023279860a1acd27a754e3ea89c2cd63810c4fb9a6e980996884d495e2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.6 MB (75571038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c4317470086018a3ee510ba348ba7179faa77d294f1f2aac91d00e9d1137df1`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 11 May 2022 01:33:31 GMT
ADD file:57fcc3eadd20c2481e373ef3b56a194006f65b3c7ae29bd1747e625efcd89124 in / 
# Wed, 11 May 2022 01:33:37 GMT
CMD ["bash"]
# Thu, 12 May 2022 05:15:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 12 May 2022 05:15:19 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 12 May 2022 05:15:22 GMT
ENV LANG=C.UTF-8
# Thu, 12 May 2022 05:42:06 GMT
ENV RUBY_MAJOR=3.1
# Thu, 12 May 2022 05:42:08 GMT
ENV RUBY_VERSION=3.1.2
# Thu, 12 May 2022 05:42:10 GMT
ENV RUBY_DOWNLOAD_SHA256=ca10d017f8a1b6d247556622c841fc56b90c03b1803f87198da1e4fd3ec3bf2a
# Thu, 12 May 2022 05:51:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 12 May 2022 05:51:31 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 12 May 2022 05:51:36 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 12 May 2022 05:51:41 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 12 May 2022 05:51:49 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 12 May 2022 05:51:52 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:97c4e3bbd0d14c4a194ce9c48b362e1649c341b249c2ad560738b06fe8576dc3`  
		Last Modified: Wed, 11 May 2022 01:44:06 GMT  
		Size: 30.6 MB (30560544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:199aa8dcafd23b84d89b4737f31fbacb6ddf979495ce14ae309fe454fe782c76`  
		Last Modified: Thu, 12 May 2022 06:44:17 GMT  
		Size: 12.7 MB (12722178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdecccd5b88614ec7ed51b36e7f590e3c9d979881e524932f8282f44efe6f55d`  
		Last Modified: Thu, 12 May 2022 06:44:13 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcace5b74c02f1a784245301d4cbaab5c5a467bd330ecb61d01e6b5c1898997e`  
		Last Modified: Thu, 12 May 2022 06:46:29 GMT  
		Size: 32.3 MB (32287942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:582536fd64de163fda31ae947d6dfffa78cfad436c01b0408c7ff067bd4bcc84`  
		Last Modified: Thu, 12 May 2022 06:46:25 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:3-slim-buster` - linux; s390x

```console
$ docker pull ruby@sha256:17698adce6ea8da513bd37f39231c6ef2060c721e43812a135b90ecc9bf71492
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.6 MB (68624366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09f887749ae614b8d02c9d09b62441ec09a4270ab6ad7ade5f275dfecf9a1f9c`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 11 May 2022 00:44:47 GMT
ADD file:28b1e60f65391906bebd81248a4da766172138fab99b8b9e6b18bce76afea02d in / 
# Wed, 11 May 2022 00:44:49 GMT
CMD ["bash"]
# Wed, 11 May 2022 11:14:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 11:14:51 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 11 May 2022 11:14:52 GMT
ENV LANG=C.UTF-8
# Wed, 11 May 2022 11:23:56 GMT
ENV RUBY_MAJOR=3.1
# Wed, 11 May 2022 11:23:57 GMT
ENV RUBY_VERSION=3.1.2
# Wed, 11 May 2022 11:23:57 GMT
ENV RUBY_DOWNLOAD_SHA256=ca10d017f8a1b6d247556622c841fc56b90c03b1803f87198da1e4fd3ec3bf2a
# Wed, 11 May 2022 11:26:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 11 May 2022 11:26:04 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 11 May 2022 11:26:04 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 11 May 2022 11:26:04 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 May 2022 11:26:05 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 11 May 2022 11:26:05 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:bf64474a39a67000556a4502abd4584010a062b942cf8e2545d0502d38ffa150`  
		Last Modified: Wed, 11 May 2022 00:50:43 GMT  
		Size: 25.8 MB (25758738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b699904a5f5bfe1ebea696041265cf325f94502869867a1f9f818fd2ad465d`  
		Last Modified: Wed, 11 May 2022 11:44:01 GMT  
		Size: 10.8 MB (10821161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4d4e15daa6ff12eec7fa4e1464553aba8a53d2a9fa565545d7c2428c2ddb0a3`  
		Last Modified: Wed, 11 May 2022 11:43:59 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a4b959dfcf494f3f954f9f8f28c561f8585d364a3ce42da21de5666f1d5ca3f`  
		Last Modified: Wed, 11 May 2022 11:45:13 GMT  
		Size: 32.0 MB (32044093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9909b934f3666694e0907c7f1d83cf61534bcac3cf3f9a9c38f4acdd03c610d6`  
		Last Modified: Wed, 11 May 2022 11:45:11 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
