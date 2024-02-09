## `ruby:bullseye`

```console
$ docker pull ruby@sha256:c90e45dee63a6e88f1a9db1533c8cd538044c3bbf8655043ee647879c9cc7d4a
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
$ docker pull ruby@sha256:34fd87dd7ff4e16d0f833e1afbbdae88d8090bc581ffa75d7d2dbdb4e06e8933
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.6 MB (358644593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7df94ef25923325a529ce493218e29ccdce1e9764f29447447a8eb56e547b72f`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 31 Jan 2024 22:35:29 GMT
ADD file:4fa73c8d113df02c8656b74ab87563432215332f3de78446a02e5ab7d6e2ab7a in / 
# Wed, 31 Jan 2024 22:35:29 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:24:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:24:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:25:29 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 07 Feb 2024 00:26:58 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Wed, 07 Feb 2024 00:26:58 GMT
ENV LANG=C.UTF-8
# Wed, 07 Feb 2024 00:26:58 GMT
ENV RUBY_VERSION=3.3.0
# Wed, 07 Feb 2024 00:26:58 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.0.tar.xz
# Wed, 07 Feb 2024 00:26:58 GMT
ENV RUBY_DOWNLOAD_SHA256=676b65a36e637e90f982b57b059189b3276b9045034dcd186a7e9078847b975b
# Wed, 07 Feb 2024 00:26:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 07 Feb 2024 00:26:58 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 07 Feb 2024 00:26:58 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 07 Feb 2024 00:26:58 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Feb 2024 00:26:58 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Wed, 07 Feb 2024 00:26:58 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:7faaa42ac0c18c9baf539c97a5c8f042d02a77b05380cb57759e4407385710dc`  
		Last Modified: Wed, 31 Jan 2024 22:40:15 GMT  
		Size: 55.1 MB (55056963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1efd1e766326156b6d61b11d929f560cb73024ca0ff2a896b23e8bc6e0044244`  
		Last Modified: Wed, 31 Jan 2024 23:33:27 GMT  
		Size: 15.8 MB (15765028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f124d049a72aebbe5ef2fd589921f51fde08aa5b66cfa8cf81748411af8874dc`  
		Last Modified: Wed, 31 Jan 2024 23:33:44 GMT  
		Size: 54.6 MB (54601507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c200adf1811433c67c208599f5f71578e5237cfd9be60d64045c78282562b77`  
		Last Modified: Wed, 31 Jan 2024 23:34:15 GMT  
		Size: 196.9 MB (196898029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ea7e47d0eecc843d875a9b5e6a0d4bb6e35167cbbb9556c36a54ecf7fe4f735`  
		Last Modified: Wed, 07 Feb 2024 17:55:59 GMT  
		Size: 200.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e493888b8b222855e5386ebe563227a3bc1e1b9648597c9b0532c9b56b99c511`  
		Last Modified: Wed, 07 Feb 2024 17:56:01 GMT  
		Size: 36.3 MB (36322723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da0406e7cbb78d09eb2c9447ccc69212633497a28b01e498219f74db721a7915`  
		Last Modified: Wed, 07 Feb 2024 17:55:59 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:bullseye` - unknown; unknown

```console
$ docker pull ruby@sha256:ac461ae598baf3a1d17760ee239d78b7304ce84fa0bde96c14a6b158c4088ccb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 MB (13095752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07db26b07464f96000f8a69595d3b186acafc1e4be92c91a1345a1314a91224b`

```dockerfile
```

-	Layers:
	-	`sha256:ffcf860e5b7d429aee1cc98697a5ac4b93f03c38f1e6be1fdfc785537564c32f`  
		Last Modified: Wed, 07 Feb 2024 17:56:00 GMT  
		Size: 13.1 MB (13072934 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:232eefb707e7857dc1723c3055a108b7a55f0b61845406bcaed342d33d7e34ae`  
		Last Modified: Wed, 07 Feb 2024 17:55:59 GMT  
		Size: 22.8 KB (22818 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:bullseye` - linux; arm variant v5

```console
$ docker pull ruby@sha256:5b36af6cc0f150a9effe4e9d857ea15b5d6465fa816fa305a5e825ad699c5416
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.8 MB (327779571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21740ea3a62cc37b0dd9036b9ff49d9723c0dc9407753a19c25c9bb0bd7179a3`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:29 GMT
ADD file:b3de5afb7e9c6d6d7f3bca38d87575a8f510b9eb6ee1aca78b37cd5792f6cd3d in / 
# Wed, 31 Jan 2024 22:44:31 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:13:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:13:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:15:49 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 07 Feb 2024 00:26:58 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Wed, 07 Feb 2024 00:26:58 GMT
ENV LANG=C.UTF-8
# Wed, 07 Feb 2024 00:26:58 GMT
ENV RUBY_VERSION=3.3.0
# Wed, 07 Feb 2024 00:26:58 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.0.tar.xz
# Wed, 07 Feb 2024 00:26:58 GMT
ENV RUBY_DOWNLOAD_SHA256=676b65a36e637e90f982b57b059189b3276b9045034dcd186a7e9078847b975b
# Wed, 07 Feb 2024 00:26:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 07 Feb 2024 00:26:58 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 07 Feb 2024 00:26:58 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 07 Feb 2024 00:26:58 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Feb 2024 00:26:58 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Wed, 07 Feb 2024 00:26:58 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:3613d41e91f9f86b71a10338dcfe412e314cd29bee2d9674a0b53f59989b5a42`  
		Last Modified: Wed, 31 Jan 2024 22:48:22 GMT  
		Size: 52.6 MB (52560866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:067da67c4d09fae4c4194d0bf830bc5d88e93cc76d61c68ef8b5cc523864e61d`  
		Last Modified: Wed, 31 Jan 2024 23:23:50 GMT  
		Size: 15.4 MB (15376447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:839390782bb735a0c8ac19a96786946523371bf9a989770a9da6c86ca3583548`  
		Last Modified: Wed, 31 Jan 2024 23:24:12 GMT  
		Size: 52.3 MB (52333517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a64c9eccbd5ac6085a2760b6ef04a0140c0bf1633c08d30c4dacf7544003818`  
		Last Modified: Wed, 31 Jan 2024 23:24:46 GMT  
		Size: 175.1 MB (175124271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7db784d6197be6e1a61c954df23b8c8da9ca25f25acea7f3ef60db5cc69bd26`  
		Last Modified: Thu, 01 Feb 2024 18:24:26 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e42e8f3286149f4307912a86a59b4bd0940769b6e5fbb1ba1f77999b706e1712`  
		Last Modified: Wed, 07 Feb 2024 18:34:04 GMT  
		Size: 32.4 MB (32384130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed58644f5015f19116b1552351d1a3613c172f59c4d16b705cfe24ccaf864ecc`  
		Last Modified: Wed, 07 Feb 2024 18:34:02 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:bullseye` - unknown; unknown

```console
$ docker pull ruby@sha256:c408796ac32c2588b93af3b0cb9674533a06e9291794231b59a993acf5bd83de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.9 MB (12917458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f221261aaee177e093722d1d06406a920d039e7f37614d6f8c1e4f7b035f0ef`

```dockerfile
```

-	Layers:
	-	`sha256:759517192b3dd724eb011e98a79b845016f9764bd77745d431c46186682693f6`  
		Last Modified: Wed, 07 Feb 2024 18:34:03 GMT  
		Size: 12.9 MB (12895207 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2de377e2d80bc0acb854b549c17a8b8d142ebe9987c796d097945165180bf140`  
		Last Modified: Wed, 07 Feb 2024 18:34:02 GMT  
		Size: 22.3 KB (22251 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:bullseye` - linux; arm variant v7

```console
$ docker pull ruby@sha256:27993e7c12b2b6f35a88a6e9bb3a5e6a92c602e2a0cb026b6e98b7b44e997d07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.1 MB (315137558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54288ef63101ce8d6a1973630ffedd2d6e2b00779925ea51c12959950d68463a`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:31 GMT
ADD file:7a3ca444fa582cdedade49cd6262ee982b6da86eafe22b1b77326c8eab3f88cf in / 
# Wed, 31 Jan 2024 22:44:31 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 02:49:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 02:49:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 02:50:16 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 07 Feb 2024 00:26:58 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Wed, 07 Feb 2024 00:26:58 GMT
ENV LANG=C.UTF-8
# Wed, 07 Feb 2024 00:26:58 GMT
ENV RUBY_VERSION=3.3.0
# Wed, 07 Feb 2024 00:26:58 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.0.tar.xz
# Wed, 07 Feb 2024 00:26:58 GMT
ENV RUBY_DOWNLOAD_SHA256=676b65a36e637e90f982b57b059189b3276b9045034dcd186a7e9078847b975b
# Wed, 07 Feb 2024 00:26:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 07 Feb 2024 00:26:58 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 07 Feb 2024 00:26:58 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 07 Feb 2024 00:26:58 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Feb 2024 00:26:58 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Wed, 07 Feb 2024 00:26:58 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:413453d204f637339c7a4727b614537000709bb2ff00a6307e262cf37237761c`  
		Last Modified: Wed, 31 Jan 2024 22:49:12 GMT  
		Size: 50.2 MB (50216178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b1bf41a938a7614b6b4a47164d8e064bbe0014418bfb366d6fac331d52eb271`  
		Last Modified: Thu, 01 Feb 2024 02:59:37 GMT  
		Size: 14.9 MB (14880646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e95de382e9abef96d20556d56d3fb966963ac36ee44cacf79096d796176232c7`  
		Last Modified: Thu, 01 Feb 2024 02:59:54 GMT  
		Size: 50.4 MB (50361245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90bfc3e692e8ff6873d25f44400c58bd3aa6d14344de87d8ad43f17573aaa0cf`  
		Last Modified: Thu, 01 Feb 2024 03:00:28 GMT  
		Size: 167.4 MB (167381508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95a8b120d33157b97a1db43b79f61ae5ee1b41f90bf585ce5bef38b8c42eaa82`  
		Last Modified: Fri, 02 Feb 2024 10:44:42 GMT  
		Size: 200.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8481eae9821b61777a3a29d47b6ead468ffe0286e3ace6a40577b2ebc5575778`  
		Last Modified: Thu, 08 Feb 2024 03:43:43 GMT  
		Size: 32.3 MB (32297637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69964b4d5a641d4daf87d7dee826e48fb2a3867eb8a10d70c4b50d40cf23fecb`  
		Last Modified: Thu, 08 Feb 2024 03:43:41 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:bullseye` - unknown; unknown

```console
$ docker pull ruby@sha256:15d70b031b786453a95f93740bf009f69a7520a56b5c8df9f2f3bdb4d2df17d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.9 MB (12922832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fc1958729a0bbf487cace11d03a10a44546270395e7ec7e23b20a0f73adc8c0`

```dockerfile
```

-	Layers:
	-	`sha256:f27881dd44a66ce8f8d73e48ebbd0cbee0c44448a53d8deddf7474a2f268c8da`  
		Last Modified: Thu, 08 Feb 2024 03:43:42 GMT  
		Size: 12.9 MB (12900581 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f4b55c554538f2717899796ed0013580e1acc6bdc9e264f55b75c79804879af`  
		Last Modified: Thu, 08 Feb 2024 03:43:41 GMT  
		Size: 22.3 KB (22251 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:bullseye` - linux; arm64 variant v8

```console
$ docker pull ruby@sha256:d2bc05df461175d024accf43a3ea822800974dbdb0a4b14d2a770a612556deeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.2 MB (350223231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6616b0eb68ed511d31b77a70edf889e89f752a80cd7387477ce77afe7ad5630c`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:33 GMT
ADD file:81cb49e646b9feb1ddeddea1cb6dbafa672a250f1553cc28eae09c955607236d in / 
# Wed, 31 Jan 2024 22:44:34 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:44:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:44:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:45:33 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 07 Feb 2024 00:26:58 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Wed, 07 Feb 2024 00:26:58 GMT
ENV LANG=C.UTF-8
# Wed, 07 Feb 2024 00:26:58 GMT
ENV RUBY_VERSION=3.3.0
# Wed, 07 Feb 2024 00:26:58 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.0.tar.xz
# Wed, 07 Feb 2024 00:26:58 GMT
ENV RUBY_DOWNLOAD_SHA256=676b65a36e637e90f982b57b059189b3276b9045034dcd186a7e9078847b975b
# Wed, 07 Feb 2024 00:26:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 07 Feb 2024 00:26:58 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 07 Feb 2024 00:26:58 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 07 Feb 2024 00:26:58 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Feb 2024 00:26:58 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Wed, 07 Feb 2024 00:26:58 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:4b6eb2d0256d18652f84fd30c1db34ce9462e535a2d96fbf2f9044db000b13f5`  
		Last Modified: Wed, 31 Jan 2024 22:48:27 GMT  
		Size: 53.7 MB (53708267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a36799ce495b4202a2dd0034c9955834237665bad54a5154faf464f20da7eb84`  
		Last Modified: Wed, 31 Jan 2024 23:53:07 GMT  
		Size: 15.8 MB (15750615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8da2c043d162bc242dc65d025ae4775153d19e07ae75f2d759ab1f51bdefb529`  
		Last Modified: Wed, 31 Jan 2024 23:53:22 GMT  
		Size: 54.7 MB (54699941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:890edf75599fe558c8b1705d12a7ed49aca378c73d11ce7f7d9f59e1fc0e6c90`  
		Last Modified: Wed, 31 Jan 2024 23:53:47 GMT  
		Size: 189.8 MB (189834575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:334a21121cb821e3c5010bf24f8058cb08b2dbfe3c9c192d8efde93ad86b1897`  
		Last Modified: Fri, 02 Feb 2024 18:35:02 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ec626bac12fdd9d2922934947260494e31cfa5ff6b2773742823bd1192633e0`  
		Last Modified: Wed, 07 Feb 2024 18:34:18 GMT  
		Size: 36.2 MB (36229491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a60aca84edd33c71e83bf6ad5ac7c990dab67c7e95e40e7b7099539ee3bdf272`  
		Last Modified: Wed, 07 Feb 2024 18:34:17 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:bullseye` - unknown; unknown

```console
$ docker pull ruby@sha256:2bee04dc90b6e15914eb76b5235087a9355577c2e81487ae64391d39db011178
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 MB (13097459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dba967ad3f4c10d9b77727839299a5869b7a60531027d6f717f30bcf6ef00ec5`

```dockerfile
```

-	Layers:
	-	`sha256:1f243311f5d699fe69c22815af6bdff7097ae5ac545f12e04da4a3f567a22f81`  
		Last Modified: Wed, 07 Feb 2024 18:34:23 GMT  
		Size: 13.1 MB (13075294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a63a018681e0c5ea5c910a0c4bd481c04752675951cd2e792402cceafb2e9a8`  
		Last Modified: Wed, 07 Feb 2024 18:34:17 GMT  
		Size: 22.2 KB (22165 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:bullseye` - linux; 386

```console
$ docker pull ruby@sha256:f12f701b173b12489c643193745169f4e09af4f7ba626951c82c22a4f16e2863
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.5 MB (360452193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e03c0b8831d8ec9dd1a822098e9f4ba1073ea74a0867c3e82895e07507231e89`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 31 Jan 2024 22:39:11 GMT
ADD file:52ba8552e4cd0d950c9eb8ab6bf54413f34e4ef697dc4ae766a04f22b7ea1a38 in / 
# Wed, 31 Jan 2024 22:39:12 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:34:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:34:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:36:27 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 07 Feb 2024 00:26:58 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Wed, 07 Feb 2024 00:26:58 GMT
ENV LANG=C.UTF-8
# Wed, 07 Feb 2024 00:26:58 GMT
ENV RUBY_VERSION=3.3.0
# Wed, 07 Feb 2024 00:26:58 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.0.tar.xz
# Wed, 07 Feb 2024 00:26:58 GMT
ENV RUBY_DOWNLOAD_SHA256=676b65a36e637e90f982b57b059189b3276b9045034dcd186a7e9078847b975b
# Wed, 07 Feb 2024 00:26:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 07 Feb 2024 00:26:58 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 07 Feb 2024 00:26:58 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 07 Feb 2024 00:26:58 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Feb 2024 00:26:58 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Wed, 07 Feb 2024 00:26:58 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:3f04d4a4d4fa39eba128eb2d49424bb31d43a6258c318d2547e85c723fd692f7`  
		Last Modified: Wed, 31 Jan 2024 22:44:11 GMT  
		Size: 56.0 MB (56046343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f99b6c7685036bde084776c74f9136023dec781b8147da8aeefb0986d4f1c1cf`  
		Last Modified: Wed, 31 Jan 2024 23:46:17 GMT  
		Size: 16.3 MB (16269365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52e6e11307bb0bd3d381c7c9caf2866148b59acb310fab1329102bed20a4e04e`  
		Last Modified: Wed, 31 Jan 2024 23:46:37 GMT  
		Size: 55.9 MB (55939864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b16eaec20d2529e6d6598173a9d9d703f940af73aa52ac269cec733301bc178`  
		Last Modified: Wed, 31 Jan 2024 23:47:23 GMT  
		Size: 199.8 MB (199825679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab0581e9efe548972bb9cff96f52775f3b8915191046c8ea734590b95d49437f`  
		Last Modified: Wed, 07 Feb 2024 17:55:39 GMT  
		Size: 201.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e349105a05ef8cd8ac288f258c3992ddf859f0df1131c6ef05a67e44c545bf80`  
		Last Modified: Wed, 07 Feb 2024 17:55:40 GMT  
		Size: 32.4 MB (32370598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e060c212a98d36bb07dc6462c6247078c4b5e866064d3db8748bd77df46e52a9`  
		Last Modified: Wed, 07 Feb 2024 17:55:39 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:bullseye` - unknown; unknown

```console
$ docker pull ruby@sha256:42521593bee232cd14e2d9fcd206939c913bc148c41f20c7b239eccdfa7e65a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 MB (13084656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:535d9724b8a49a164313272b35ed9150a1fdaa770908a2b53d8b667f50dc5cea`

```dockerfile
```

-	Layers:
	-	`sha256:d168501b1592ac8748defe75100d5cf486486fbba865c2cbd438558e3c6fc955`  
		Last Modified: Wed, 07 Feb 2024 17:55:40 GMT  
		Size: 13.1 MB (13061871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:638f96da3653f785e4ec02ab5837281073dc9b2e9791b51798591d8ca86580c6`  
		Last Modified: Wed, 07 Feb 2024 17:55:40 GMT  
		Size: 22.8 KB (22785 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:bullseye` - linux; mips64le

```console
$ docker pull ruby@sha256:a8fd3b2a91feb2027c4cd972ef53bc9bfe49300033ec060dc36b15fc3589e9aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.9 MB (334856789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8429096b23dcffa77f6888aa99ac6afd9fe94f461e76b81a50879a6c02c8269`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 31 Jan 2024 22:27:47 GMT
ADD file:646762dde2578506254f2b52895972c76193565971632fabb304bfd0d84e4301 in / 
# Wed, 31 Jan 2024 22:27:53 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 07:16:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 07:18:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 07:24:11 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 07 Feb 2024 00:26:58 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Wed, 07 Feb 2024 00:26:58 GMT
ENV LANG=C.UTF-8
# Wed, 07 Feb 2024 00:26:58 GMT
ENV RUBY_VERSION=3.3.0
# Wed, 07 Feb 2024 00:26:58 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.0.tar.xz
# Wed, 07 Feb 2024 00:26:58 GMT
ENV RUBY_DOWNLOAD_SHA256=676b65a36e637e90f982b57b059189b3276b9045034dcd186a7e9078847b975b
# Wed, 07 Feb 2024 00:26:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 07 Feb 2024 00:26:58 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 07 Feb 2024 00:26:58 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 07 Feb 2024 00:26:58 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Feb 2024 00:26:58 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Wed, 07 Feb 2024 00:26:58 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:c1282b8885af09f8f21ef0080afd2b77263b28d997ded5c3e116452fb071674d`  
		Last Modified: Wed, 31 Jan 2024 22:39:06 GMT  
		Size: 53.3 MB (53289105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:540709fc3a1629228a5870109f777c55eca65db59573494afa87e285f8cd276a`  
		Last Modified: Thu, 01 Feb 2024 07:48:49 GMT  
		Size: 15.5 MB (15530667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a4d84da99a70f6525286e6829101a8ec425b5bf8fa809b85cfa4e246e0467d2`  
		Last Modified: Thu, 01 Feb 2024 07:49:34 GMT  
		Size: 53.3 MB (53312108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47251fd4f095a1e69c5e1a5af220fd6f5b6f01fbe471939335aa5d4c348cb1de`  
		Last Modified: Thu, 01 Feb 2024 07:51:31 GMT  
		Size: 179.0 MB (179021258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4f7049279c89d1ca67d446caa9523c9904cec19e68c7c9f85bd171e2295bebf`  
		Last Modified: Wed, 07 Feb 2024 18:55:49 GMT  
		Size: 200.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bc46f9bc4e5689acb17e649f68d2deead4da4bcb840f2f2b7c3dcbe30200f71`  
		Last Modified: Wed, 07 Feb 2024 18:55:53 GMT  
		Size: 33.7 MB (33703308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4e7e5a84fe5e79299f760cd6d44de2d418e2202cbfb288dea131b2767faeeb1`  
		Last Modified: Wed, 07 Feb 2024 18:55:49 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:bullseye` - unknown; unknown

```console
$ docker pull ruby@sha256:c57287a4b38da0f2a56f75857bd07d5f3e4813c37233dd37686417ead470f888
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 KB (22666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:849887b62940f8fc261072d9def8907fd0d17548c1726a5e311bf01180e8166b`

```dockerfile
```

-	Layers:
	-	`sha256:47cf96128d955eca1cb65e5d5aa54095e6075a82dead5e395d7b62344b97159d`  
		Last Modified: Wed, 07 Feb 2024 18:55:49 GMT  
		Size: 22.7 KB (22666 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:bullseye` - linux; ppc64le

```console
$ docker pull ruby@sha256:55f32c95e9a372dda20d9d3b3eaa9ca07421b14d267d65450b7c80a354443487
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.9 MB (364909774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3606c48c0c1727f4f74aeb84046edb365da8c6a3e7d4bcb8df1080c06bbf514`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 31 Jan 2024 22:29:53 GMT
ADD file:feff7236892a5ed9be64b73bb7748b1b8017599aad443cae41dfdc07dce2bb8e in / 
# Wed, 31 Jan 2024 22:29:57 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:31:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:31:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:35:30 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 07 Feb 2024 00:26:58 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Wed, 07 Feb 2024 00:26:58 GMT
ENV LANG=C.UTF-8
# Wed, 07 Feb 2024 00:26:58 GMT
ENV RUBY_VERSION=3.3.0
# Wed, 07 Feb 2024 00:26:58 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.0.tar.xz
# Wed, 07 Feb 2024 00:26:58 GMT
ENV RUBY_DOWNLOAD_SHA256=676b65a36e637e90f982b57b059189b3276b9045034dcd186a7e9078847b975b
# Wed, 07 Feb 2024 00:26:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 07 Feb 2024 00:26:58 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 07 Feb 2024 00:26:58 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 07 Feb 2024 00:26:58 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Feb 2024 00:26:58 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Wed, 07 Feb 2024 00:26:58 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:59e847189f64174916c93398cc517f0b07c2a03b89a56fc88a1216415420047a`  
		Last Modified: Wed, 31 Jan 2024 22:34:47 GMT  
		Size: 58.9 MB (58930288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e97e560f4ccece1914eb3223f7f1dd7f1efb3f797d1cf2f2931b1423428b5668`  
		Last Modified: Wed, 31 Jan 2024 23:48:56 GMT  
		Size: 16.8 MB (16767360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8718270d2cbe623b0cb0056d5d433cf38e8ec5f126002f62f67693ef5edb7456`  
		Last Modified: Wed, 31 Jan 2024 23:49:15 GMT  
		Size: 58.9 MB (58874241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8c8fee1359a50ceab803cfc7fbcbdb50e8cb467db6a3203354529949ebe118e`  
		Last Modified: Wed, 31 Jan 2024 23:49:53 GMT  
		Size: 196.3 MB (196277517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdf3105e55956e3803f8e747ca4c62d02d8dffdd6cfbc946c0b0e6f3d134dbfa`  
		Last Modified: Fri, 02 Feb 2024 11:38:58 GMT  
		Size: 199.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff9986a35c124b892adfc789f3f0a76faa7ebf358ff0296b52eee10829179390`  
		Last Modified: Wed, 07 Feb 2024 18:26:28 GMT  
		Size: 34.1 MB (34060025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e18687dbbd6c49a7d8b8510ee7a9eb3f48599e3908dda8f6ddf8b7cc26763c9a`  
		Last Modified: Wed, 07 Feb 2024 18:26:26 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:bullseye` - unknown; unknown

```console
$ docker pull ruby@sha256:ced716ea32da219251a7b9496b5d083af3b06b4daee56377efb6455840302043
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 MB (13070477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9ed6f93614901c9c06b021bfe0f1981767300ee208b2bf9586901ca3551e42d`

```dockerfile
```

-	Layers:
	-	`sha256:068723b2e7f4e33d5bb725a415eff4506f9dbeceabff1be9e4196d0738223702`  
		Last Modified: Wed, 07 Feb 2024 18:26:27 GMT  
		Size: 13.0 MB (13048281 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b68f4c0c6d4951bbe6fe8794ee29d9dfd40771e6ef47544d058625910fd29b4f`  
		Last Modified: Wed, 07 Feb 2024 18:26:26 GMT  
		Size: 22.2 KB (22196 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:bullseye` - linux; s390x

```console
$ docker pull ruby@sha256:2b7176033934f8f1cfdb91b43c9b79dfdee27d75be18553ae21e6051be582175
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.6 MB (329579348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e236d69ac53cffe17cf72b0c16a83da08e528edf4da6530948854aa73176a92f`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 31 Jan 2024 23:00:14 GMT
ADD file:dabd3f74723e205f5c7918d395104495ae736b6dea76f8e097cea5fecfb5afb1 in / 
# Wed, 31 Jan 2024 23:00:18 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 07:27:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 07:29:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 07:33:43 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 07 Feb 2024 00:26:58 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Wed, 07 Feb 2024 00:26:58 GMT
ENV LANG=C.UTF-8
# Wed, 07 Feb 2024 00:26:58 GMT
ENV RUBY_VERSION=3.3.0
# Wed, 07 Feb 2024 00:26:58 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.0.tar.xz
# Wed, 07 Feb 2024 00:26:58 GMT
ENV RUBY_DOWNLOAD_SHA256=676b65a36e637e90f982b57b059189b3276b9045034dcd186a7e9078847b975b
# Wed, 07 Feb 2024 00:26:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 07 Feb 2024 00:26:58 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 07 Feb 2024 00:26:58 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 07 Feb 2024 00:26:58 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Feb 2024 00:26:58 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Wed, 07 Feb 2024 00:26:58 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:7014cd04a53b5809417ad8478246286af7c09e19b05597a0f119e96f7e859b1f`  
		Last Modified: Wed, 31 Jan 2024 23:29:24 GMT  
		Size: 53.3 MB (53294682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f23ecdcf8ccc5ce5336d916683310b1e013c65a510e5e5800558225199775e30`  
		Last Modified: Thu, 01 Feb 2024 08:19:47 GMT  
		Size: 15.6 MB (15643328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33fd27dc397984da98ece9a2d55abf511e61b71edc88c38624d78b7fc0cb773f`  
		Last Modified: Thu, 01 Feb 2024 08:20:18 GMT  
		Size: 54.1 MB (54071240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db0b0db4f23942f60acef6ba1bd97c9d42b0327cd92d6882b65d1dd04594b47d`  
		Last Modified: Thu, 01 Feb 2024 08:20:44 GMT  
		Size: 172.9 MB (172923157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41821e870f158833f0c5d1d958507b5d1dfc2950244fd069a1fb86fe23756edf`  
		Last Modified: Wed, 07 Feb 2024 13:57:36 GMT  
		Size: 200.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b9bc657b1234542e892838e69658a40329a95de84bbf8d67d465881a8a5ed59`  
		Last Modified: Fri, 09 Feb 2024 00:27:53 GMT  
		Size: 33.6 MB (33646598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf685741d29052abd1020cf8295a2f2f3c53cc7d435eb4ea13fcce10f1c16cc9`  
		Last Modified: Fri, 09 Feb 2024 00:27:52 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:bullseye` - unknown; unknown

```console
$ docker pull ruby@sha256:f0feed55a65c4c92751857d2cc2f04510d8689e6f06372cec021373a67bcb3f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.9 MB (12938707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4275ba74b2412c99608db656813998c1f0e205fa3fdeb9760ddc0c3e147ae98e`

```dockerfile
```

-	Layers:
	-	`sha256:372e9a353728b9a147cadad0aa216727448fe82417f41fb6f88eda1751a12588`  
		Last Modified: Fri, 09 Feb 2024 00:27:52 GMT  
		Size: 12.9 MB (12916552 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c46115aee9448d901e2785ac84995093fac586c11c969198a1fb1adc748f2e25`  
		Last Modified: Fri, 09 Feb 2024 00:27:52 GMT  
		Size: 22.2 KB (22155 bytes)  
		MIME: application/vnd.in-toto+json
