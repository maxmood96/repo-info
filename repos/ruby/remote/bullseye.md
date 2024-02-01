## `ruby:bullseye`

```console
$ docker pull ruby@sha256:174e8643e7bcfd40c8e895399a144505a7868bb7e0bd90ff2a41562a22b44b3e
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
$ docker pull ruby@sha256:49dbfc910c14c53f8f834d137997d737a48818fdd9e10eaed044e3207023e204
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.6 MB (358646062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d14826f647f56999c6e822d263e02e6dedaf5481e45070404efd269f3686832`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 26 Dec 2023 18:22:18 GMT
ADD file:4fa73c8d113df02c8656b74ab87563432215332f3de78446a02e5ab7d6e2ab7a in / 
# Tue, 26 Dec 2023 18:22:18 GMT
CMD ["bash"]
# Tue, 26 Dec 2023 18:22:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 26 Dec 2023 18:22:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 26 Dec 2023 18:22:18 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 26 Dec 2023 18:22:18 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Tue, 26 Dec 2023 18:22:18 GMT
ENV LANG=C.UTF-8
# Tue, 26 Dec 2023 18:22:18 GMT
ENV RUBY_VERSION=3.3.0
# Tue, 26 Dec 2023 18:22:18 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.0.tar.xz
# Tue, 26 Dec 2023 18:22:18 GMT
ENV RUBY_DOWNLOAD_SHA256=676b65a36e637e90f982b57b059189b3276b9045034dcd186a7e9078847b975b
# Tue, 26 Dec 2023 18:22:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 26 Dec 2023 18:22:18 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 26 Dec 2023 18:22:18 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 26 Dec 2023 18:22:18 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Dec 2023 18:22:18 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Tue, 26 Dec 2023 18:22:18 GMT
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
	-	`sha256:d455b9a88e270effd7dae3d77ae8e7cd6d73201f5184f55471f23ed50a0540de`  
		Last Modified: Thu, 01 Feb 2024 00:09:36 GMT  
		Size: 199.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ae3f0de16572400634c126d4cd0932481940ff94788fd5e23c7a8bb58801486`  
		Last Modified: Thu, 01 Feb 2024 00:09:37 GMT  
		Size: 36.3 MB (36324194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b6285ee032ed0f6c2c20954dc4f0ba51a3cfea6d16944965b37370cec541fc3`  
		Last Modified: Thu, 01 Feb 2024 00:09:36 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:bullseye` - unknown; unknown

```console
$ docker pull ruby@sha256:f2a208761e01685014f7929989cf2c883e6d31bab9637eccaa239d33af010035
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 MB (13067561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2734676c47ef663a36d5bd1397835e5873ed5390fe552adc798662c4e54606c4`

```dockerfile
```

-	Layers:
	-	`sha256:57d19c818b496d7ca7d4ef214871b8f31ded94ad4001fec806e35c8f3938cd25`  
		Last Modified: Thu, 01 Feb 2024 00:09:36 GMT  
		Size: 13.0 MB (13044679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d228e3953463d0dfbb18c68da65f9aaf2f5db49b3c9b44c2338c3366e9f8b287`  
		Last Modified: Thu, 01 Feb 2024 00:09:35 GMT  
		Size: 22.9 KB (22882 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:bullseye` - linux; arm variant v5

```console
$ docker pull ruby@sha256:61cd1caaef68dd579a8d464ad57ae433883ed59998b48d8d3bbe8f475eba3c07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.8 MB (327780363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a0e3b124219368ba00ba8295af5a28fefd776d102d78999b679c10def3342aa`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 26 Dec 2023 18:22:18 GMT
ADD file:b3de5afb7e9c6d6d7f3bca38d87575a8f510b9eb6ee1aca78b37cd5792f6cd3d in / 
# Tue, 26 Dec 2023 18:22:18 GMT
CMD ["bash"]
# Tue, 26 Dec 2023 18:22:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 26 Dec 2023 18:22:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 26 Dec 2023 18:22:18 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 26 Dec 2023 18:22:18 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Tue, 26 Dec 2023 18:22:18 GMT
ENV LANG=C.UTF-8
# Tue, 26 Dec 2023 18:22:18 GMT
ENV RUBY_VERSION=3.3.0
# Tue, 26 Dec 2023 18:22:18 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.0.tar.xz
# Tue, 26 Dec 2023 18:22:18 GMT
ENV RUBY_DOWNLOAD_SHA256=676b65a36e637e90f982b57b059189b3276b9045034dcd186a7e9078847b975b
# Tue, 26 Dec 2023 18:22:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 26 Dec 2023 18:22:18 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 26 Dec 2023 18:22:18 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 26 Dec 2023 18:22:18 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Dec 2023 18:22:18 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Tue, 26 Dec 2023 18:22:18 GMT
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
	-	`sha256:a9e4e9444260d3453727d55e590975e014af2e9119d4212b905317d49e6fd17a`  
		Last Modified: Thu, 01 Feb 2024 18:24:27 GMT  
		Size: 32.4 MB (32384921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07dd4023385872e33c1e29d0509617edf0b0ea9358092058d38d65fca0e50035`  
		Last Modified: Thu, 01 Feb 2024 18:24:26 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:bullseye` - unknown; unknown

```console
$ docker pull ruby@sha256:9c6470b1168b761cc322b30157bd3d12118595a8696f7f2bc5c33f0052bc9684
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.9 MB (12889267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71b4ce09ea951c329a4ab9e7cddc13f94236a6ef626a38790dc90e37eb4dfabd`

```dockerfile
```

-	Layers:
	-	`sha256:017ba9c84b67cce3abc50b04e923ff1828ef73dd5e71500b45b18f05eb0d737a`  
		Last Modified: Thu, 01 Feb 2024 18:24:27 GMT  
		Size: 12.9 MB (12866952 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15427a1e527b66f393079aef7342c3bbda615a4b706931868b002f894c49fcf0`  
		Last Modified: Thu, 01 Feb 2024 18:24:26 GMT  
		Size: 22.3 KB (22315 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:bullseye` - linux; arm variant v7

```console
$ docker pull ruby@sha256:507ab3c01139bb79e1eaf8ea033755aa975d59f2eada108f9e62b2a7824ec76e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.1 MB (315139153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1aae70c922fb04f1216fb4f02386667b1cb17cff2db1494db80a073a4b3e66b3`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 26 Dec 2023 18:22:18 GMT
ADD file:06c355196a858f2594c761bea3314e053018c78a4b06eabe168db940f6c18e26 in / 
# Tue, 26 Dec 2023 18:22:18 GMT
CMD ["bash"]
# Tue, 26 Dec 2023 18:22:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 26 Dec 2023 18:22:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 26 Dec 2023 18:22:18 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 26 Dec 2023 18:22:18 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Tue, 26 Dec 2023 18:22:18 GMT
ENV LANG=C.UTF-8
# Tue, 26 Dec 2023 18:22:18 GMT
ENV RUBY_VERSION=3.3.0
# Tue, 26 Dec 2023 18:22:18 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.0.tar.xz
# Tue, 26 Dec 2023 18:22:18 GMT
ENV RUBY_DOWNLOAD_SHA256=676b65a36e637e90f982b57b059189b3276b9045034dcd186a7e9078847b975b
# Tue, 26 Dec 2023 18:22:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 26 Dec 2023 18:22:18 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 26 Dec 2023 18:22:18 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 26 Dec 2023 18:22:18 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Dec 2023 18:22:18 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Tue, 26 Dec 2023 18:22:18 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:6c8fc6a3ed50d9d1c829e556b5efd4ca23cd5d51d5dcdec2a7a70b583673ef89`  
		Last Modified: Thu, 11 Jan 2024 02:49:02 GMT  
		Size: 50.2 MB (50215530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc92f863388ea7a660a09ac1581e426ed098ac1fe970d4ad13e7ac5a7d728ee3`  
		Last Modified: Thu, 11 Jan 2024 03:30:20 GMT  
		Size: 14.9 MB (14880496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a45ae6e4109fcb63cfd59b29d1bc073059fb189aecab8d10de1468ec026aeae`  
		Last Modified: Wed, 17 Jan 2024 02:20:03 GMT  
		Size: 50.4 MB (50361413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c23fb1c630ad99b41c55ffc45c51811221b308683a461f9615d0788e64f9b9a`  
		Last Modified: Wed, 17 Jan 2024 02:20:44 GMT  
		Size: 167.4 MB (167381995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c815af1b7b89b9de21b3691ebf9079b944e7c8b293a5b08d6a35da8e5da1ddc3`  
		Last Modified: Thu, 18 Jan 2024 11:48:29 GMT  
		Size: 199.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5ce0b308d7edfd2d047ecee30b0557cffce636f015c2fa1c73ac9b3a2681210`  
		Last Modified: Thu, 18 Jan 2024 11:48:30 GMT  
		Size: 32.3 MB (32299376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36d688bbf04f51842043553650c7455bb9a124f745d6508d74d7d206e1aabbbd`  
		Last Modified: Thu, 18 Jan 2024 11:48:29 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:bullseye` - unknown; unknown

```console
$ docker pull ruby@sha256:8bbc4d2935164ea1d947d58cfa0f103327beb772bbbb9d83894afeddee3a5eed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.9 MB (12894641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1cb0eaafc4f64ecae7f1a5b4df450cf69eb094c00465e12505eec486686319a`

```dockerfile
```

-	Layers:
	-	`sha256:60becae28e920a5980b9181dd67ac9dfc2e7335c6b0e09eac4d35d458386232b`  
		Last Modified: Thu, 18 Jan 2024 11:48:30 GMT  
		Size: 12.9 MB (12872326 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12d9efac75e4fd984cddd5b35ca24be42a554bbefbe3210d13461eca32406092`  
		Last Modified: Thu, 18 Jan 2024 11:48:29 GMT  
		Size: 22.3 KB (22315 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:bullseye` - linux; arm64 variant v8

```console
$ docker pull ruby@sha256:591164d803aa547ab0d5496dcda4430320093bafa549d2745561c629462e4a59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.2 MB (350224081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13b72bdd03f42fa3d7f0efc711810d44347372eb4524919654bef394c6c28380`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 26 Dec 2023 18:22:18 GMT
ADD file:8fb65cadfd211811589ee046d0fbd69d1fe11461b0c0c154a7650bf97307b857 in / 
# Tue, 26 Dec 2023 18:22:18 GMT
CMD ["bash"]
# Tue, 26 Dec 2023 18:22:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 26 Dec 2023 18:22:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 26 Dec 2023 18:22:18 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 26 Dec 2023 18:22:18 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Tue, 26 Dec 2023 18:22:18 GMT
ENV LANG=C.UTF-8
# Tue, 26 Dec 2023 18:22:18 GMT
ENV RUBY_VERSION=3.3.0
# Tue, 26 Dec 2023 18:22:18 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.0.tar.xz
# Tue, 26 Dec 2023 18:22:18 GMT
ENV RUBY_DOWNLOAD_SHA256=676b65a36e637e90f982b57b059189b3276b9045034dcd186a7e9078847b975b
# Tue, 26 Dec 2023 18:22:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 26 Dec 2023 18:22:18 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 26 Dec 2023 18:22:18 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 26 Dec 2023 18:22:18 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Dec 2023 18:22:18 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Tue, 26 Dec 2023 18:22:18 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:cf83973c4a096cce9f37c421ad6f19cf1ebf7ae4d8ea98dac4913bd2aef08d1c`  
		Last Modified: Thu, 11 Jan 2024 02:44:25 GMT  
		Size: 53.7 MB (53707847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aebf2a961043d6b9dd703d0a485e216a2e302edf2e2525f7f410987d26905e71`  
		Last Modified: Thu, 11 Jan 2024 09:35:03 GMT  
		Size: 15.8 MB (15750711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:646806c0e22a1bfa60edc42bcc6170f0ccd02431e5871b9cec1962c34d610232`  
		Last Modified: Wed, 17 Jan 2024 02:59:33 GMT  
		Size: 54.7 MB (54699826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cd94a910a6d687fc7621b3af4657f78c1208a07fa463f30e2ed002dadb7e021`  
		Last Modified: Wed, 17 Jan 2024 03:00:10 GMT  
		Size: 189.8 MB (189834377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0bf3d2e988601e8f11bc9f971677053020a4526526eabc487c0d9ac4e2ddc5b`  
		Last Modified: Thu, 18 Jan 2024 08:17:00 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6e6266073c9848e57e7d3b1d454fb556da72525239100e6a311acccb48eb6dc`  
		Last Modified: Thu, 18 Jan 2024 08:17:01 GMT  
		Size: 36.2 MB (36230979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67e1c6320d6d56b8ec81ac6269ba1b913050d0297190f6581abe446c41a5da13`  
		Last Modified: Thu, 18 Jan 2024 08:17:00 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:bullseye` - unknown; unknown

```console
$ docker pull ruby@sha256:fefe750742c3c1970b73fb7dda5f64075d2f77e10ae22dc77986f8d70b12f705
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 MB (13069267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:061236e18652547a40f58444f3600773c6f81f9455ab89234bed9c2bc68f9a60`

```dockerfile
```

-	Layers:
	-	`sha256:400ea3ab5e416292c6145ffb966948a0f88053394cfce361b92c9c84f0c5714f`  
		Last Modified: Thu, 18 Jan 2024 08:17:01 GMT  
		Size: 13.0 MB (13047039 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ecdd6daf99cd8d4c73d01baee3ae39b251e1dc93eca2ac56bd72323058ddf916`  
		Last Modified: Thu, 18 Jan 2024 08:17:00 GMT  
		Size: 22.2 KB (22228 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:bullseye` - linux; 386

```console
$ docker pull ruby@sha256:d8043d3bdaf2b811828e34b315f5994983f5be625edb7f40f9de0f1bf6f556ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.5 MB (360454215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6982ab690d8601642165320b673d180d4e3e35d4d59d32fe453b167dec57d615`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 26 Dec 2023 18:22:18 GMT
ADD file:52ba8552e4cd0d950c9eb8ab6bf54413f34e4ef697dc4ae766a04f22b7ea1a38 in / 
# Tue, 26 Dec 2023 18:22:18 GMT
CMD ["bash"]
# Tue, 26 Dec 2023 18:22:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 26 Dec 2023 18:22:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 26 Dec 2023 18:22:18 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 26 Dec 2023 18:22:18 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Tue, 26 Dec 2023 18:22:18 GMT
ENV LANG=C.UTF-8
# Tue, 26 Dec 2023 18:22:18 GMT
ENV RUBY_VERSION=3.3.0
# Tue, 26 Dec 2023 18:22:18 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.0.tar.xz
# Tue, 26 Dec 2023 18:22:18 GMT
ENV RUBY_DOWNLOAD_SHA256=676b65a36e637e90f982b57b059189b3276b9045034dcd186a7e9078847b975b
# Tue, 26 Dec 2023 18:22:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 26 Dec 2023 18:22:18 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 26 Dec 2023 18:22:18 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 26 Dec 2023 18:22:18 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Dec 2023 18:22:18 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Tue, 26 Dec 2023 18:22:18 GMT
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
	-	`sha256:a48559ea604794cc5f15ce1ff7c6dd043feea70bafd01580a2fff6840553d87c`  
		Last Modified: Thu, 01 Feb 2024 01:01:15 GMT  
		Size: 200.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:014a4709b2cb9dcf66e79c82e346d2f0201087d0ed7ab6ff98f8e19d0a0f3f10`  
		Last Modified: Thu, 01 Feb 2024 01:01:25 GMT  
		Size: 32.4 MB (32372623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ed0678c866a10ffdae108668570a614c6f6935033578e0db4b26f22a61af1e`  
		Last Modified: Thu, 01 Feb 2024 01:01:24 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:bullseye` - unknown; unknown

```console
$ docker pull ruby@sha256:4086539b774e66fc651e2224567299be3b084b7456e32eace881e0740bbf9e72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 MB (13056465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:029a8a8042992193d5391c86c07c254c75e63a7a1bf0f55e10295df03344cb34`

```dockerfile
```

-	Layers:
	-	`sha256:13ed120b9656b8b45be370a38849e28e438debd7c8ca1afa6ef68dd0f6ba326f`  
		Last Modified: Thu, 01 Feb 2024 01:01:24 GMT  
		Size: 13.0 MB (13033616 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a1f167c6e2367f3834880d8b1bea33f892f203b60f23863732accfc13b5164d`  
		Last Modified: Thu, 01 Feb 2024 01:01:24 GMT  
		Size: 22.8 KB (22849 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:bullseye` - linux; mips64le

```console
$ docker pull ruby@sha256:ca014eacc799e6f0e0938d28c25f5ec9662988239f3edf6b8654390588b4afa4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.9 MB (334858163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84acc1b731f6f99d02e4efc308a5ac550ca9b10a3bfc14eeb862196e959e9edc`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 26 Dec 2023 18:22:18 GMT
ADD file:624f588d8cd5ac8189fd789968263b87196e86dd1d90debb6c5261b515ce80a4 in / 
# Tue, 26 Dec 2023 18:22:18 GMT
CMD ["bash"]
# Tue, 26 Dec 2023 18:22:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 26 Dec 2023 18:22:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 26 Dec 2023 18:22:18 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 26 Dec 2023 18:22:18 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Tue, 26 Dec 2023 18:22:18 GMT
ENV LANG=C.UTF-8
# Tue, 26 Dec 2023 18:22:18 GMT
ENV RUBY_VERSION=3.3.0
# Tue, 26 Dec 2023 18:22:18 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.0.tar.xz
# Tue, 26 Dec 2023 18:22:18 GMT
ENV RUBY_DOWNLOAD_SHA256=676b65a36e637e90f982b57b059189b3276b9045034dcd186a7e9078847b975b
# Tue, 26 Dec 2023 18:22:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 26 Dec 2023 18:22:18 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 26 Dec 2023 18:22:18 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 26 Dec 2023 18:22:18 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Dec 2023 18:22:18 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Tue, 26 Dec 2023 18:22:18 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:80f37a7fb2daee9d24c2a15489b4104fd20747297db13799a90f5f67e3a79154`  
		Last Modified: Thu, 11 Jan 2024 02:23:35 GMT  
		Size: 53.3 MB (53288875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:533b4dc197845232bb31ea262c56891dac2feed854c3f09a70f819ec88464da5`  
		Last Modified: Thu, 11 Jan 2024 03:27:38 GMT  
		Size: 15.5 MB (15530460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79df6684e42e6c10044d92cf112f4ce85d38191e76029bbd3b653af7973f1cc2`  
		Last Modified: Wed, 17 Jan 2024 02:51:07 GMT  
		Size: 53.3 MB (53311880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae916a756b80f0c87e4fad3dddc330425876b82f662496c6b17c205cbac40a22`  
		Last Modified: Wed, 17 Jan 2024 02:53:14 GMT  
		Size: 179.0 MB (179020983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f841f00ccdbcd22b3729133a565b856852d9d7840367b2d7b2cfd8ff32c7ebc2`  
		Last Modified: Wed, 17 Jan 2024 13:41:43 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d2ebb67c31c1e7d5d99c86fb227f521263192e265cd2e475c20bb1b5f8dfb65`  
		Last Modified: Wed, 17 Jan 2024 13:41:46 GMT  
		Size: 33.7 MB (33705623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e86313ffae093a23fd714460e1d561df20b599d9fa76d4aef6dcf0737997ca07`  
		Last Modified: Wed, 17 Jan 2024 13:41:43 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:bullseye` - unknown; unknown

```console
$ docker pull ruby@sha256:5950c8fdec60738ceb96be540c5b42254f42e8634380bf424d26df1ff34eae8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.1 KB (22066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1293d7af3a373fe70d4ca32b2df1d99039e1f15d3154e7a6907ec41ba3a5365`

```dockerfile
```

-	Layers:
	-	`sha256:ca503705d3b2f54fa8ccd380f536e4f700623e72fbbcada1516b4343eeb16b6b`  
		Last Modified: Wed, 17 Jan 2024 13:41:43 GMT  
		Size: 22.1 KB (22066 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:bullseye` - linux; ppc64le

```console
$ docker pull ruby@sha256:e062d0f256109730f0664b775ef464685deb99546a79189dc8512ba5f503d595
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.9 MB (364910740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6081e8cbdde5fac2a997188b58db0dc498e89300f2d6c51ef1e5b3fc0cfb537d`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 26 Dec 2023 18:22:18 GMT
ADD file:cb900134161e1d051fb57c4a488efa9478959953f2773baa8a90b13198589a81 in / 
# Tue, 26 Dec 2023 18:22:18 GMT
CMD ["bash"]
# Tue, 26 Dec 2023 18:22:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 26 Dec 2023 18:22:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 26 Dec 2023 18:22:18 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 26 Dec 2023 18:22:18 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Tue, 26 Dec 2023 18:22:18 GMT
ENV LANG=C.UTF-8
# Tue, 26 Dec 2023 18:22:18 GMT
ENV RUBY_VERSION=3.3.0
# Tue, 26 Dec 2023 18:22:18 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.0.tar.xz
# Tue, 26 Dec 2023 18:22:18 GMT
ENV RUBY_DOWNLOAD_SHA256=676b65a36e637e90f982b57b059189b3276b9045034dcd186a7e9078847b975b
# Tue, 26 Dec 2023 18:22:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 26 Dec 2023 18:22:18 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 26 Dec 2023 18:22:18 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 26 Dec 2023 18:22:18 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Dec 2023 18:22:18 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Tue, 26 Dec 2023 18:22:18 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:1b9340c192fedc0211d4cda28f7a01e9ff3be108c42783e576f4a366c373f30b`  
		Last Modified: Thu, 11 Jan 2024 02:39:48 GMT  
		Size: 58.9 MB (58929662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:764e705cb61758280364899cd162b2510b2a119833c02f501318b83950af12d2`  
		Last Modified: Thu, 11 Jan 2024 07:24:33 GMT  
		Size: 16.8 MB (16767158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:145205e451151b6f00222d734b41542a45ff000be2156f6dbce151466b7f0645`  
		Last Modified: Wed, 17 Jan 2024 03:25:51 GMT  
		Size: 58.9 MB (58874243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1556eebd2a6ebc2c0ceb94060d683a42d2497130a1a12ddf85649f866bab40f8`  
		Last Modified: Wed, 17 Jan 2024 03:26:27 GMT  
		Size: 196.3 MB (196277746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:622e13715b39ceb861a0304e7cb7dd3b6ac97f9e89be604c5057b69e7a073aa0`  
		Last Modified: Wed, 17 Jan 2024 19:52:52 GMT  
		Size: 199.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78e70968b75f0576d4f4ae2ad730aad4b32f000c3fd40828ae4277d9c4d63663`  
		Last Modified: Wed, 17 Jan 2024 19:52:53 GMT  
		Size: 34.1 MB (34061588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37d0c7484555c3ea493a0be0b1190821396887a52396fadea971c4ce33adf0c7`  
		Last Modified: Wed, 17 Jan 2024 19:52:52 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:bullseye` - unknown; unknown

```console
$ docker pull ruby@sha256:c97e63947049db54bcdac9c6058aac3eda6dc7f644fc1160c94de4c8fbb22807
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.0 MB (13042287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78fc1041036135e4592a2a38f49575388afd53dab3b961db19785d0eccd23da3`

```dockerfile
```

-	Layers:
	-	`sha256:38302be22ebff496eb40d82d99bec7b27dfb69120d4cc0c294856ac4d90db617`  
		Last Modified: Wed, 17 Jan 2024 19:52:52 GMT  
		Size: 13.0 MB (13020026 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17dfc0a1c2f7d06ff1d026925fc8aabe5b53670866263015be5391a086178036`  
		Last Modified: Wed, 17 Jan 2024 19:52:52 GMT  
		Size: 22.3 KB (22261 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:bullseye` - linux; s390x

```console
$ docker pull ruby@sha256:e69d3db29291ecb63ec92d81fcf24c3ce4c7ced7d17e3c6f363496d5c85b7288
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.6 MB (329576694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bc65987c580760d5f4861c4b8781cfb06bc4463c0dc7917a3193ab3ae02b8f9`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 26 Dec 2023 18:22:18 GMT
ADD file:9ddcb5238e539e3b1fd8032aecf5e40f0b8b8162e6d045fcd58520db01e93296 in / 
# Tue, 26 Dec 2023 18:22:18 GMT
CMD ["bash"]
# Tue, 26 Dec 2023 18:22:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 26 Dec 2023 18:22:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 26 Dec 2023 18:22:18 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 26 Dec 2023 18:22:18 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Tue, 26 Dec 2023 18:22:18 GMT
ENV LANG=C.UTF-8
# Tue, 26 Dec 2023 18:22:18 GMT
ENV RUBY_VERSION=3.3.0
# Tue, 26 Dec 2023 18:22:18 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.0.tar.xz
# Tue, 26 Dec 2023 18:22:18 GMT
ENV RUBY_DOWNLOAD_SHA256=676b65a36e637e90f982b57b059189b3276b9045034dcd186a7e9078847b975b
# Tue, 26 Dec 2023 18:22:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 26 Dec 2023 18:22:18 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 26 Dec 2023 18:22:18 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 26 Dec 2023 18:22:18 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Dec 2023 18:22:18 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Tue, 26 Dec 2023 18:22:18 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:a1442bb0c8abfd050e8bdb2270126c2f24402a8c57a00f8229c40c2a35253665`  
		Last Modified: Thu, 11 Jan 2024 01:51:04 GMT  
		Size: 53.3 MB (53296125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1d30f97393df8af87413ca6aa015986e13ab489522ffe9a065961b2ed0f9352`  
		Last Modified: Thu, 11 Jan 2024 02:22:01 GMT  
		Size: 15.6 MB (15642723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59822891147cf801aabc1a3824089c8385793e177e1610b0c14dfb8ccafc4934`  
		Last Modified: Wed, 17 Jan 2024 04:04:21 GMT  
		Size: 54.1 MB (54070709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:515d393636eb45ce9c7153873b9a523d1c13aae090017d8089b56b8da8e16645`  
		Last Modified: Wed, 17 Jan 2024 04:04:47 GMT  
		Size: 172.9 MB (172919632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a04bd9de7d588feb396b224da99b645e1a6a08e36c49f3a6b0276c04a015431`  
		Last Modified: Sat, 20 Jan 2024 15:18:16 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45dd368206fe71856e9a47630e3bc6321cd1b5fe232f7056d2e70c00287ca1fd`  
		Last Modified: Sat, 20 Jan 2024 15:18:18 GMT  
		Size: 33.6 MB (33647163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91ceba490b644c9159e2bca1d5f5794484d7abe5e6f08ed727c45e6de5408390`  
		Last Modified: Sat, 20 Jan 2024 15:18:16 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:bullseye` - unknown; unknown

```console
$ docker pull ruby@sha256:6cdbf8936700ccbda8f472f26c52667b2aa91bdec98e026fd4e277816591e4b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.9 MB (12910516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e7d0e6acd24c340104a9ff337e2b4f8f9ef0c06caf6b402045b95469f208d34`

```dockerfile
```

-	Layers:
	-	`sha256:ba36072cfc759ef0780c37ea45e6097d71ce85b6ca92acac0949e2f13f74e244`  
		Last Modified: Sat, 20 Jan 2024 15:18:16 GMT  
		Size: 12.9 MB (12888297 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37fe11831f8c9d5f32e3caf394323800eb1efab76a21fca008accf0a27febf51`  
		Last Modified: Sat, 20 Jan 2024 15:18:16 GMT  
		Size: 22.2 KB (22219 bytes)  
		MIME: application/vnd.in-toto+json
