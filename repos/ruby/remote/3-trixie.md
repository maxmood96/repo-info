## `ruby:3-trixie`

```console
$ docker pull ruby@sha256:faa69a72b244dc1a28c308f0ae273746063a0a63aff688a8dc246d9f0772e131
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
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `ruby:3-trixie` - linux; amd64

```console
$ docker pull ruby@sha256:a8b4ece4685543eaff90b78e0bbab11dbbd8dac076f60fc2f84f940a27405a34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **421.1 MB (421078523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80a4a8eaed3ecf05cb39280a0c82ad389fb1ffbd23408a147176319a81160e70`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:40:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 20:26:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 21:18:02 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 22:44:48 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 08 May 2026 22:46:39 GMT
ENV LANG=C.UTF-8
# Fri, 08 May 2026 22:46:39 GMT
ENV RUBY_VERSION=3.4.9
# Fri, 08 May 2026 22:46:39 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Fri, 08 May 2026 22:46:39 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Fri, 08 May 2026 22:46:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 08 May 2026 22:46:39 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 08 May 2026 22:46:39 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 08 May 2026 22:46:39 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 22:46:39 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 08 May 2026 22:46:39 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:307f8152a55ef1e9eeb1acbbee7bc81232615329eaeb00d8dd93b46be297f34c`  
		Last Modified: Fri, 08 May 2026 18:24:07 GMT  
		Size: 49.3 MB (49302320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caf6c0a95e34418907d5abfe604d08c5cc6bf9d689943856fcd842eb2be82c6c`  
		Last Modified: Fri, 08 May 2026 19:40:57 GMT  
		Size: 25.6 MB (25623106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82a92b93bf7181c9d6b4525236a1a2fec85dc591d4deee481e828e707853f42c`  
		Last Modified: Fri, 08 May 2026 20:27:02 GMT  
		Size: 67.8 MB (67789206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5470790761244112ed0b9ea9218282e5185dc7fd1e91840e855a32550e2ecd73`  
		Last Modified: Fri, 08 May 2026 21:18:48 GMT  
		Size: 236.1 MB (236145627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e3fa955a2839c24f5fcde683e56e0d615591e01e96f525e35ba5f3c8302881c`  
		Last Modified: Fri, 08 May 2026 22:46:57 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d543e56dbe64cde300e7f797935398e01dada98a53f91c26b9b8dd5913f06021`  
		Last Modified: Fri, 08 May 2026 22:46:59 GMT  
		Size: 42.2 MB (42217931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d37cc22e4b28b6ef16e07fcf64c6a622dc78cba1f0194259bc5dabecfa298b2`  
		Last Modified: Fri, 08 May 2026 22:46:57 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-trixie` - unknown; unknown

```console
$ docker pull ruby@sha256:78ff42a894db08b5754c198ea30f1339e4f8c40a06cd3cdff654e306f8785a5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17349063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d01aa49f8c185ec7685cb6ab135f555f7fb4bfa0cf11c58c6c160f31571ec3ca`

```dockerfile
```

-	Layers:
	-	`sha256:3154916ea9686240b69c609fc83a6d4327d12e8c5b683d9e24b6664b63260b2e`  
		Last Modified: Fri, 08 May 2026 22:46:58 GMT  
		Size: 17.3 MB (17326736 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80c481a4c34f585cd192fbc688a448b70703b3639d6f548149929dbaae444f2f`  
		Last Modified: Fri, 08 May 2026 22:46:57 GMT  
		Size: 22.3 KB (22327 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-trixie` - linux; arm variant v5

```console
$ docker pull ruby@sha256:14cb19ea71e8e139eb84819f364609384ee91d897e9727bfc355fddc868d94d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **381.0 MB (381034631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79f42dfc7b6da2ad3f0283cb81a0c8dc4d8d480a9fd29d600ca664647c068230`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 20:57:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 21:56:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 22:13:16 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 22:52:28 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 08 May 2026 22:54:59 GMT
ENV LANG=C.UTF-8
# Fri, 08 May 2026 22:54:59 GMT
ENV RUBY_VERSION=3.4.9
# Fri, 08 May 2026 22:54:59 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Fri, 08 May 2026 22:54:59 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Fri, 08 May 2026 22:54:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 08 May 2026 22:54:59 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 08 May 2026 22:54:59 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 08 May 2026 22:54:59 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 22:54:59 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 08 May 2026 22:54:59 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:ab1ea4901b2e5ef4c23bc85e77bccd29b5e37409a6599c547024038487caa48a`  
		Last Modified: Fri, 08 May 2026 18:33:49 GMT  
		Size: 47.5 MB (47466292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2782236aac3a37777665c4737690456903e8f45d5d8a06d88dfd8fdb29da5876`  
		Last Modified: Fri, 08 May 2026 20:57:34 GMT  
		Size: 24.4 MB (24363654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:768a28224fae77f3965cdd69933693d2e36af26e730f0f75e576bd8b5e516d41`  
		Last Modified: Fri, 08 May 2026 21:56:37 GMT  
		Size: 65.3 MB (65318209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac2b43951eb50fbbec798a98a0d5e3979bc819241fd4dcdb56f1db4886771d88`  
		Last Modified: Fri, 08 May 2026 22:13:57 GMT  
		Size: 205.9 MB (205853310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dd0235cf7c3689a65939d6b76e60a1fe96fe43175fdfa8453145c9086886ecb`  
		Last Modified: Fri, 08 May 2026 22:55:19 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d171f25c0282da3c96e2d4f2976c87e6977c874b476854a7d20fbab293e0c4ef`  
		Last Modified: Fri, 08 May 2026 22:55:20 GMT  
		Size: 38.0 MB (38032832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2feafe551773c0bc52e06e977d4ffb87c3fee9980f0e94d9c0ea80f933656a95`  
		Last Modified: Fri, 08 May 2026 22:55:19 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-trixie` - unknown; unknown

```console
$ docker pull ruby@sha256:ad199ce3fe571503556f38c3e05a18481cac325561f77f841f5e01c578ed8aee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17111408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5aafa3f4c92beba2edcbdcbe8d39fd9e051a7f577beb09ea42386a2ca67c9b3`

```dockerfile
```

-	Layers:
	-	`sha256:1ed0373e6d2fcf715a33ec844217d5aba50488b7701cf4ec0543a522ba4131a2`  
		Last Modified: Fri, 08 May 2026 22:55:20 GMT  
		Size: 17.1 MB (17088958 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34ab862421eaf8f5e2f38ea4dc357753acfe35522719817e86c1c7f02c248738`  
		Last Modified: Fri, 08 May 2026 22:55:19 GMT  
		Size: 22.4 KB (22450 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-trixie` - linux; arm variant v7

```console
$ docker pull ruby@sha256:735743f15230b04856aee2b816ac344d244fdc402044f48f88e3a5de9fe52a14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.5 MB (363456677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bed20bd8ae70f6b6829558364c56c65f3a865aa670e92018dcb86b364cde7392`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:44:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 21:35:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 22:13:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 23:47:43 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 08 May 2026 23:49:58 GMT
ENV LANG=C.UTF-8
# Fri, 08 May 2026 23:49:58 GMT
ENV RUBY_VERSION=3.4.9
# Fri, 08 May 2026 23:49:58 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Fri, 08 May 2026 23:49:58 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Fri, 08 May 2026 23:49:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 08 May 2026 23:49:58 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 08 May 2026 23:49:58 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 08 May 2026 23:49:58 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 23:49:58 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 08 May 2026 23:49:58 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:54e91da80876b5fdcd3d8cbdf1cebc52bdf513f8a587b419fa82f5fb473a2b30`  
		Last Modified: Fri, 08 May 2026 18:37:56 GMT  
		Size: 45.7 MB (45738425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa31143502952cbe5df185dc297d98ec2482b596177bb3d2884695855e7091f1`  
		Last Modified: Fri, 08 May 2026 19:45:06 GMT  
		Size: 23.6 MB (23636413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb6753753dc173af6d2d0689a1eccd6337abda3fd742e649454b834a7d6c6afc`  
		Last Modified: Fri, 08 May 2026 21:35:45 GMT  
		Size: 62.7 MB (62728028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42c66f6797abbefc309d6193205f793cea64fedf67e46f6f6933d96ecdcb0436`  
		Last Modified: Fri, 08 May 2026 22:13:45 GMT  
		Size: 193.5 MB (193461530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eac25c1cf741b5d466b72dbd8d3adc26f99ff0a98875f223c374d96316b1ea64`  
		Last Modified: Fri, 08 May 2026 23:50:21 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76501a536c561bbec24fb68aee19d26c1dd6160f324841b6bb1c31f99a045976`  
		Last Modified: Fri, 08 May 2026 23:50:23 GMT  
		Size: 37.9 MB (37891947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9a77a6fd3c94ecbae6826338e32d9fd8079abaa7eb5424245c68d6d8e24a090`  
		Last Modified: Fri, 08 May 2026 23:50:21 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-trixie` - unknown; unknown

```console
$ docker pull ruby@sha256:746703d861c0aa8a576419e81a9d593d9bdf98958d53f5860b15a62420f1a0e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17117198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19f55bd0d81a1c3a5aface13fd3de54b27e1716df8928d1a05cfbf98112e62ff`

```dockerfile
```

-	Layers:
	-	`sha256:4e7375fbcef091881300ceed7e028b67f7adf55c4bde671e033bd5ff369a939c`  
		Last Modified: Fri, 08 May 2026 23:50:22 GMT  
		Size: 17.1 MB (17094748 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d3cb825a6a68b4835c4764f742d3f6afeb4b2d9b8054a6b248dd19337ac1f7d`  
		Last Modified: Fri, 08 May 2026 23:50:21 GMT  
		Size: 22.4 KB (22450 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-trixie` - linux; arm64 variant v8

```console
$ docker pull ruby@sha256:265815adc72ef5556a0dbb9bb09b236472e63b378e52a1d51f9fe7d1af1c72ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **410.7 MB (410748867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8669f57e09ce2b897d48ce055e67afdb11836174c8b47af25e4217a4d5cced9b`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:42:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 20:32:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 21:18:38 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 22:45:13 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 08 May 2026 22:47:22 GMT
ENV LANG=C.UTF-8
# Fri, 08 May 2026 22:47:22 GMT
ENV RUBY_VERSION=3.4.9
# Fri, 08 May 2026 22:47:22 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Fri, 08 May 2026 22:47:22 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Fri, 08 May 2026 22:47:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 08 May 2026 22:47:22 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 08 May 2026 22:47:22 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 08 May 2026 22:47:22 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 22:47:22 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 08 May 2026 22:47:22 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:b5d74b688654dda99557234223479d1600781c2797759908abb12a2e782ab1ad`  
		Last Modified: Fri, 08 May 2026 18:26:51 GMT  
		Size: 49.7 MB (49669445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6968d8edb06bcdaf22846e8626a2500d70d68bae3413bca896fefe955e2a6ef0`  
		Last Modified: Fri, 08 May 2026 19:42:46 GMT  
		Size: 25.0 MB (25023476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc880ef5fbb726989fb57630c05c39cfe57a36a9f03c5b86a2d51c9c86ed66f2`  
		Last Modified: Fri, 08 May 2026 20:32:42 GMT  
		Size: 67.6 MB (67592055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8335e8e024cb0fa8e07cb848bdae282ce9861dd9255063fc58f55ccdf85a6f08`  
		Last Modified: Fri, 08 May 2026 21:19:23 GMT  
		Size: 226.3 MB (226273474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc45e0cf53b5f167c30f981b1e75b00fdc2c012771b4068e8de8fec3252b1fb7`  
		Last Modified: Fri, 08 May 2026 22:47:43 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fd6ae665c0ed06ba2a9cfede8c9a7556de90fe047134b8bc869a9a556824cea`  
		Last Modified: Fri, 08 May 2026 22:47:44 GMT  
		Size: 42.2 MB (42190083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd2979a97a2ac61e6513ada0a3e605e4167a162a8a1b62a981c0f1ba77346475`  
		Last Modified: Fri, 08 May 2026 22:47:43 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-trixie` - unknown; unknown

```console
$ docker pull ruby@sha256:ad3cf8f131750548c0d44cdbf449cb39b4bd4d8aabfc06bbad74ea79936180d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 MB (17433551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3eed9c759714d2ecc4bf640cee0b43d2091c2064b16a4d03648f65bcf70e456`

```dockerfile
```

-	Layers:
	-	`sha256:5b7fc1fda18a058e516bbac7a387b860bbdafb5083da0560841e445d5d255680`  
		Last Modified: Fri, 08 May 2026 22:47:44 GMT  
		Size: 17.4 MB (17411066 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:898eb2d8db88368c251fb7e6e49d2a85a5d64fea461f47ad9d5c9624510f29cb`  
		Last Modified: Fri, 08 May 2026 22:47:43 GMT  
		Size: 22.5 KB (22485 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-trixie` - linux; 386

```console
$ docker pull ruby@sha256:4c488b47734a1e39694112ad0adefd18c3a9fa2577b20a4ca04c71374e893df0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **425.5 MB (425456471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2a64a58e30b7cb658ccb698f12104806c1b6da88b79734e98cd7c936240eaff`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:43:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 23:05:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Sat, 09 May 2026 02:26:36 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Sat, 09 May 2026 03:45:28 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Sat, 09 May 2026 03:47:14 GMT
ENV LANG=C.UTF-8
# Sat, 09 May 2026 03:47:14 GMT
ENV RUBY_VERSION=3.4.9
# Sat, 09 May 2026 03:47:14 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Sat, 09 May 2026 03:47:14 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Sat, 09 May 2026 03:47:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Sat, 09 May 2026 03:47:14 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 09 May 2026 03:47:14 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 09 May 2026 03:47:14 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 May 2026 03:47:14 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Sat, 09 May 2026 03:47:14 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:93e493f785bb54571482f102af521d43083373078c8450f7707bbcce2dd2b0a2`  
		Last Modified: Fri, 08 May 2026 18:32:46 GMT  
		Size: 50.8 MB (50825581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:802713bb4712073d4a0875914c45b85ffab64ce3389edccc50bbfe0147fa12db`  
		Last Modified: Fri, 08 May 2026 19:44:08 GMT  
		Size: 26.8 MB (26784941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3633f2ad7dfa64f7e00b07a5405063f2d661e1f1a5e715c57ad65aaaf0f60d5`  
		Last Modified: Fri, 08 May 2026 23:05:42 GMT  
		Size: 69.8 MB (69815583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfce016012aae1811a31b56f808d3457fa3b5556823afa341bd018e63864905d`  
		Last Modified: Sat, 09 May 2026 02:27:17 GMT  
		Size: 240.2 MB (240244203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65b6be79ec9752c6179fca91fc2ca59e5e96d3d0727b1ad5aa54be27c1669adb`  
		Last Modified: Sat, 09 May 2026 03:47:30 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fcac355fdca2112ad13fc68e6caeecb4bde3624231ca3845e3ce7bbaff7e12a`  
		Last Modified: Sat, 09 May 2026 03:47:32 GMT  
		Size: 37.8 MB (37785829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe19c405ffde9434083a1aef9a7bdecd9ed6cd9caf9516c3218ab61040e7012f`  
		Last Modified: Sat, 09 May 2026 03:47:30 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-trixie` - unknown; unknown

```console
$ docker pull ruby@sha256:2281b61ba3608c0504bab590c8fde4f8290f377c484ff971766af88f9b97b67d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17318595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95ead7093c5d8624cabd01d4209978e9b75a8ba3e31ce8211bf5b196e8761d45`

```dockerfile
```

-	Layers:
	-	`sha256:89174edb5bd45c5fbf7872df814e82b9b0bce2320c30e1ea07906d36f6de4484`  
		Last Modified: Sat, 09 May 2026 03:47:31 GMT  
		Size: 17.3 MB (17296313 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7b0d46ffef9f2190a333207d1649c95264b8062cc8e5a2cfa115a8786ac9f5a`  
		Last Modified: Sat, 09 May 2026 03:47:30 GMT  
		Size: 22.3 KB (22282 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-trixie` - linux; ppc64le

```console
$ docker pull ruby@sha256:0c1d204ed69310b643e112368bd4c88b3670b53713fbfa31d2e51f77fe75a1c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **424.0 MB (424011597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a9223ce9fd1fb6b759d58590b07eabed5ad76f8eb2225fa54824e36536d6d6d`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 03:40:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 09:39:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 12:17:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 19:59:29 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 22 Apr 2026 20:09:13 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 20:09:13 GMT
ENV RUBY_VERSION=3.4.9
# Wed, 22 Apr 2026 20:09:13 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Wed, 22 Apr 2026 20:09:13 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Wed, 22 Apr 2026 20:09:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 22 Apr 2026 20:09:13 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 22 Apr 2026 20:09:13 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 22 Apr 2026 20:09:13 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 20:09:14 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 22 Apr 2026 20:09:14 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:0fab4f6170940889900b2327e1b3c62dace993eab8074ca7d33d1ffeef137c08`  
		Last Modified: Wed, 22 Apr 2026 00:18:18 GMT  
		Size: 53.1 MB (53122984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2454d511c21492888baf49902a298f334e8095ce0fe93b53b274ab3f39febd31`  
		Last Modified: Wed, 22 Apr 2026 03:40:51 GMT  
		Size: 27.0 MB (27014616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4f9e1a80821bce13187cd275a074ab44791a07c4796e61afbcda3a692b97ac4`  
		Last Modified: Wed, 22 Apr 2026 09:39:58 GMT  
		Size: 73.0 MB (73039689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eee24d1527042fdf5416c0f176e46ee07a4162716bc3c579e21e2b5b37cf0dc3`  
		Last Modified: Wed, 22 Apr 2026 12:18:28 GMT  
		Size: 231.2 MB (231209822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f8ca4f3c1d38e91dfe515c4ec168d38704eb5b381e24771f5fefffb62fea372`  
		Last Modified: Wed, 22 Apr 2026 20:03:16 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7565b55e1395b909f3d5088144f964830ec586757dacefe3e903e3cecde52b03`  
		Last Modified: Wed, 22 Apr 2026 20:09:58 GMT  
		Size: 39.6 MB (39624153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8570badf854bdc6b57f78e3739f82a0be7b187124e87a8597bd95d973cd37dd3`  
		Last Modified: Wed, 22 Apr 2026 20:09:57 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-trixie` - unknown; unknown

```console
$ docker pull ruby@sha256:eb2e31195da2886d34f31e26e51a0dd37f3f7eacc3ed60f9627a47d112195b03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17334693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f214aef01995d9336fe3b440b8fc939f10fe10cbe511dd7b7deba0d673ede7d3`

```dockerfile
```

-	Layers:
	-	`sha256:dd74798789b74a0031548fb89ed7ce3a7c9242cc74c4084d9d47aeb9d4915a7b`  
		Last Modified: Wed, 22 Apr 2026 20:09:57 GMT  
		Size: 17.3 MB (17312305 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c3dd70d25de854e65accc1c0fc4c15136ba2016dd421a391a2fa99f55b5c5c8`  
		Last Modified: Wed, 22 Apr 2026 20:09:57 GMT  
		Size: 22.4 KB (22388 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-trixie` - linux; riscv64

```console
$ docker pull ruby@sha256:eb3ff45a2be1538b472af39f52330d8ee0924e5183abe3f46d980a5e3bd42b5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **500.5 MB (500502721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:563e0da2b03381ee926a29b493d4040b1af14f100eead959f24395215428dc49`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1776729600'
# Sun, 26 Apr 2026 15:21:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Sun, 26 Apr 2026 19:06:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Sun, 26 Apr 2026 20:13:53 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Mon, 27 Apr 2026 17:51:11 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Mon, 27 Apr 2026 21:58:15 GMT
ENV LANG=C.UTF-8
# Mon, 27 Apr 2026 21:58:15 GMT
ENV RUBY_VERSION=3.4.9
# Mon, 27 Apr 2026 21:58:15 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Mon, 27 Apr 2026 21:58:15 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Mon, 27 Apr 2026 21:58:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Mon, 27 Apr 2026 21:58:15 GMT
ENV GEM_HOME=/usr/local/bundle
# Mon, 27 Apr 2026 21:58:15 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Mon, 27 Apr 2026 21:58:15 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 27 Apr 2026 21:58:16 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Mon, 27 Apr 2026 21:58:16 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:6e518626ae0de2d990c7c66185d308a25cb3affebb6204543438f56fd9f94992`  
		Last Modified: Wed, 22 Apr 2026 02:29:17 GMT  
		Size: 47.8 MB (47798217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84ad20ed76b58e7abcec15ac3129845a802887c092560883b4939e006992099b`  
		Last Modified: Sun, 26 Apr 2026 15:22:58 GMT  
		Size: 25.0 MB (24955805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a233e35e9c32890f2d416d3e6707a14b173707fad25985773c22f4606dee5c05`  
		Last Modified: Sun, 26 Apr 2026 19:10:01 GMT  
		Size: 66.6 MB (66648074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:375b0ab5684a2ec8ed31b820ba37fcb1bdf59a507240c61d57d8e8abbf2c70e2`  
		Last Modified: Sun, 26 Apr 2026 20:29:22 GMT  
		Size: 323.0 MB (323025554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb89bf8893e3c7bc91b12362aaca8495f37bb422d9caab5a5deeec67e86e52f9`  
		Last Modified: Mon, 27 Apr 2026 19:54:04 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f329a3e692d0288032d4bc014c3c2a1740f349e58ebc88a20b2acf6991b66765`  
		Last Modified: Mon, 27 Apr 2026 22:06:29 GMT  
		Size: 38.1 MB (38074740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:252c2cf5838bbf02ec38351b2beac0762d73cb63b794597ac92a3b257666bfca`  
		Last Modified: Mon, 27 Apr 2026 22:06:21 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-trixie` - unknown; unknown

```console
$ docker pull ruby@sha256:f6647426a2b6628766b893589b100f4c3e163c7fc870e8bf5b1de15a561eda1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 MB (17405281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6067643f2bee171e50e1914e8e0d793a613df982729bc2bb4fc4e77cd5aae165`

```dockerfile
```

-	Layers:
	-	`sha256:e4bb6ce1d835e8c67491364120a8670e99a46f8f23286c42dcb879cb3f985678`  
		Last Modified: Mon, 27 Apr 2026 22:06:26 GMT  
		Size: 17.4 MB (17382894 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c955d2472b6dddaa192313b6cd78c7a337a2c4e721459885fe90fb1b36f5bc9e`  
		Last Modified: Mon, 27 Apr 2026 22:06:21 GMT  
		Size: 22.4 KB (22387 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-trixie` - linux; s390x

```console
$ docker pull ruby@sha256:cac380f8bc1cf8c283f335c49e67ab3123eaf0e527085a7d277c90519b64d9b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **390.7 MB (390736702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63744b7242b7b55c938ad3a73b5a2eb391b2b19cc73bbb429241547b9de19d8b`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 02:32:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 04:21:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 05:13:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 09:43:04 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 22 Apr 2026 09:46:32 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 09:46:32 GMT
ENV RUBY_VERSION=3.4.9
# Wed, 22 Apr 2026 09:46:32 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Wed, 22 Apr 2026 09:46:32 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Wed, 22 Apr 2026 09:46:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 22 Apr 2026 09:46:32 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 22 Apr 2026 09:46:32 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 22 Apr 2026 09:46:32 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 09:46:32 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 22 Apr 2026 09:46:32 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:943402c24d6e7299016c00f751297dfb5fc1821547fdd1d9c56a206079784185`  
		Last Modified: Wed, 22 Apr 2026 00:17:09 GMT  
		Size: 49.4 MB (49372106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c2a3da428dd91e4b5df556514e279e6a571eec116b1f2b3ed1bc95489fcee4`  
		Last Modified: Wed, 22 Apr 2026 02:32:51 GMT  
		Size: 26.8 MB (26802425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c81397603fbb04688ca83ea8697469c3a01388a59e003d38dd37d22beb13789`  
		Last Modified: Wed, 22 Apr 2026 04:21:39 GMT  
		Size: 68.6 MB (68636900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9797d445faaa1f9219c6d6ae09f17025e8f5995b4cec1bfc6cac2d3adf9581a2`  
		Last Modified: Wed, 22 Apr 2026 05:14:44 GMT  
		Size: 206.6 MB (206602552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72ca89a5d7462dfd320be53fa6b539dad132f2aaf24e2ef50f029c5b1ee14fa2`  
		Last Modified: Wed, 22 Apr 2026 09:47:08 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2e8705c7ea5405f23dc0ee0bbd34e3a6e491f17bec2c34c6c8c3c8bbf5dc4e4`  
		Last Modified: Wed, 22 Apr 2026 09:47:09 GMT  
		Size: 39.3 MB (39322387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f49e1a723d257663c9bca9ac660db71867b63106975ff540151f16809603c34`  
		Last Modified: Wed, 22 Apr 2026 09:47:08 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-trixie` - unknown; unknown

```console
$ docker pull ruby@sha256:17d8c6ccf3bb8f52dbd147b7aff7ae655864151278e278a4a0ed9c223ffc01a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17126297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0f76e24981ceff1ddc05fb8b89f6288527c4c3bccedca04c08a27bdee664340`

```dockerfile
```

-	Layers:
	-	`sha256:5f55cb037301f64d09399452539796033673e4422feb8dae8f7fd9b7ad1e836d`  
		Last Modified: Wed, 22 Apr 2026 09:47:08 GMT  
		Size: 17.1 MB (17103969 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44f910ef1bc40313f1c3ce0496af7964fb279a5b65d5d9ffb75d83a83dba74db`  
		Last Modified: Wed, 22 Apr 2026 09:47:08 GMT  
		Size: 22.3 KB (22328 bytes)  
		MIME: application/vnd.in-toto+json
