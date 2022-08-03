## `ruby:2-slim-buster`

```console
$ docker pull ruby@sha256:37b1a59b438e2227cd28718200157be30be9b4b7a9e32038acca19285d21341f
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
$ docker pull ruby@sha256:d8f99fac5d284c74be3b2a0d95de1567a77c841a3f2cc22bc675b5bc634e5631
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.3 MB (54263484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41953719237bce21e3565a69883c8c5c3bdada4351fa70676cc619f56197862f`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 02 Aug 2022 01:20:24 GMT
ADD file:81dbfe4f9df4d280f7580380c0c5c93ba71fedba17b3072d2b7b4bce127f88a9 in / 
# Tue, 02 Aug 2022 01:20:24 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 14:18:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 14:18:13 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 02 Aug 2022 14:18:13 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 14:45:24 GMT
ENV RUBY_MAJOR=2.7
# Tue, 02 Aug 2022 14:45:24 GMT
ENV RUBY_VERSION=2.7.6
# Tue, 02 Aug 2022 14:45:24 GMT
ENV RUBY_DOWNLOAD_SHA256=54dcd3044726c4ab75a9d4604720501442b229a3aed6a55fe909567da8807f24
# Tue, 02 Aug 2022 14:47:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 02 Aug 2022 14:47:15 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 02 Aug 2022 14:47:15 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 02 Aug 2022 14:47:15 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Aug 2022 14:47:16 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 02 Aug 2022 14:47:16 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:751ef25978b2971e15496369695ba51ed5b1b9aaca7e37b18a173d754d1ca820`  
		Last Modified: Tue, 02 Aug 2022 01:25:00 GMT  
		Size: 27.1 MB (27140083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5004f1658c2438c800c5651037f086bb966a3ab97b49f2fa04dfdfd6bc6589b3`  
		Last Modified: Tue, 02 Aug 2022 14:49:53 GMT  
		Size: 12.6 MB (12575384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b67fded145ff4487a01dae2b0d37a3e5d2688b0dfb6835f5ba4dfc737993f311`  
		Last Modified: Tue, 02 Aug 2022 14:49:51 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93e6be74ffc52b96c287feacae69f2f8b9231bf1eb745ab24f1ccafdb5d7dda4`  
		Last Modified: Tue, 02 Aug 2022 14:53:41 GMT  
		Size: 14.5 MB (14547641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e281afdfdde8503e676d9178c19da420cb90c464e3194d11c6b1c0539e93745`  
		Last Modified: Tue, 02 Aug 2022 14:53:39 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:2-slim-buster` - linux; arm variant v5

```console
$ docker pull ruby@sha256:c82a4eff19caebfa1b87ff7428b61666da7c5afbaccdce41f9a0c4f40ff6afee
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49148437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1910b5984efaa20368b52dbfeb5a8b18bd9c0eb9d0d4827502f92e1256cca09b`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 02 Aug 2022 00:49:37 GMT
ADD file:2ed7ca0d45c68b46a10ae186e8a03f98e72cadfeed17105668f53adf14d31e1f in / 
# Tue, 02 Aug 2022 00:49:38 GMT
CMD ["bash"]
# Wed, 03 Aug 2022 02:43:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 Aug 2022 02:43:52 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 03 Aug 2022 02:43:52 GMT
ENV LANG=C.UTF-8
# Wed, 03 Aug 2022 03:58:52 GMT
ENV RUBY_MAJOR=2.7
# Wed, 03 Aug 2022 03:58:52 GMT
ENV RUBY_VERSION=2.7.6
# Wed, 03 Aug 2022 03:58:52 GMT
ENV RUBY_DOWNLOAD_SHA256=54dcd3044726c4ab75a9d4604720501442b229a3aed6a55fe909567da8807f24
# Wed, 03 Aug 2022 04:02:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 03 Aug 2022 04:02:20 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 03 Aug 2022 04:02:20 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 03 Aug 2022 04:02:20 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Aug 2022 04:02:21 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 03 Aug 2022 04:02:21 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:187ecffbd1e0eae5de6567dff32bd58f28623635657779760c9d9539d6b7cc59`  
		Last Modified: Tue, 02 Aug 2022 00:57:06 GMT  
		Size: 24.9 MB (24889750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f36ed511c2c5f4184e7178ce05b43e8513b79f9755b84c0f3ef92f861166c07`  
		Last Modified: Wed, 03 Aug 2022 04:06:22 GMT  
		Size: 10.4 MB (10355879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d1758538fd2e006f0a80d5dcad5c3042faaaf65df5f5e295af5f908c37f87ff`  
		Last Modified: Wed, 03 Aug 2022 04:06:16 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8804c5622771d1c8597d6175cd1e7a3e36b7cf826f318faffb372813a2286bec`  
		Last Modified: Wed, 03 Aug 2022 04:11:23 GMT  
		Size: 13.9 MB (13902434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5695df75c47d9416af7ac5ead7c96ccaecda90a5ad5c929dd3b67c43fccb74c`  
		Last Modified: Wed, 03 Aug 2022 04:11:20 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:2-slim-buster` - linux; arm variant v7

```console
$ docker pull ruby@sha256:335e9bc0fc21fdc570a372e259b613b20fe9c1b35123368c4edf98a76c98418a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.4 MB (46418788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3af2d24872bfe6b01a68ec928b645f41cdbebe69fe95463e5a236dd897c08fc3`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 02 Aug 2022 00:59:42 GMT
ADD file:0656e10e6cb873c5d63fea742902bbcc364ebebda21b294bc210f6436505b520 in / 
# Tue, 02 Aug 2022 00:59:43 GMT
CMD ["bash"]
# Wed, 03 Aug 2022 20:56:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 Aug 2022 20:56:37 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 03 Aug 2022 20:56:37 GMT
ENV LANG=C.UTF-8
# Wed, 03 Aug 2022 21:37:04 GMT
ENV RUBY_MAJOR=2.7
# Wed, 03 Aug 2022 21:37:04 GMT
ENV RUBY_VERSION=2.7.6
# Wed, 03 Aug 2022 21:37:04 GMT
ENV RUBY_DOWNLOAD_SHA256=54dcd3044726c4ab75a9d4604720501442b229a3aed6a55fe909567da8807f24
# Wed, 03 Aug 2022 21:39:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 03 Aug 2022 21:39:36 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 03 Aug 2022 21:39:36 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 03 Aug 2022 21:39:36 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Aug 2022 21:39:37 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 03 Aug 2022 21:39:37 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:47c9fa1d05a77a2ace7faf7092bc54fda93d940a4ed5861769487557b38bb28b`  
		Last Modified: Tue, 02 Aug 2022 01:07:47 GMT  
		Size: 22.7 MB (22748031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e94d182bf90d9e27c4f78dd3ee605a78c7e9fcc4ee94dd663f40372edfcb0cff`  
		Last Modified: Wed, 03 Aug 2022 21:44:34 GMT  
		Size: 9.9 MB (9874536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d16e974ac8f7b730fd43d248c3121b21e1b7391c58ae7d19fd5950a6d4adfc2`  
		Last Modified: Wed, 03 Aug 2022 21:44:31 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87ee7bbad3c0776190a14b1e2d23b261339b16f577966916e289b8650e67add2`  
		Last Modified: Wed, 03 Aug 2022 21:49:24 GMT  
		Size: 13.8 MB (13795846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaf3e637ecf05311b5813fbd1aae4a5eb3c53ccf4555b223b2c68654e94cfdb7`  
		Last Modified: Wed, 03 Aug 2022 21:49:22 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:2-slim-buster` - linux; arm64 variant v8

```console
$ docker pull ruby@sha256:687895bb30a344122471edad3540852f9fa44f2391bbceb4b389804c04a95982
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.4 MB (51363465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a9101e46711076a320565de96f0d1e2ae814e113fed87b879bda1e82d1ca8e1`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 02 Aug 2022 00:41:03 GMT
ADD file:d973e057fdca9166fb9f39e73d7d5d4ca8ac2af6a55813580bf14a13cef4c159 in / 
# Tue, 02 Aug 2022 00:41:04 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 16:02:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 16:02:34 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 02 Aug 2022 16:02:35 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 16:28:45 GMT
ENV RUBY_MAJOR=2.7
# Tue, 02 Aug 2022 16:28:45 GMT
ENV RUBY_VERSION=2.7.6
# Tue, 02 Aug 2022 16:28:46 GMT
ENV RUBY_DOWNLOAD_SHA256=54dcd3044726c4ab75a9d4604720501442b229a3aed6a55fe909567da8807f24
# Tue, 02 Aug 2022 16:30:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 02 Aug 2022 16:30:27 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 02 Aug 2022 16:30:28 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 02 Aug 2022 16:30:29 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Aug 2022 16:30:30 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 02 Aug 2022 16:30:31 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:6d588874b4737b02fc84169cf7d3d1d70f20c7f5dbd1ddfe27de4aff25e23314`  
		Last Modified: Tue, 02 Aug 2022 00:46:56 GMT  
		Size: 25.9 MB (25914363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67c1417f563853f021d58748cb84a2d8727289286ea19a4fd87424da945f08f1`  
		Last Modified: Tue, 02 Aug 2022 16:34:51 GMT  
		Size: 11.3 MB (11274755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2583849177402a7aebec413e14ff3f79553920fbacd7d11b6d13b12b562bd09b`  
		Last Modified: Tue, 02 Aug 2022 16:34:48 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e135e6f7f24c9e3ff876ff56cff4a0657a519cdc8e67092f9be1211106ce29e6`  
		Last Modified: Tue, 02 Aug 2022 16:39:24 GMT  
		Size: 14.2 MB (14174004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13923d35d532b805511e9cf9c639a1085bb7971647739900dc905496beeda817`  
		Last Modified: Tue, 02 Aug 2022 16:39:22 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:2-slim-buster` - linux; 386

```console
$ docker pull ruby@sha256:2db5a3681e6f49e6e5cc1d37603ed0918b1c90f1e8ea134bd3f24f810b4449d0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.8 MB (58838491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd03c07b7ab99dc44a270814ddd9ba1785027382a5da8720316fbdcdf35be9f1`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 02 Aug 2022 00:39:47 GMT
ADD file:e8057ee44359188db14ad06a6f8e9cab7a301b479e0f7e0e61810abb0ecf48dd in / 
# Tue, 02 Aug 2022 00:39:47 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:00:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:00:07 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 02 Aug 2022 15:00:08 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 15:26:36 GMT
ENV RUBY_MAJOR=2.7
# Tue, 02 Aug 2022 15:26:36 GMT
ENV RUBY_VERSION=2.7.6
# Tue, 02 Aug 2022 15:26:37 GMT
ENV RUBY_DOWNLOAD_SHA256=54dcd3044726c4ab75a9d4604720501442b229a3aed6a55fe909567da8807f24
# Tue, 02 Aug 2022 15:28:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 02 Aug 2022 15:28:17 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 02 Aug 2022 15:28:18 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 02 Aug 2022 15:28:19 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Aug 2022 15:28:20 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 02 Aug 2022 15:28:21 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:0481fdd8148a195a336acc1d5b3d6b0f7fe46395e01c9b674e3ff6974b6ac5a7`  
		Last Modified: Tue, 02 Aug 2022 00:46:14 GMT  
		Size: 27.8 MB (27799555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eba19dab45d427843765e105492fc2f6e9afcbac88abb4fd92c69a85b7fb4507`  
		Last Modified: Tue, 02 Aug 2022 15:32:58 GMT  
		Size: 17.2 MB (17233251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3049b8955741ef2c315f062633f5d74f765dcc7021f5e815ff1937a57ce1f7a2`  
		Last Modified: Tue, 02 Aug 2022 15:32:55 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aef4f82e555abf1dc7211e02d7cb913da8d3deeea15a3cdf18e173bdd44d202c`  
		Last Modified: Tue, 02 Aug 2022 15:38:04 GMT  
		Size: 13.8 MB (13805341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56ba99389ecb57b7e0d912be3640272ab17bfd92c5c800b7a067e76e8c710112`  
		Last Modified: Tue, 02 Aug 2022 15:38:02 GMT  
		Size: 144.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:2-slim-buster` - linux; mips64le

```console
$ docker pull ruby@sha256:a2fa151b1afb8a9979856411275972b8959630249e6ac6473d4202c97b2033d5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.9 MB (51903414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2f8ecfb76427faa2c34e754ddf0cb432f0a172ebcd627deada349573d3e7bf7`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 02 Aug 2022 01:11:38 GMT
ADD file:b7476c2fa56932f078ca753025b4af1a7d8b859c69923deb3dbe182c4dc5d9f2 in / 
# Tue, 02 Aug 2022 01:11:42 GMT
CMD ["bash"]
# Wed, 03 Aug 2022 00:31:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 Aug 2022 00:31:47 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 03 Aug 2022 00:31:50 GMT
ENV LANG=C.UTF-8
# Wed, 03 Aug 2022 02:48:42 GMT
ENV RUBY_MAJOR=2.7
# Wed, 03 Aug 2022 02:48:45 GMT
ENV RUBY_VERSION=2.7.6
# Wed, 03 Aug 2022 02:48:47 GMT
ENV RUBY_DOWNLOAD_SHA256=54dcd3044726c4ab75a9d4604720501442b229a3aed6a55fe909567da8807f24
# Wed, 03 Aug 2022 02:58:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 03 Aug 2022 02:58:26 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 03 Aug 2022 02:58:29 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 03 Aug 2022 02:58:32 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Aug 2022 02:58:38 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 03 Aug 2022 02:58:41 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:1ebd72c951363da95763516634b561a0cd58d555f86d8bb84550dbc5eefb0d34`  
		Last Modified: Tue, 02 Aug 2022 01:22:25 GMT  
		Size: 25.8 MB (25814575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccd142d69b4d1391a582426b4d5cbf97bf98e432cf809909e95a88949d752428`  
		Last Modified: Wed, 03 Aug 2022 03:01:24 GMT  
		Size: 11.6 MB (11635553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ea2f691f978aefd29eb4e25734931c0fbf82a08da2fc00e48c030b34d3f34a8`  
		Last Modified: Wed, 03 Aug 2022 03:01:14 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3959144e1254af2d92da60c6b6f3253a159ff96e420dfac923a1d5cb569bcef4`  
		Last Modified: Wed, 03 Aug 2022 03:06:58 GMT  
		Size: 14.5 MB (14452942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:567ffa7591917050a61d5e09a267c20198283472a313c2590faaa385c6391f92`  
		Last Modified: Wed, 03 Aug 2022 03:06:51 GMT  
		Size: 144.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:2-slim-buster` - linux; ppc64le

```console
$ docker pull ruby@sha256:e7b16c79c00c4392766e4f30f9022eada9d5562d82c0008f372617807d0b394f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.3 MB (58313141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5ad9be8c9c5b9e45752f13aefb58ffd70560e97ee4d514f2c70cb651b8a2ced`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:04 GMT
ADD file:6d33ba25d3625e5f445fc2183b60c64e2cbc780cb541d7f8ac76ce193b311d13 in / 
# Tue, 02 Aug 2022 01:18:06 GMT
CMD ["bash"]
# Wed, 03 Aug 2022 00:33:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 Aug 2022 00:33:51 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 03 Aug 2022 00:33:52 GMT
ENV LANG=C.UTF-8
# Wed, 03 Aug 2022 01:14:23 GMT
ENV RUBY_MAJOR=2.7
# Wed, 03 Aug 2022 01:14:24 GMT
ENV RUBY_VERSION=2.7.6
# Wed, 03 Aug 2022 01:14:24 GMT
ENV RUBY_DOWNLOAD_SHA256=54dcd3044726c4ab75a9d4604720501442b229a3aed6a55fe909567da8807f24
# Wed, 03 Aug 2022 01:17:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 03 Aug 2022 01:17:21 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 03 Aug 2022 01:17:21 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 03 Aug 2022 01:17:22 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Aug 2022 01:17:23 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 03 Aug 2022 01:17:24 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:fc8842eebb7ccaf249b2bb2d6a3878fffdae26c9db8f23b393c7f76a6249d2f6`  
		Last Modified: Tue, 02 Aug 2022 01:25:45 GMT  
		Size: 30.6 MB (30560308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d838b51a88863f86df39309502c4b9382dec0f90e8f13f1f7a135bfd50979b6a`  
		Last Modified: Wed, 03 Aug 2022 01:22:14 GMT  
		Size: 12.7 MB (12722052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1a9f98a7f3660fcce9db2644e8150eab122f86e53239594f7e74e83591195ee`  
		Last Modified: Wed, 03 Aug 2022 01:22:10 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a952718ade295fa37fa7ac7d5df6978fc62c4bc4341bfff1979f6ae00a9fac3`  
		Last Modified: Wed, 03 Aug 2022 01:27:32 GMT  
		Size: 15.0 MB (15030406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49a60269ffc94a418725076d5b50b786bf40a635282fcce8d52a61acdf92dc7a`  
		Last Modified: Wed, 03 Aug 2022 01:27:29 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:2-slim-buster` - linux; s390x

```console
$ docker pull ruby@sha256:6108d09d5825f2fe4a136e94266730484509c08b5bc5cefa5e664802671c2019
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.3 MB (51316753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:173677edcebbec4be4722543d11110ae0148eea9610b8cc77c1c205cdb1178db`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 02 Aug 2022 00:42:56 GMT
ADD file:e455828726a550da92d8fc424a6d7694b6be24a8ca52a6152e2ee89d4f7269d0 in / 
# Tue, 02 Aug 2022 00:42:58 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 11:03:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 11:03:22 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 02 Aug 2022 11:03:22 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 11:27:21 GMT
ENV RUBY_MAJOR=2.7
# Tue, 02 Aug 2022 11:27:21 GMT
ENV RUBY_VERSION=2.7.6
# Tue, 02 Aug 2022 11:27:21 GMT
ENV RUBY_DOWNLOAD_SHA256=54dcd3044726c4ab75a9d4604720501442b229a3aed6a55fe909567da8807f24
# Tue, 02 Aug 2022 11:28:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 02 Aug 2022 11:28:53 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 02 Aug 2022 11:28:53 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 02 Aug 2022 11:28:53 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Aug 2022 11:28:54 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 02 Aug 2022 11:28:54 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:42614a0fa81c110340e6a5a5db155f27bbb6fa8c1e2421b2c2c5f148ea18f35d`  
		Last Modified: Tue, 02 Aug 2022 00:48:34 GMT  
		Size: 25.8 MB (25758761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:691f0736152184b1d9f7eb0f997da97231488c6fd7982b248dfbcacbbe10bc89`  
		Last Modified: Tue, 02 Aug 2022 11:32:57 GMT  
		Size: 10.8 MB (10821329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7acc40c3b4a0a1d44f47ab69b3992b747932168b596c59050c6e88c8cad4d13`  
		Last Modified: Tue, 02 Aug 2022 11:32:55 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71b06b49e84bbcb1dd3338fff5b913e5c80320c4fe7986cca7bf478ac4ad67a6`  
		Last Modified: Tue, 02 Aug 2022 11:35:58 GMT  
		Size: 14.7 MB (14736288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15e9ae036147078128f3f84f1e276f199cc6e5f164baf4ec429faf16b64829a2`  
		Last Modified: Tue, 02 Aug 2022 11:35:57 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
