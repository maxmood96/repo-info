## `ruby:4-trixie`

```console
$ docker pull ruby@sha256:5c41c8e4cde76a43773222821a3ea723de4a4bda82b92d8dabc88faca96c7163
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

### `ruby:4-trixie` - linux; amd64

```console
$ docker pull ruby@sha256:714ab37867060eaf62a74552016c3a2e55e65447d1ed1804b746bcc1209d5f30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **428.4 MB (428376529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11ca65802f6fea558eee6f458e2ea643eafbea68544af8c3c1f29284ffce330c`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:10:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 03:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 04:50:16 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 06:06:51 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 13 Jan 2026 06:09:00 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 06:09:00 GMT
ENV RUBY_VERSION=4.0.0
# Tue, 13 Jan 2026 06:09:00 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/4.0/ruby-4.0.0.tar.xz
# Tue, 13 Jan 2026 06:09:00 GMT
ENV RUBY_DOWNLOAD_SHA256=a72bacee9de07283ebc19baa4ac243b193129f21aa4e168c7186fb1fe7d07fe1
# Tue, 13 Jan 2026 06:09:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 		${rustArch:+--enable-zjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 13 Jan 2026 06:09:00 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 13 Jan 2026 06:09:00 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 13 Jan 2026 06:09:00 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 06:09:00 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 13 Jan 2026 06:09:00 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:2ca1bfae7ba8b9e2a56c1c19a2d14036cae96bf868ca154ca88bc078eaf7c376`  
		Last Modified: Tue, 13 Jan 2026 00:42:40 GMT  
		Size: 49.3 MB (49285621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e18c5e1c15ff34b31f1443e9327b69daaa0c1bd65a23846328fc3738c7f8f1`  
		Last Modified: Tue, 13 Jan 2026 02:11:21 GMT  
		Size: 25.6 MB (25613410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be442a7e0d6f290b909f8da51840566e06ab51bfbea277c70fbda26c44c8259d`  
		Last Modified: Tue, 13 Jan 2026 03:54:48 GMT  
		Size: 67.8 MB (67786776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26d823e3848f3d74363d9b5b44f39f2d2f81a99a37d8c7fb54831a489a32e999`  
		Last Modified: Tue, 13 Jan 2026 05:12:51 GMT  
		Size: 236.0 MB (236001828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b0b4fc640eeea2a71e613d20622b61c4c839c05eb7a1254dee00ae34c084503`  
		Last Modified: Tue, 13 Jan 2026 06:09:32 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:459866c56dc56e7b95c3907b1fccecb602f1cd787200cea2236cf02e39251437`  
		Last Modified: Tue, 13 Jan 2026 06:09:34 GMT  
		Size: 49.7 MB (49688562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf5be198c3adb114faf5592745629e736169badd8074cc49a5bdfc7e7f617385`  
		Last Modified: Tue, 13 Jan 2026 06:09:32 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:4-trixie` - unknown; unknown

```console
$ docker pull ruby@sha256:ebd38220b6bee0e4411462be98f0879d1168ee603f9d182105f572d764d90dae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17346052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb67e9557dd9985fd3a7688d4286bba004c285a63c3c57d28de5d5968b5d6ceb`

```dockerfile
```

-	Layers:
	-	`sha256:ebcf6262524325bb55d8aaa10f725bbfc19cb1d440598ce98453be30a0bdae0a`  
		Last Modified: Tue, 13 Jan 2026 07:03:58 GMT  
		Size: 17.3 MB (17323025 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a69da4d907d525b8c0e7c08a5c4356b061d6198ce82cee4322813c54ebca12af`  
		Last Modified: Tue, 13 Jan 2026 07:03:59 GMT  
		Size: 23.0 KB (23027 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:4-trixie` - linux; arm variant v5

```console
$ docker pull ruby@sha256:c1f59ee600866cd24517cace4cdc0164c142d3feec61b9dc414773935af8f718
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **385.6 MB (385581562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddf60c3c4b02e77ca04c06e931dae08fa5b00456b99d35612cba62783b19ce9c`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:29:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 04:08:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 05:13:47 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 07:17:19 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 13 Jan 2026 07:19:58 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 07:19:58 GMT
ENV RUBY_VERSION=4.0.0
# Tue, 13 Jan 2026 07:19:58 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/4.0/ruby-4.0.0.tar.xz
# Tue, 13 Jan 2026 07:19:58 GMT
ENV RUBY_DOWNLOAD_SHA256=a72bacee9de07283ebc19baa4ac243b193129f21aa4e168c7186fb1fe7d07fe1
# Tue, 13 Jan 2026 07:19:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 		${rustArch:+--enable-zjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 13 Jan 2026 07:19:58 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 13 Jan 2026 07:19:58 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 13 Jan 2026 07:19:58 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 07:19:58 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 13 Jan 2026 07:19:58 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:16d4329ceaa8dc305221873389c356e4c5bf3cdb5b245a79ff75a1b1806f3778`  
		Last Modified: Tue, 13 Jan 2026 00:42:16 GMT  
		Size: 47.4 MB (47448362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad4ac90147d1f1c4bc0ab2c1c245fb4105c9ad56d7e5e75726e8ec474c79f05f`  
		Last Modified: Tue, 13 Jan 2026 02:30:05 GMT  
		Size: 24.4 MB (24353866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0b0fe9087175027e9a76a41e2c394603c9345a19f6296b58e7044e930aafb08`  
		Last Modified: Tue, 13 Jan 2026 04:08:45 GMT  
		Size: 65.3 MB (65318536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2a03a66aae139adaadd8a808ca96b9e5d75cefae43a5eca814727bc64c805f6`  
		Last Modified: Tue, 13 Jan 2026 06:13:40 GMT  
		Size: 205.7 MB (205729923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3468b5a3587c6fb27561b3cb7fac278b61322e4dbd34f3250a8455689e75d47c`  
		Last Modified: Tue, 13 Jan 2026 07:20:31 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d649ba9c8a1da7217950ad4d4b47b6dd52b239609911c2fec2787660f8a07ce`  
		Last Modified: Tue, 13 Jan 2026 07:20:35 GMT  
		Size: 42.7 MB (42730542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1f846cad9dc1625bf779b6a7bfa262b1dfea3d862b14817bbde69b836c586f7`  
		Last Modified: Tue, 13 Jan 2026 07:20:37 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:4-trixie` - unknown; unknown

```console
$ docker pull ruby@sha256:8e8851ccb79406fa36e71844826559a9e14b34b652ed70f286c471ce6779ca6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17108428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb761418fbfe729c3ee5d7ed5bd84c2d5bc0f013378827e0594b1dbfb6c820ed`

```dockerfile
```

-	Layers:
	-	`sha256:dd3bb0311cdf43a04eae1681704302619aba17f64829089402b353474a0cc62d`  
		Last Modified: Tue, 13 Jan 2026 10:01:43 GMT  
		Size: 17.1 MB (17085263 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3718784fd2c5bf0a7285389ceb2bdab3493a41204c44dd141be26fe41717f80c`  
		Last Modified: Tue, 13 Jan 2026 10:01:44 GMT  
		Size: 23.2 KB (23165 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:4-trixie` - linux; arm variant v7

```console
$ docker pull ruby@sha256:af4b8c1cd4d6f529835600502e84535a810b6b0a6aaafaa7a96a2e358ce7fd58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.9 MB (367948092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f68c8fdf2e0b1d4ef791473b22c380adbee9992070e78ffe7060b39542367848`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:58:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 04:25:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 05:19:23 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 07:46:55 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 13 Jan 2026 07:49:19 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 07:49:19 GMT
ENV RUBY_VERSION=4.0.0
# Tue, 13 Jan 2026 07:49:19 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/4.0/ruby-4.0.0.tar.xz
# Tue, 13 Jan 2026 07:49:19 GMT
ENV RUBY_DOWNLOAD_SHA256=a72bacee9de07283ebc19baa4ac243b193129f21aa4e168c7186fb1fe7d07fe1
# Tue, 13 Jan 2026 07:49:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 		${rustArch:+--enable-zjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 13 Jan 2026 07:49:19 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 13 Jan 2026 07:49:19 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 13 Jan 2026 07:49:19 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 07:49:19 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 13 Jan 2026 07:49:19 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:0f4296a8ece8abd5a409e5fbdb0cf93258815e4fec9dc768c39a63faf3c16052`  
		Last Modified: Tue, 13 Jan 2026 01:18:45 GMT  
		Size: 45.7 MB (45717820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a8e700e2f18987ab9f97abcd0497d5dfc1706a8c057e685438ce3b71d8067c0`  
		Last Modified: Tue, 13 Jan 2026 02:59:15 GMT  
		Size: 23.6 MB (23626665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bf6f5dfbcc297b2e354e856be84c591ec9f96e89fd8401a4d485596c43b8ed8`  
		Last Modified: Tue, 13 Jan 2026 04:26:15 GMT  
		Size: 62.7 MB (62713384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bc2c3dfa2d6df259da14558beefb7cee69246c0da0fdc440a04d5af7c8fb7dd`  
		Last Modified: Tue, 13 Jan 2026 06:15:55 GMT  
		Size: 193.3 MB (193306851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bedf5edced3f300c154361c6d1e8b0ba2c8cde04e41b3b085e872374fa284c3`  
		Last Modified: Tue, 13 Jan 2026 07:49:46 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47e476cd65a7bdb6a5837eb9d3000f19fdd02363e41996ece4d98dd71cfc627f`  
		Last Modified: Tue, 13 Jan 2026 07:49:49 GMT  
		Size: 42.6 MB (42583040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73355bb78a5fedcc06d9d1f3772ea4f3a690c3f6a2790f45c7d8f5c0934d690c`  
		Last Modified: Tue, 13 Jan 2026 07:49:46 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:4-trixie` - unknown; unknown

```console
$ docker pull ruby@sha256:07c8fe91584e2a7eb690ac603cf7a22539cd11acf5e174cf85ea3b9cb052f60a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17114218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c75be4cc8b3c7f187a16e625fb4ae8f5e627e9db31561597f55d5033fddc9caf`

```dockerfile
```

-	Layers:
	-	`sha256:53929ecff6b102b1544a2b33854544662d78431027bcd742a2c05ce18bfd2ad4`  
		Last Modified: Tue, 13 Jan 2026 10:02:13 GMT  
		Size: 17.1 MB (17091053 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3be427dc63dbf74464d5ab7e8921bfb8f133fa0426c918157a3b36394e19b95e`  
		Last Modified: Tue, 13 Jan 2026 10:02:14 GMT  
		Size: 23.2 KB (23165 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:4-trixie` - linux; arm64 variant v8

```console
$ docker pull ruby@sha256:748d3c71358f132926fc8d78b0dcebf277c44b651c16d82619331d7914c2e1c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **418.0 MB (417966744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef7eb7b4d228fe7a24efc532f3959d5507c21475da1d08ac689c5c1740bb5e4a`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:15:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 03:58:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 04:52:45 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 06:08:03 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 13 Jan 2026 06:10:14 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 06:10:14 GMT
ENV RUBY_VERSION=4.0.0
# Tue, 13 Jan 2026 06:10:14 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/4.0/ruby-4.0.0.tar.xz
# Tue, 13 Jan 2026 06:10:14 GMT
ENV RUBY_DOWNLOAD_SHA256=a72bacee9de07283ebc19baa4ac243b193129f21aa4e168c7186fb1fe7d07fe1
# Tue, 13 Jan 2026 06:10:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 		${rustArch:+--enable-zjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 13 Jan 2026 06:10:14 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 13 Jan 2026 06:10:14 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 13 Jan 2026 06:10:14 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 06:10:14 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 13 Jan 2026 06:10:14 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:5582010cab7f00a8f96e076b02666116eaa7e4af9a74eb44f2946a593b50294f`  
		Last Modified: Tue, 13 Jan 2026 00:42:51 GMT  
		Size: 49.6 MB (49648083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:599d5b6b6766fd729045e2e7d0396d1f61fe41c612d4aef6bb3bf5ea7db12ae2`  
		Last Modified: Tue, 13 Jan 2026 02:15:57 GMT  
		Size: 25.0 MB (25022636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9b629762372f548de0ebccf01b8e80ae5ce251dfd36aef6fc3ae8d963493edf`  
		Last Modified: Tue, 13 Jan 2026 03:58:49 GMT  
		Size: 67.6 MB (67591513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fffeb567ed4215b503f814aeaab9fa5a2e701d3efa35d4c285b3cf111e9cb4a`  
		Last Modified: Tue, 13 Jan 2026 05:16:01 GMT  
		Size: 226.1 MB (226143857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56c943deb66328dddf7d2771af026a1c533d7c9c5a9981a41b0557af4958bb92`  
		Last Modified: Tue, 13 Jan 2026 06:10:43 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e2a7d694c072544c5ec9602a5a129f559fe73c48653859ddc4f35c35f88699d`  
		Last Modified: Tue, 13 Jan 2026 06:10:47 GMT  
		Size: 49.6 MB (49560324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b13129a05cc4e25d9845b9dd3a251c155b8bd0e68bc6779d571e439d309ddd3`  
		Last Modified: Tue, 13 Jan 2026 06:10:43 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:4-trixie` - unknown; unknown

```console
$ docker pull ruby@sha256:846b9a93b91dd34c1baae8fa7559bcea98abe28473ce95098e8c23018eaed703
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 MB (17430588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48a516f9732ec54bcc72bc1580b8db6491fbf30e85761a93585a61ef5cda51bd`

```dockerfile
```

-	Layers:
	-	`sha256:3c42c126e2126df8478a2d45eb60018938588fee14d0e4ca0e72f5f710d069cd`  
		Last Modified: Tue, 13 Jan 2026 10:02:30 GMT  
		Size: 17.4 MB (17407379 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53899fcbc85f99512d50bdde228306ff370171d14d30c2d3931adfe7cd3a6bca`  
		Last Modified: Tue, 13 Jan 2026 10:02:31 GMT  
		Size: 23.2 KB (23209 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:4-trixie` - linux; 386

```console
$ docker pull ruby@sha256:b3ba1928822f6e7a3d3d002d0ebbab40d3bd5b4a57947f2d25f4c5ae757274fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **430.0 MB (429964180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6346fd8504c7462a0dcecda0bb8a533825ea85a32253d887b72d6532a96762e0`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:03:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 03:04:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 03:56:48 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 04:48:34 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 13 Jan 2026 04:50:20 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 04:50:20 GMT
ENV RUBY_VERSION=4.0.0
# Tue, 13 Jan 2026 04:50:20 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/4.0/ruby-4.0.0.tar.xz
# Tue, 13 Jan 2026 04:50:20 GMT
ENV RUBY_DOWNLOAD_SHA256=a72bacee9de07283ebc19baa4ac243b193129f21aa4e168c7186fb1fe7d07fe1
# Tue, 13 Jan 2026 04:50:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 		${rustArch:+--enable-zjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 13 Jan 2026 04:50:20 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 13 Jan 2026 04:50:20 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 13 Jan 2026 04:50:20 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 04:50:20 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 13 Jan 2026 04:50:20 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:1f0b243ad587d8f60f107748ba9fe54e338921c7b90e6a5d26e1d50d32f7481b`  
		Last Modified: Tue, 13 Jan 2026 00:43:36 GMT  
		Size: 50.8 MB (50798876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef949cdbd6ae265d5239bd005e65c3d578de54ebe10474ccd2feb9708b6e1843`  
		Last Modified: Tue, 13 Jan 2026 02:03:47 GMT  
		Size: 26.8 MB (26778274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01ad78e3f6c783e58b723e0e1c78c005c2b612d1657c3a40830f5d7d97f9d85c`  
		Last Modified: Tue, 13 Jan 2026 03:04:58 GMT  
		Size: 69.8 MB (69803208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c438693622c619054710e61f4e49c9f44709996e7ac1c8577527c38f87d008f`  
		Last Modified: Tue, 13 Jan 2026 04:02:03 GMT  
		Size: 240.1 MB (240108789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f55884ec3c9d15e582fd82c9fee75d3296eabddc7f7e4623d176df8111edf7fb`  
		Last Modified: Tue, 13 Jan 2026 04:50:46 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baf4a2e1d0981e0ee1f90f53cdb8f8f6f9f7162a0c64ff1306dd4899cd21add6`  
		Last Modified: Tue, 13 Jan 2026 04:50:49 GMT  
		Size: 42.5 MB (42474700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f5c6414e342dfdc1c01cf7fbc0e174148efc70dfc5d53b0fcb16a9a84a3a895`  
		Last Modified: Tue, 13 Jan 2026 04:50:46 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:4-trixie` - unknown; unknown

```console
$ docker pull ruby@sha256:0432dcc29a43b18795ef882d6131a68167c997d1a19468cc93c67adf16ae0646
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17315563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:399d955773eb769c733757d5b52eb53c29f97a385d160d0a3bffdd61dc62a076`

```dockerfile
```

-	Layers:
	-	`sha256:cc7cb9522c1eac30fa4889200dff996a754379db3ec23d910370d1f4e188b2eb`  
		Last Modified: Tue, 13 Jan 2026 07:05:05 GMT  
		Size: 17.3 MB (17292592 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb48b86024ed3b64b83ba34d6edfe601c75c401cf63d0a5a70baa7c23f0bad0d`  
		Last Modified: Tue, 13 Jan 2026 07:05:06 GMT  
		Size: 23.0 KB (22971 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:4-trixie` - linux; ppc64le

```console
$ docker pull ruby@sha256:a41bb60d74b310fc9a7c46a34aa6afd99b8efdce81a98729660cc7143803e885
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **428.8 MB (428771607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a9b95a114901773703a475f8d478fe085fb90d5088dca420ca66ee898ad11e6`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 03:18:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 08:22:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 09:11:39 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 14:41:18 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 30 Dec 2025 14:44:02 GMT
ENV LANG=C.UTF-8
# Tue, 30 Dec 2025 14:44:02 GMT
ENV RUBY_VERSION=4.0.0
# Tue, 30 Dec 2025 14:44:02 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/4.0/ruby-4.0.0.tar.xz
# Tue, 30 Dec 2025 14:44:02 GMT
ENV RUBY_DOWNLOAD_SHA256=a72bacee9de07283ebc19baa4ac243b193129f21aa4e168c7186fb1fe7d07fe1
# Tue, 30 Dec 2025 14:44:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 		${rustArch:+--enable-zjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 30 Dec 2025 14:44:02 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 30 Dec 2025 14:44:02 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 30 Dec 2025 14:44:02 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 14:44:03 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 30 Dec 2025 14:44:03 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:d586c84fb9377f9b3f4030e2c3e1e9ff7b1a23a68b8abc2c48a43163a3589257`  
		Last Modified: Tue, 30 Dec 2025 01:51:01 GMT  
		Size: 53.1 MB (53108485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd44afe623a2af1e017b0756e314b5b0882afdc551ddbb8ab4a0e0d718eb8f20`  
		Last Modified: Tue, 30 Dec 2025 03:19:14 GMT  
		Size: 27.0 MB (26996817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1464b5ef37e07d88bfdddc49e0cb0b76c46c151a0ee23e6a2bd75bd6783f9790`  
		Last Modified: Tue, 30 Dec 2025 08:23:35 GMT  
		Size: 73.0 MB (73031008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47d3a85aaf4fce519ba1881ffe98345cfe2bb8d405248c0e26407d788b5fbe09`  
		Last Modified: Tue, 30 Dec 2025 09:13:44 GMT  
		Size: 231.1 MB (231106961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4692cf30e99b2334625487f0b1be2d80699142edffd9b82a08e62a4afd4ae1d3`  
		Last Modified: Tue, 30 Dec 2025 14:44:58 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:789ee6b46798ffef94c36580310928cf4e6fe11ccb817b89e5304ff7de44037e`  
		Last Modified: Tue, 30 Dec 2025 14:45:03 GMT  
		Size: 44.5 MB (44528003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:019b644041609091b1be2b2306043a96a809196e71131c1309f887e8e97e3198`  
		Last Modified: Tue, 30 Dec 2025 14:44:58 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:4-trixie` - unknown; unknown

```console
$ docker pull ruby@sha256:f338f85af1fa232865eb5a2ade9564777c5eeb024bd3d27e82c6916cfbc458f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17330574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed799ed9024401eb06f5994fc139fbf1913f8f7beeb25324678ed8cfd7b8f147`

```dockerfile
```

-	Layers:
	-	`sha256:dac6c5863a308098f40d0d47efa73a6332a7ce4f6c38b48fc63aeffa1cecda47`  
		Last Modified: Tue, 30 Dec 2025 16:00:41 GMT  
		Size: 17.3 MB (17307475 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ce33b1408446034ec0a775cc7502f3f691d4f795f9ecbd472b3e77c3cc91868`  
		Last Modified: Tue, 30 Dec 2025 16:00:42 GMT  
		Size: 23.1 KB (23099 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:4-trixie` - linux; riscv64

```console
$ docker pull ruby@sha256:1b649df3148d9824ce92cc96925534eacfdf6aae7cd5ada8f19f13ccfb4f6b30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **506.5 MB (506505916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be3677b67f21d2003439f7dc568a788e28d28ed51c449fc4472fe94148814f6d`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1766966400'
# Wed, 31 Dec 2025 10:16:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Thu, 01 Jan 2026 12:43:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 02 Jan 2026 20:04:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Sat, 03 Jan 2026 21:52:44 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Sat, 03 Jan 2026 23:47:46 GMT
ENV LANG=C.UTF-8
# Sat, 03 Jan 2026 23:47:46 GMT
ENV RUBY_VERSION=4.0.0
# Sat, 03 Jan 2026 23:47:46 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/4.0/ruby-4.0.0.tar.xz
# Sat, 03 Jan 2026 23:47:46 GMT
ENV RUBY_DOWNLOAD_SHA256=a72bacee9de07283ebc19baa4ac243b193129f21aa4e168c7186fb1fe7d07fe1
# Sat, 03 Jan 2026 23:47:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 		${rustArch:+--enable-zjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Sat, 03 Jan 2026 23:47:46 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 03 Jan 2026 23:47:46 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 03 Jan 2026 23:47:46 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 03 Jan 2026 23:47:47 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Sat, 03 Jan 2026 23:47:47 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:aaf3ef12aa0c431a6203a456b21b1e30e26cb56dfc257b8bca2efe1ba7c531de`  
		Last Modified: Tue, 30 Dec 2025 00:51:33 GMT  
		Size: 47.8 MB (47771153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3f7933c6ef71f06a1f0f33145f157cbfe6df70a0a3efc496c514e6bf0f3c52`  
		Last Modified: Wed, 31 Dec 2025 10:17:43 GMT  
		Size: 25.0 MB (24953863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e727fba04feac92f30181733d92a9aab095f91af402efca58918b26fc389037e`  
		Last Modified: Thu, 01 Jan 2026 12:46:54 GMT  
		Size: 66.7 MB (66660576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d5842d1b9c503108d0c11e7fac9c78cd2e8430f5b938c14278c02d62d5dcbea`  
		Last Modified: Fri, 02 Jan 2026 20:21:44 GMT  
		Size: 322.9 MB (322886588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f805d49a9843699b3b2af83b567e84c3910859c6c3afa3935646d13fb0f4d38`  
		Last Modified: Sat, 03 Jan 2026 23:56:21 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c9195711163cc2699b45880e77b06fc29cbc3a34ff1a2cb53bf42f7c00782ff`  
		Last Modified: Sat, 03 Jan 2026 23:56:27 GMT  
		Size: 44.2 MB (44233403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55fecfccebd74f1a4c3b649d10b1b46a2901fbe362daab286d3ada399ccb7b07`  
		Last Modified: Sat, 03 Jan 2026 23:56:20 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:4-trixie` - unknown; unknown

```console
$ docker pull ruby@sha256:69cef2145d1befdbc92e49c4aa15cd6fa5842662bdb5657a00aa93a115929203
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 MB (17401162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eb34f432de407e71a994d6e19d1901da6b40088cbcf3faa38f349ea49d210ca`

```dockerfile
```

-	Layers:
	-	`sha256:a69007b0159e1a8aaee606a2ba9a5fc06471cb0049a54d2a49e3b3512fba62cd`  
		Last Modified: Sun, 04 Jan 2026 01:00:09 GMT  
		Size: 17.4 MB (17378064 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb6d180f6a3014cb74ce20cae9cb329aee7bb36b7c90d47e0450a7a4fba2feb6`  
		Last Modified: Sun, 04 Jan 2026 01:00:10 GMT  
		Size: 23.1 KB (23098 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:4-trixie` - linux; s390x

```console
$ docker pull ruby@sha256:3a1e147b55f190ec6a5f0d7f5df3ba5d59a5720fda38b17e827af1593678ae7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **395.7 MB (395665005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:582b40de5540aae21da9ae99296ffee6bb9830f7e62779d69242bc9ca30d1ecc`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:11:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 03:15:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 04:18:59 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 08:17:25 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 13 Jan 2026 08:20:13 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 08:20:13 GMT
ENV RUBY_VERSION=4.0.0
# Tue, 13 Jan 2026 08:20:13 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/4.0/ruby-4.0.0.tar.xz
# Tue, 13 Jan 2026 08:20:13 GMT
ENV RUBY_DOWNLOAD_SHA256=a72bacee9de07283ebc19baa4ac243b193129f21aa4e168c7186fb1fe7d07fe1
# Tue, 13 Jan 2026 08:20:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 		${rustArch:+--enable-zjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 13 Jan 2026 08:20:13 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 13 Jan 2026 08:20:13 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 13 Jan 2026 08:20:13 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 08:20:13 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 13 Jan 2026 08:20:13 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:9de0288d81a9602539c9f3015fc521191e25eebfe6442c22cb974ea3a486f3a8`  
		Last Modified: Tue, 13 Jan 2026 00:41:55 GMT  
		Size: 49.3 MB (49348704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:629a9411869af8d59bfb1073c3573138af1f96d808896b3f2fd14cf62fca6dba`  
		Last Modified: Tue, 13 Jan 2026 02:11:34 GMT  
		Size: 26.8 MB (26792892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff54b33211ee85001fc045dcc86b026876894b17d1d6f873a415014f68cb0c9f`  
		Last Modified: Tue, 13 Jan 2026 03:16:21 GMT  
		Size: 68.6 MB (68632678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68fc8348b5ddb8c2acabb8e9ca2d1b4b97457b5a1f89dd3ca04047f15644b88c`  
		Last Modified: Tue, 13 Jan 2026 05:17:23 GMT  
		Size: 206.5 MB (206530469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10e1b9f563a0ea1950bc28b75ef8851e676e5f87296b4efcdb7e49cf085d509b`  
		Last Modified: Tue, 13 Jan 2026 08:20:59 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daed499d7bf0686908673097b61d47d471c1d10172d142bcae05cc5db786bc8e`  
		Last Modified: Tue, 13 Jan 2026 08:21:03 GMT  
		Size: 44.4 MB (44359930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:126dfa01815dc994220d264f55b42bb813fcd4f1b52079df845886a1183652bc`  
		Last Modified: Tue, 13 Jan 2026 08:20:59 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:4-trixie` - unknown; unknown

```console
$ docker pull ruby@sha256:b8a1365e21f806ba7ec76682f22cb95ff1a7d6190c65299a553990c63cf1a3ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17123285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff66d932a2450cbb536583a8a80842b783e927624074b7dd1755b0b3d8a58e5e`

```dockerfile
```

-	Layers:
	-	`sha256:b4213fcc4900afba97e07d01cbe0760d7c19af3f5aa63b45224180129a42d78b`  
		Last Modified: Tue, 13 Jan 2026 13:02:28 GMT  
		Size: 17.1 MB (17100258 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb4b6731e4ce7ef12975313c1d9612869908a446d00600a5664df02acd5b0872`  
		Last Modified: Tue, 13 Jan 2026 13:02:29 GMT  
		Size: 23.0 KB (23027 bytes)  
		MIME: application/vnd.in-toto+json
