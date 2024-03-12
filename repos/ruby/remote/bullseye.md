## `ruby:bullseye`

```console
$ docker pull ruby@sha256:e2977da0b0095c7046ebb87e02fad2b9b050af4e0718d1cd80c53559b82d0b06
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

### `ruby:bullseye` - linux; amd64

```console
$ docker pull ruby@sha256:d0cb443d2c3f4b9934e636f70b1ae56140c35587c104a86925c1947384ea13b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.7 MB (358747493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a6fc66601c453eb35f35bf22b82ac0d0f12f387504508f06b8cd127f4280526`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 29 Feb 2024 21:45:14 GMT
ADD file:ff6bc341b5945acf6b9c190d70b5f5806fb3fae7b5c568ad6395aec1b95ba89c in / 
# Thu, 29 Feb 2024 21:45:14 GMT
CMD ["bash"]
# Thu, 29 Feb 2024 21:45:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 29 Feb 2024 21:45:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 29 Feb 2024 21:45:14 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 29 Feb 2024 21:45:14 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Thu, 29 Feb 2024 21:45:14 GMT
ENV LANG=C.UTF-8
# Thu, 29 Feb 2024 21:45:14 GMT
ENV RUBY_VERSION=3.3.0
# Thu, 29 Feb 2024 21:45:14 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.0.tar.xz
# Thu, 29 Feb 2024 21:45:14 GMT
ENV RUBY_DOWNLOAD_SHA256=676b65a36e637e90f982b57b059189b3276b9045034dcd186a7e9078847b975b
# Thu, 29 Feb 2024 21:45:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		wget -O 'arm64-fix.patch' 'https://github.com/ruby/ruby/commit/7f97e3540ce448b501bcbee15afac5f94bb22dd9.patch?full_index=1'; 	echo '86bc65415fd62cb2272a4df249f39fb79db15617ad05c540e05a22f02eae73b3 *arm64-fix.patch' | sha256sum --check --strict; 	patch -p1 -i arm64-fix.patch; 	rm arm64-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 29 Feb 2024 21:45:14 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 29 Feb 2024 21:45:14 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 29 Feb 2024 21:45:14 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Feb 2024 21:45:14 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Thu, 29 Feb 2024 21:45:14 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:ec335f17d0c74f7a270925cb1bbd29acc72ae904c6f4570f9ae369e3eebb64ed`  
		Last Modified: Tue, 12 Mar 2024 01:25:59 GMT  
		Size: 55.1 MB (55084969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2b4675e1918dcb7f5c9bfedbb5a8634d2459306d1f3b91f08c7293380f10585`  
		Last Modified: Tue, 12 Mar 2024 06:03:29 GMT  
		Size: 15.8 MB (15763469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f67b1746a83d257a6398cf8eec47bfa1f854670097ea4234f12857cfc7d5932`  
		Last Modified: Tue, 12 Mar 2024 06:03:46 GMT  
		Size: 54.6 MB (54588494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e6939aa9b63c6ee738fb4a9904fac366ecb96aec3d980993009e3b7ee3f7516`  
		Last Modified: Tue, 12 Mar 2024 06:04:18 GMT  
		Size: 197.0 MB (196985243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c795ca9f400c519cca697f103b3fcbc49e404a99899c5c5240a910162e638dd`  
		Last Modified: Tue, 12 Mar 2024 07:01:21 GMT  
		Size: 199.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caf1ca4068af691246092fe5819e0df6f3dd4d999bc8ba4d419ff582af4b3631`  
		Last Modified: Tue, 12 Mar 2024 07:01:21 GMT  
		Size: 36.3 MB (36324976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4235630892232fbd772f06f57618743dd1530a94f42d3e84bf78285236b8256d`  
		Last Modified: Tue, 12 Mar 2024 07:01:20 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:bullseye` - unknown; unknown

```console
$ docker pull ruby@sha256:fc412b861d715b655884f1925a0f01fd87dfdb442bd70d56a6c11970685587e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15118286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4117a0d53d6d139a3e113d6401241814153e44516d0e5ce39603998113ace02a`

```dockerfile
```

-	Layers:
	-	`sha256:34d24bc990c2a77034104681e7dc05311454c05f18f4423494b641e56c159a94`  
		Last Modified: Tue, 12 Mar 2024 07:01:21 GMT  
		Size: 15.1 MB (15094208 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18dcd4d3482b36e5eb1bd702437458699bbe65e36e24ba541d558235cf419612`  
		Last Modified: Tue, 12 Mar 2024 07:01:20 GMT  
		Size: 24.1 KB (24078 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:bullseye` - linux; arm variant v5

```console
$ docker pull ruby@sha256:31aa4e984cdcfa39034a8fb9ce32d5e3d7420ff940cd65e40f1ca84bdce69922
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.8 MB (327847396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4c6e5c6726cf2561cfbbe227e02e2151e04d483810c836f3c0441be64aa2619`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 13 Feb 2024 01:08:36 GMT
ADD file:e60f5be11728cbf36bc5b1ee8a186ec55fb8e6bbc13d939c76ff03e91e934e90 in / 
# Tue, 13 Feb 2024 01:08:37 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:42:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 01:43:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 01:45:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 29 Feb 2024 21:45:14 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Thu, 29 Feb 2024 21:45:14 GMT
ENV LANG=C.UTF-8
# Thu, 29 Feb 2024 21:45:14 GMT
ENV RUBY_VERSION=3.3.0
# Thu, 29 Feb 2024 21:45:14 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.0.tar.xz
# Thu, 29 Feb 2024 21:45:14 GMT
ENV RUBY_DOWNLOAD_SHA256=676b65a36e637e90f982b57b059189b3276b9045034dcd186a7e9078847b975b
# Thu, 29 Feb 2024 21:45:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		wget -O 'arm64-fix.patch' 'https://github.com/ruby/ruby/commit/7f97e3540ce448b501bcbee15afac5f94bb22dd9.patch?full_index=1'; 	echo '86bc65415fd62cb2272a4df249f39fb79db15617ad05c540e05a22f02eae73b3 *arm64-fix.patch' | sha256sum --check --strict; 	patch -p1 -i arm64-fix.patch; 	rm arm64-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 29 Feb 2024 21:45:14 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 29 Feb 2024 21:45:14 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 29 Feb 2024 21:45:14 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Feb 2024 21:45:14 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Thu, 29 Feb 2024 21:45:14 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:bbf2c22df990ef0a734a6681b9078a2b5c2ea21e9fee5c8e62c2171859d433d8`  
		Last Modified: Tue, 13 Feb 2024 01:13:53 GMT  
		Size: 52.6 MB (52586881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:116d258d0865d6b4269397d1ca385bf94ac78bce402a330982fe9c5cf6cf5e74`  
		Last Modified: Tue, 13 Feb 2024 01:55:14 GMT  
		Size: 15.4 MB (15374936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc02d7d7d38fe07956e4599b2b651fc55e5e2b28292d866c9380c4dfe44188b0`  
		Last Modified: Tue, 13 Feb 2024 01:55:36 GMT  
		Size: 52.3 MB (52329047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bb168a1b4717ff082f25d1e77a5afa2bceccca40396bd897118ae6007b17d88`  
		Last Modified: Tue, 13 Feb 2024 01:56:21 GMT  
		Size: 175.2 MB (175158430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acb228c55465612d9546d3aa338d46d60384193a8390a618da26e67d62141fa8`  
		Last Modified: Wed, 14 Feb 2024 19:26:25 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:274fafb5dde6c02de56923f8813468e75f3684b54cec12826a99d420f8ad4d57`  
		Last Modified: Fri, 01 Mar 2024 00:26:49 GMT  
		Size: 32.4 MB (32397763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4398afd2e071dc643be9af1de1f059b6c5b5ca838b108149b4374b733355447e`  
		Last Modified: Fri, 01 Mar 2024 00:26:48 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:bullseye` - unknown; unknown

```console
$ docker pull ruby@sha256:1d10cde2a494e62c328deed32decefc19b62353e41fd30e8673c23ea53c57083
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14914234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd686a8a8c1d55312f0d6c37046995488198d0ba25695d5fd4663f734715b614`

```dockerfile
```

-	Layers:
	-	`sha256:798077b21dee1b6778514305bed7d688845adb70705ed24d93d09295c17b75dd`  
		Last Modified: Fri, 01 Mar 2024 00:26:48 GMT  
		Size: 14.9 MB (14890723 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d0ebaacf24826a62568b59c9ed435ab5d93fd5290da338537e958ac4e2d1d88`  
		Last Modified: Fri, 01 Mar 2024 00:26:47 GMT  
		Size: 23.5 KB (23511 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:bullseye` - linux; arm variant v7

```console
$ docker pull ruby@sha256:f84eade11f23d576e718e956da71362dd6727e389c92320a812bae236b0c6c7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.2 MB (315221777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b37e5ef5a4273f7f6e3b81c3826b65daab00a341ac59e8c64b411dbb01e4bb95`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 13 Feb 2024 01:20:21 GMT
ADD file:a6e150be02b0758f7cb3863651ae586c1592e19949e91c78e3771ceaad602a2a in / 
# Tue, 13 Feb 2024 01:20:22 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 04:16:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 04:16:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 04:17:41 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 29 Feb 2024 21:45:14 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Thu, 29 Feb 2024 21:45:14 GMT
ENV LANG=C.UTF-8
# Thu, 29 Feb 2024 21:45:14 GMT
ENV RUBY_VERSION=3.3.0
# Thu, 29 Feb 2024 21:45:14 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.0.tar.xz
# Thu, 29 Feb 2024 21:45:14 GMT
ENV RUBY_DOWNLOAD_SHA256=676b65a36e637e90f982b57b059189b3276b9045034dcd186a7e9078847b975b
# Thu, 29 Feb 2024 21:45:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		wget -O 'arm64-fix.patch' 'https://github.com/ruby/ruby/commit/7f97e3540ce448b501bcbee15afac5f94bb22dd9.patch?full_index=1'; 	echo '86bc65415fd62cb2272a4df249f39fb79db15617ad05c540e05a22f02eae73b3 *arm64-fix.patch' | sha256sum --check --strict; 	patch -p1 -i arm64-fix.patch; 	rm arm64-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 29 Feb 2024 21:45:14 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 29 Feb 2024 21:45:14 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 29 Feb 2024 21:45:14 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Feb 2024 21:45:14 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Thu, 29 Feb 2024 21:45:14 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:623a3ffac68434a8d471ef584bdb1dcbfafd4648778c484c1566ff7910d04b0e`  
		Last Modified: Tue, 13 Feb 2024 01:27:15 GMT  
		Size: 50.2 MB (50241706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c12ee536bcdc51ad528b0ed79abe7893d5c4c356dd3b5d3321eb8eda18294ca`  
		Last Modified: Tue, 13 Feb 2024 04:28:21 GMT  
		Size: 14.9 MB (14879180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eebe7ea1391c25ae1a4d9bd9382746170a0edc00c1085152e15d7ade4b3fa456`  
		Last Modified: Tue, 13 Feb 2024 04:28:43 GMT  
		Size: 50.4 MB (50357734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dbdd712885977c538429b59aa851dd5be6499412cb7b2ba0cb37a20b9186252`  
		Last Modified: Tue, 13 Feb 2024 04:29:25 GMT  
		Size: 167.4 MB (167437433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f39d0a753d6abf1f2e015f4a4c7f9b15f6af8d0c2bd9bd9e9fef3a35e80d2bf1`  
		Last Modified: Fri, 16 Feb 2024 06:35:52 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fd940fb41025b3a9e79e98421e907e2e0d25734a6e453f85a8848bb6a4e2dab`  
		Last Modified: Thu, 29 Feb 2024 23:37:29 GMT  
		Size: 32.3 MB (32305384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15ba99a86832c5ada4c6ac5f4a186ca6f628e1f68d2d43ca2aac5996fa4227b5`  
		Last Modified: Thu, 29 Feb 2024 23:37:28 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:bullseye` - unknown; unknown

```console
$ docker pull ruby@sha256:be0ed8476d7ca10715f90fae84f8f9ab6e9c6b359d8deb591ffd58b742648e06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14919605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f5f2aa321698f9ffce7f34a637d3408c9566e619e813c86bfb3bc7355ed0174`

```dockerfile
```

-	Layers:
	-	`sha256:ff153b93e21e8f2e7aa355cd3d9ad8fa773a5cf5cc5d15c537fbc2dc6dbd2a28`  
		Last Modified: Thu, 29 Feb 2024 23:37:28 GMT  
		Size: 14.9 MB (14896097 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3299136693fe67ba5315fe2a72b6704a8ca867aa820def53e143050039eee2eb`  
		Last Modified: Thu, 29 Feb 2024 23:37:27 GMT  
		Size: 23.5 KB (23508 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:bullseye` - linux; arm64 variant v8

```console
$ docker pull ruby@sha256:26737cb89fa1b15a2b619ff8594a80bf6610d182d1fa25ab35a6b636c185f336
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.3 MB (350281081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10f70a6ef382e9b82df2c27858cb09ce0fcc4d76bd51b1d822b685d02147f914`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:27 GMT
ADD file:46791e28a2eef97a17393ff5cf2928d2e721f9380340a34c7d2e85053edec7c1 in / 
# Tue, 13 Feb 2024 00:41:27 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:38:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 01:39:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 01:40:03 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 29 Feb 2024 21:45:14 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Thu, 29 Feb 2024 21:45:14 GMT
ENV LANG=C.UTF-8
# Thu, 29 Feb 2024 21:45:14 GMT
ENV RUBY_VERSION=3.3.0
# Thu, 29 Feb 2024 21:45:14 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.0.tar.xz
# Thu, 29 Feb 2024 21:45:14 GMT
ENV RUBY_DOWNLOAD_SHA256=676b65a36e637e90f982b57b059189b3276b9045034dcd186a7e9078847b975b
# Thu, 29 Feb 2024 21:45:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		wget -O 'arm64-fix.patch' 'https://github.com/ruby/ruby/commit/7f97e3540ce448b501bcbee15afac5f94bb22dd9.patch?full_index=1'; 	echo '86bc65415fd62cb2272a4df249f39fb79db15617ad05c540e05a22f02eae73b3 *arm64-fix.patch' | sha256sum --check --strict; 	patch -p1 -i arm64-fix.patch; 	rm arm64-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 29 Feb 2024 21:45:14 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 29 Feb 2024 21:45:14 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 29 Feb 2024 21:45:14 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Feb 2024 21:45:14 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Thu, 29 Feb 2024 21:45:14 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:4245faf914201feff648b048cbaf6c46414d24a56e29e4cff1f82ac1b151d326`  
		Last Modified: Tue, 13 Feb 2024 00:45:14 GMT  
		Size: 53.7 MB (53721486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95d359f54bdf6c7734649777e288d4d317d49bd63e944dd5f852641a97b61527`  
		Last Modified: Tue, 13 Feb 2024 01:47:39 GMT  
		Size: 15.7 MB (15749141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53c2c85b768f52fc0353f0af0e43d671b1d1025996f39d238e750611070d206c`  
		Last Modified: Tue, 13 Feb 2024 01:47:53 GMT  
		Size: 54.7 MB (54693679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65abc8b7accd0e9bdc9cc49eb9156409ec3f7da3e3f756461cedc2eba2531331`  
		Last Modified: Tue, 13 Feb 2024 01:48:18 GMT  
		Size: 189.9 MB (189883632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe33fe37d776be3b8accfcb4bba43ed1c66635bad55e10561a1d6dce2d2b62be`  
		Last Modified: Wed, 14 Feb 2024 08:19:36 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac4b375187668ae77fd0e721093c23d0c54da80b59f03cb67c1ffe8cf1470e80`  
		Last Modified: Thu, 29 Feb 2024 23:05:29 GMT  
		Size: 36.2 MB (36232803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bc2e23e17f70cf98a78350e49dd4ad70fc2c557e1481acfc7e055dfb2786448`  
		Last Modified: Thu, 29 Feb 2024 23:05:28 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:bullseye` - unknown; unknown

```console
$ docker pull ruby@sha256:b5c36c5fd271109e09665a0aab306efe0d430cf972d2c2f58a89b295fae7d897
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15120099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:283a8cd8e97f582472111906a22bd0130568cea2874a481b34aafc5c7f91dc6a`

```dockerfile
```

-	Layers:
	-	`sha256:453a2e4a013313da9bcfc820ce3514b5d5b2471fe9259de1ee582a1bae4207c3`  
		Last Modified: Thu, 29 Feb 2024 23:05:29 GMT  
		Size: 15.1 MB (15096674 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd246fd78f1afe343c12c4e3b794ee6d2421fd09ec622b4ce26125f3add5c9fa`  
		Last Modified: Thu, 29 Feb 2024 23:05:28 GMT  
		Size: 23.4 KB (23425 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:bullseye` - linux; 386

```console
$ docker pull ruby@sha256:125219b0094fe033a89734d886caf3e56256d05ba4cf2083b95d71aa06dc2817
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.5 MB (360521681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a65b0a023eb17bc443aa5eccc2b7a82b25c79fbe8dee47a9f133be9e60cf698`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 29 Feb 2024 21:45:14 GMT
ADD file:e7e92b37650e4d33c3374ca47bc378c2b4e15f7c7e0a7c7fc659a29c5b3fc583 in / 
# Thu, 29 Feb 2024 21:45:14 GMT
CMD ["bash"]
# Thu, 29 Feb 2024 21:45:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 29 Feb 2024 21:45:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 29 Feb 2024 21:45:14 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 29 Feb 2024 21:45:14 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Thu, 29 Feb 2024 21:45:14 GMT
ENV LANG=C.UTF-8
# Thu, 29 Feb 2024 21:45:14 GMT
ENV RUBY_VERSION=3.3.0
# Thu, 29 Feb 2024 21:45:14 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.0.tar.xz
# Thu, 29 Feb 2024 21:45:14 GMT
ENV RUBY_DOWNLOAD_SHA256=676b65a36e637e90f982b57b059189b3276b9045034dcd186a7e9078847b975b
# Thu, 29 Feb 2024 21:45:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		wget -O 'arm64-fix.patch' 'https://github.com/ruby/ruby/commit/7f97e3540ce448b501bcbee15afac5f94bb22dd9.patch?full_index=1'; 	echo '86bc65415fd62cb2272a4df249f39fb79db15617ad05c540e05a22f02eae73b3 *arm64-fix.patch' | sha256sum --check --strict; 	patch -p1 -i arm64-fix.patch; 	rm arm64-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 29 Feb 2024 21:45:14 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 29 Feb 2024 21:45:14 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 29 Feb 2024 21:45:14 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Feb 2024 21:45:14 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Thu, 29 Feb 2024 21:45:14 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:ec2ed44737cc768246d63628c6de48f2d223cdb3a6c218bddd11786679e34647`  
		Last Modified: Tue, 12 Mar 2024 01:03:04 GMT  
		Size: 56.1 MB (56057973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80e62ee72cfeca9426a0e18adfa8e6b05d9f029372d831f73d3e089ccb16f297`  
		Last Modified: Tue, 12 Mar 2024 07:54:46 GMT  
		Size: 16.3 MB (16267990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e632a01713bf6f27a1de411f14f1e21b375412e471fa832f03dc7ea3c86a0a51`  
		Last Modified: Tue, 12 Mar 2024 07:55:07 GMT  
		Size: 55.9 MB (55927686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbfe6f6eb32ca002367ebec491da1c709c88fc7418bca1dc16043bf62ff525ff`  
		Last Modified: Tue, 12 Mar 2024 07:55:52 GMT  
		Size: 199.9 MB (199890619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e49325854a7675284fbd6046324138626e777f5280cb5557ebf70e119a3f0ea`  
		Last Modified: Tue, 12 Mar 2024 08:58:48 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dff0c22a672c9fe6539d0caa70b58e6f4fcb2513c3ba25ae8331f4fecd2cb97a`  
		Last Modified: Tue, 12 Mar 2024 08:59:11 GMT  
		Size: 32.4 MB (32377073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8de71615cf5a0ae7af01c73c2f47a3d0cf10d140ce946611007590a12b9ca478`  
		Last Modified: Tue, 12 Mar 2024 08:59:10 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:bullseye` - unknown; unknown

```console
$ docker pull ruby@sha256:37c49f31a3aca1dc03531a02a5919f030bfd0333c28c33d042e1fb42e917511d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15107084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae1676cbeeced2fa660aa2a6594c6a1aa48bce8b818ca54a4839a826424cdabd`

```dockerfile
```

-	Layers:
	-	`sha256:576a345710c064af7a79e91ced7f6b5805f809d4d9c0f00645319448e807fb73`  
		Last Modified: Tue, 12 Mar 2024 08:59:11 GMT  
		Size: 15.1 MB (15083039 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7447f6ad37684e5258f07d7cce565cc6550905c8ef04982d71971ec58c7272fa`  
		Last Modified: Tue, 12 Mar 2024 08:59:10 GMT  
		Size: 24.0 KB (24045 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:bullseye` - linux; mips64le

```console
$ docker pull ruby@sha256:c5105c1b7b2427a0dca63688159cb5a7da03b2f35c10d699657de07dc5fc8b4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **335.1 MB (335147939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1f7678b884ad8d7f7632011724bb063a4e946aab4a42f9b6d148a1aba168fe6`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 13 Feb 2024 02:04:48 GMT
ADD file:f0c2e3e71ce8133518aba22664b25c63fbd8c964a5c5ce64025477e120c8e59c in / 
# Tue, 13 Feb 2024 02:04:54 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 03:52:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 03:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 04:00:01 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 29 Feb 2024 21:45:14 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Thu, 29 Feb 2024 21:45:14 GMT
ENV LANG=C.UTF-8
# Thu, 29 Feb 2024 21:45:14 GMT
ENV RUBY_VERSION=3.3.0
# Thu, 29 Feb 2024 21:45:14 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.0.tar.xz
# Thu, 29 Feb 2024 21:45:14 GMT
ENV RUBY_DOWNLOAD_SHA256=676b65a36e637e90f982b57b059189b3276b9045034dcd186a7e9078847b975b
# Thu, 29 Feb 2024 21:45:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		wget -O 'arm64-fix.patch' 'https://github.com/ruby/ruby/commit/7f97e3540ce448b501bcbee15afac5f94bb22dd9.patch?full_index=1'; 	echo '86bc65415fd62cb2272a4df249f39fb79db15617ad05c540e05a22f02eae73b3 *arm64-fix.patch' | sha256sum --check --strict; 	patch -p1 -i arm64-fix.patch; 	rm arm64-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 29 Feb 2024 21:45:14 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 29 Feb 2024 21:45:14 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 29 Feb 2024 21:45:14 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Feb 2024 21:45:14 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Thu, 29 Feb 2024 21:45:14 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:8fd455dd9aba699cef01f8ec9dcd521cc60e9d65f6f4a8b4682b184d6d9f01cb`  
		Last Modified: Tue, 13 Feb 2024 02:15:55 GMT  
		Size: 53.3 MB (53303273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bba3bdef7a4adaf4b26d1c9d17cecf0116391ff83640a2b297c799a3c9ab2486`  
		Last Modified: Tue, 13 Feb 2024 04:23:58 GMT  
		Size: 15.7 MB (15734290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27b01501f8952da39445ba5df82589cc4034f4701bb34fc660690e4a1841ed4c`  
		Last Modified: Tue, 13 Feb 2024 04:24:44 GMT  
		Size: 53.3 MB (53310605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73b7e5ed5b619e2f3d0a778cafde0e1fc84ca5cced5b5458d11a7ee49229b375`  
		Last Modified: Tue, 13 Feb 2024 04:26:42 GMT  
		Size: 179.1 MB (179094416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:649e8cb3a7ada2899989d58a8c5376f5aca7d210d2db0fb56fe3043719c588fd`  
		Last Modified: Fri, 01 Mar 2024 03:57:27 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19e3f811decd989d22cc6e7f3c24ad2d184b06b767f91930ddcd7e89d48820d8`  
		Last Modified: Fri, 01 Mar 2024 03:57:30 GMT  
		Size: 33.7 MB (33705015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58e843ddde117c1f3799176583d430f677361d5f436ec38fceaec01521c06dbc`  
		Last Modified: Fri, 01 Mar 2024 03:57:27 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:bullseye` - unknown; unknown

```console
$ docker pull ruby@sha256:393c0bec0411bf5c155fb75143dd88bc08ffd58580dad08863e960fab8c1bc2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 KB (23925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e0574d96aa6a6cc3d73481b31dadf5e9f1b23a816780267ba7b3e83b6e5acd8`

```dockerfile
```

-	Layers:
	-	`sha256:ee4d7acf8cbe6a64655618463f5ca0b895b9f34e391d459561a8c592c3dc8341`  
		Last Modified: Fri, 01 Mar 2024 03:57:23 GMT  
		Size: 23.9 KB (23925 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:bullseye` - linux; ppc64le

```console
$ docker pull ruby@sha256:5ef720547788787ffc163f4b1f1b3c340fef1bd057f097a63f887bb08fa4a670
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **365.0 MB (364978171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:602652bac6667646aeb9d5f88fc35209b083e5f4f38dbb3520cd9c70d4c44f2f`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 13 Feb 2024 00:39:15 GMT
ADD file:de34873811ec1071766dcf77b8d1180714c8e5b4373bed3aaf9a9e742ade2fee in / 
# Tue, 13 Feb 2024 00:39:19 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 07:23:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 07:24:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 07:26:45 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 29 Feb 2024 21:45:14 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Thu, 29 Feb 2024 21:45:14 GMT
ENV LANG=C.UTF-8
# Thu, 29 Feb 2024 21:45:14 GMT
ENV RUBY_VERSION=3.3.0
# Thu, 29 Feb 2024 21:45:14 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.0.tar.xz
# Thu, 29 Feb 2024 21:45:14 GMT
ENV RUBY_DOWNLOAD_SHA256=676b65a36e637e90f982b57b059189b3276b9045034dcd186a7e9078847b975b
# Thu, 29 Feb 2024 21:45:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		wget -O 'arm64-fix.patch' 'https://github.com/ruby/ruby/commit/7f97e3540ce448b501bcbee15afac5f94bb22dd9.patch?full_index=1'; 	echo '86bc65415fd62cb2272a4df249f39fb79db15617ad05c540e05a22f02eae73b3 *arm64-fix.patch' | sha256sum --check --strict; 	patch -p1 -i arm64-fix.patch; 	rm arm64-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 29 Feb 2024 21:45:14 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 29 Feb 2024 21:45:14 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 29 Feb 2024 21:45:14 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Feb 2024 21:45:14 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Thu, 29 Feb 2024 21:45:14 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:5b3ca2d45f6b2df666b88854e431316a856c6ecacdd29894dd599694e415a1eb`  
		Last Modified: Tue, 13 Feb 2024 00:44:22 GMT  
		Size: 59.0 MB (58954488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cfa650184f634b15bc0f1ddd50aeaa4b660e83cbc9fd51d576c3910ebaaad53`  
		Last Modified: Tue, 13 Feb 2024 07:37:27 GMT  
		Size: 16.8 MB (16765559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b20c4f70ca0212997eb1b2c82b5f1feb6920ff2654089e68975cba4b400a4451`  
		Last Modified: Tue, 13 Feb 2024 07:37:46 GMT  
		Size: 58.9 MB (58872935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73b71a4e8c3360ab2f0fc44790fa318623d9b5bf860bb3aff76bf5e481709053`  
		Last Modified: Tue, 13 Feb 2024 07:38:23 GMT  
		Size: 196.3 MB (196324754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3330773b260f01906d8b88b37c836d3220c4f9cac48b5952517dfd5d2abf9cf6`  
		Last Modified: Wed, 14 Feb 2024 04:38:53 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83075c0aaaa6e325f1b2dd791b1bf3b1f4f1df7f784a13eb172fe30d481bf5de`  
		Last Modified: Thu, 29 Feb 2024 23:01:59 GMT  
		Size: 34.1 MB (34060095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a05f2dffe5e0696d961b187099bd0e8eaccc731c01744737ce2b6c5080f0781d`  
		Last Modified: Thu, 29 Feb 2024 23:01:57 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:bullseye` - unknown; unknown

```console
$ docker pull ruby@sha256:1eaaa4302591e8fc8ef476376af2edc68365e4af0f90215b173cc0f98569f16a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15086970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ac8d3a3611f0c6761dc70ebb6621628435ed9d674046c4d0a9ad0244c2ed224`

```dockerfile
```

-	Layers:
	-	`sha256:c399e1c3660d51a05eb11280931ae0f41992c48d3b40dee015a6195d762947c7`  
		Last Modified: Thu, 29 Feb 2024 23:01:57 GMT  
		Size: 15.1 MB (15063513 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf859c4651d077f2d66aa9e09415d41bc4c75dca99066e0365ac79dce70b5321`  
		Last Modified: Thu, 29 Feb 2024 23:01:56 GMT  
		Size: 23.5 KB (23457 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:bullseye` - linux; s390x

```console
$ docker pull ruby@sha256:49b48f500f0343ee1e681d1db3b97a41bafce5b55cd9073e0985d60856f8146e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.7 MB (329661911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:669b5c30fb0a625c600d68633d37cead60a0c8c015fb4ac57aa220cafefcb016`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 13 Feb 2024 01:03:43 GMT
ADD file:baaec0dbf612f7bd9d783527a940d73b2148b2ceb1e6770a7be62a51d3bc72e8 in / 
# Tue, 13 Feb 2024 01:03:46 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 02:27:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 02:28:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 02:30:39 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 29 Feb 2024 21:45:14 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Thu, 29 Feb 2024 21:45:14 GMT
ENV LANG=C.UTF-8
# Thu, 29 Feb 2024 21:45:14 GMT
ENV RUBY_VERSION=3.3.0
# Thu, 29 Feb 2024 21:45:14 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.0.tar.xz
# Thu, 29 Feb 2024 21:45:14 GMT
ENV RUBY_DOWNLOAD_SHA256=676b65a36e637e90f982b57b059189b3276b9045034dcd186a7e9078847b975b
# Thu, 29 Feb 2024 21:45:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		wget -O 'arm64-fix.patch' 'https://github.com/ruby/ruby/commit/7f97e3540ce448b501bcbee15afac5f94bb22dd9.patch?full_index=1'; 	echo '86bc65415fd62cb2272a4df249f39fb79db15617ad05c540e05a22f02eae73b3 *arm64-fix.patch' | sha256sum --check --strict; 	patch -p1 -i arm64-fix.patch; 	rm arm64-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 29 Feb 2024 21:45:14 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 29 Feb 2024 21:45:14 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 29 Feb 2024 21:45:14 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Feb 2024 21:45:14 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Thu, 29 Feb 2024 21:45:14 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:75a00755bfcec7b096a7f2fdb8374002f3bbc7076571213a985c40116dbabb6a`  
		Last Modified: Tue, 13 Feb 2024 01:30:37 GMT  
		Size: 53.3 MB (53319325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73b73853a3a5d303ce5a91d0496492ac8084773db71a7ca85f6d20e26005340c`  
		Last Modified: Tue, 13 Feb 2024 02:58:56 GMT  
		Size: 15.6 MB (15641273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cb188cda5ee038922dabb4ba5c3c81be9096f05e1d4d4cdeab23a983e578d77`  
		Last Modified: Tue, 13 Feb 2024 02:59:09 GMT  
		Size: 54.1 MB (54076017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3290768c093f8e148cae12eaffa30fa6cd78ef3fa1c9639c07459aa92948e70`  
		Last Modified: Tue, 13 Feb 2024 02:59:33 GMT  
		Size: 173.0 MB (172970685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f6ae83b6ff51d0505e4aef6e38477aaf80fd55adb1148aef05178c94c5cb4f4`  
		Last Modified: Thu, 15 Feb 2024 17:27:58 GMT  
		Size: 199.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f78bb6f6de7e972020dfe5d042dc2a6edf05ba297aad9caac902069c195a5a88`  
		Last Modified: Thu, 29 Feb 2024 23:11:19 GMT  
		Size: 33.7 MB (33654270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcc4e504d69080437262769f6dff4863c4d94e9f3aa073c2e5f93430ca7be8d7`  
		Last Modified: Thu, 29 Feb 2024 23:11:18 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:bullseye` - unknown; unknown

```console
$ docker pull ruby@sha256:a745b9895610fe42fa8a484c752ab89b0a1c4d68c3e1d4d2f5f7ebab9dd02be8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14939299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daecc51ce883ab00691b9f24891fc348f6e43bb769caab8e6750c0dc733e5706`

```dockerfile
```

-	Layers:
	-	`sha256:4f44a779d5c4d90c56add4cce9986879dfd473c4f3ba758c2a08dbd1fcda6297`  
		Last Modified: Thu, 29 Feb 2024 23:11:19 GMT  
		Size: 14.9 MB (14915884 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99e8c1ba6720fe5cfb015c1ff8386a7cc974a21418cdf2e617725bd5931794e7`  
		Last Modified: Thu, 29 Feb 2024 23:11:18 GMT  
		Size: 23.4 KB (23415 bytes)  
		MIME: application/vnd.in-toto+json
