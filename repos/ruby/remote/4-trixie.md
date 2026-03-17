## `ruby:4-trixie`

```console
$ docker pull ruby@sha256:93b0c68ea6cd77fc8f08227b7a04be802ed89e660eb9c01f304605f8772fd2d8
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
$ docker pull ruby@sha256:4092d4935fd5839f641764105f4b42f11995201f917c0a09d34a28b9afeae47f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **428.5 MB (428490429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f4cbf80d82bd907390e08ddfc39687d3239fe43b88d5d13575aa300a1cd0a97`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:38:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Mon, 16 Mar 2026 23:25:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 17 Mar 2026 00:20:14 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Tue, 17 Mar 2026 16:24:59 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 17 Mar 2026 16:27:07 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 16:27:07 GMT
ENV RUBY_VERSION=4.0.2
# Tue, 17 Mar 2026 16:27:07 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/4.0/ruby-4.0.2.tar.xz
# Tue, 17 Mar 2026 16:27:07 GMT
ENV RUBY_DOWNLOAD_SHA256=4618db85bb9ec04d8152d0099db488694a3d3c4f52106625e4ad547f1318db87
# Tue, 17 Mar 2026 16:27:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 		${rustArch:+--enable-zjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 17 Mar 2026 16:27:07 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 17 Mar 2026 16:27:07 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 17 Mar 2026 16:27:07 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 16:27:07 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 17 Mar 2026 16:27:07 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:8f6ad858d0a46fa8ee628532c70b8dc82d06179d543b0b09ec19fc03d4c5b373`  
		Last Modified: Mon, 16 Mar 2026 21:53:17 GMT  
		Size: 49.3 MB (49297530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b012eb15dff0bce418c03ec940325aee6aa4300d771c325728855697e620c63a`  
		Last Modified: Mon, 16 Mar 2026 22:38:25 GMT  
		Size: 25.6 MB (25621715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee3a0e7d77f0c84203cab438fcf345647c8121bbd80506a3c692f8608a14c4f4`  
		Last Modified: Mon, 16 Mar 2026 23:25:57 GMT  
		Size: 67.8 MB (67780758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8688d0f2f567884eb217c6f80efa063bdb13a1951e92e6c5cac1ae5b736f5e1b`  
		Last Modified: Tue, 17 Mar 2026 00:21:01 GMT  
		Size: 236.1 MB (236079671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74a1780d4ea8d71840738a6220d63f45563fc0aa04d54688c1f2ece72cdf1931`  
		Last Modified: Tue, 17 Mar 2026 16:27:31 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10987269ba9b23087c97cb4277826e4ebafec04ee6f09cb5333e04f05917bf38`  
		Last Modified: Tue, 17 Mar 2026 16:27:34 GMT  
		Size: 49.7 MB (49710423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71556b3102af56c214e1ca70ecbc00671e9b77f2b5b59755d6550b383eb463c4`  
		Last Modified: Tue, 17 Mar 2026 16:27:31 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:4-trixie` - unknown; unknown

```console
$ docker pull ruby@sha256:a80467cbd6430849fac12fce1c93d9cf36897e396fd5ed6f7b7a2631bcb94999
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17346146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e66a7001074e5e03ae8c7969bb598b13a225e474fa3261b3d59fa24d3b902a2c`

```dockerfile
```

-	Layers:
	-	`sha256:714b2aac573f7af5e9389d7aba1a2b55f63f0d53c212fa26d600334db147941a`  
		Last Modified: Tue, 17 Mar 2026 16:27:32 GMT  
		Size: 17.3 MB (17323119 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:537a641a7e1ec67c86885644271488150b3224cba817186474ed37a3be6028fe`  
		Last Modified: Tue, 17 Mar 2026 16:27:31 GMT  
		Size: 23.0 KB (23027 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:4-trixie` - linux; arm variant v5

```console
$ docker pull ruby@sha256:e2841ac12952f512fdd8b39d26fd4789cc4f64b96b1a4801fe51aa232966536d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **385.7 MB (385694742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9590a7415a6ebab42ff3a3786927f6184f3b33590c7da875b5973c363fb7b170`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 23:16:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 17 Mar 2026 01:08:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 17 Mar 2026 02:19:17 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Tue, 17 Mar 2026 16:25:11 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 17 Mar 2026 16:27:46 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 16:27:46 GMT
ENV RUBY_VERSION=4.0.2
# Tue, 17 Mar 2026 16:27:46 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/4.0/ruby-4.0.2.tar.xz
# Tue, 17 Mar 2026 16:27:46 GMT
ENV RUBY_DOWNLOAD_SHA256=4618db85bb9ec04d8152d0099db488694a3d3c4f52106625e4ad547f1318db87
# Tue, 17 Mar 2026 16:27:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 		${rustArch:+--enable-zjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 17 Mar 2026 16:27:46 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 17 Mar 2026 16:27:46 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 17 Mar 2026 16:27:46 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 16:27:46 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 17 Mar 2026 16:27:46 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:8524aea9c07f7c3a1779bfcb961bdcea323ac7abd571c794a134ffeb31a825be`  
		Last Modified: Mon, 16 Mar 2026 21:52:54 GMT  
		Size: 47.5 MB (47460612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4a10acd8de7c2ea5feeb4bbe7b5147fdee10ce64d8ad5f6db26957ab6ab82a0`  
		Last Modified: Mon, 16 Mar 2026 23:17:07 GMT  
		Size: 24.4 MB (24364203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:043762e26fc507e51d741404184de0ffa48c048233f8091ab9a9f0a36a848703`  
		Last Modified: Tue, 17 Mar 2026 01:08:51 GMT  
		Size: 65.3 MB (65316059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8c68fb49833128a0e871517930af2b90f7664e7e4693c07588b34ef9db2a4ae`  
		Last Modified: Tue, 17 Mar 2026 02:19:57 GMT  
		Size: 205.8 MB (205798566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e9b090db5192b8b77c657a17e22c92b9291d6dea829596dba87c17209b71339`  
		Last Modified: Tue, 17 Mar 2026 16:28:09 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5da332dce49e8b2be195d4bf1588c0ec8914deb9eaf289e2052ec96ec2af2bfd`  
		Last Modified: Tue, 17 Mar 2026 16:28:10 GMT  
		Size: 42.8 MB (42754971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ded7040060705670d1001b0a2c4dd382e9234cd4990fcb1896b868932cac1ace`  
		Last Modified: Tue, 17 Mar 2026 16:28:09 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:4-trixie` - unknown; unknown

```console
$ docker pull ruby@sha256:9bccfb7d53c58a8079116bcd17dcf9989a2322060ac2841cdbbf2efe6fec12f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17108522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daaf4d13fb6c7f1a551941d4992b13a5154efb61c75a07d5f2aebb779c52fa7f`

```dockerfile
```

-	Layers:
	-	`sha256:01664eec43d809a880eeb62b6ecbdab22432ec9780ec564a8a5f119040fbec70`  
		Last Modified: Tue, 17 Mar 2026 16:28:10 GMT  
		Size: 17.1 MB (17085357 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a40598e6a2dfa541bddc71798b7b4c09ba33ea7cfbea5bf162a3eb4d1739014`  
		Last Modified: Tue, 17 Mar 2026 16:28:09 GMT  
		Size: 23.2 KB (23165 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:4-trixie` - linux; arm variant v7

```console
$ docker pull ruby@sha256:8bc7d6b29899445e0707a0f5ae86309e5e17449066eb7d2b196d23c00e0c7573
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.0 MB (368031440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dd43d8aafe648c1726ae3bfa866b7fa70819638dd47242d9c7cda9302cf63d5`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 00:27:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 17 Mar 2026 01:15:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 17 Mar 2026 02:17:49 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Tue, 17 Mar 2026 16:26:21 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 17 Mar 2026 16:28:42 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 16:28:42 GMT
ENV RUBY_VERSION=4.0.2
# Tue, 17 Mar 2026 16:28:42 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/4.0/ruby-4.0.2.tar.xz
# Tue, 17 Mar 2026 16:28:42 GMT
ENV RUBY_DOWNLOAD_SHA256=4618db85bb9ec04d8152d0099db488694a3d3c4f52106625e4ad547f1318db87
# Tue, 17 Mar 2026 16:28:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 		${rustArch:+--enable-zjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 17 Mar 2026 16:28:42 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 17 Mar 2026 16:28:42 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 17 Mar 2026 16:28:42 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 16:28:42 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 17 Mar 2026 16:28:42 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:83d3fd32d825865515469d080b5a8d89e630e2ed8f99a18d7b80d9c437631ab6`  
		Last Modified: Mon, 16 Mar 2026 21:53:25 GMT  
		Size: 45.7 MB (45732648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cceb46da040530c459a3d55c1b9d0ccf68be7e284352029649a82437d5fc663`  
		Last Modified: Tue, 17 Mar 2026 00:27:35 GMT  
		Size: 23.6 MB (23637012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e536a24ef93e50bf0d2984c667c771026334af7e30ed6318f85d146e4ff7a306`  
		Last Modified: Tue, 17 Mar 2026 01:15:28 GMT  
		Size: 62.7 MB (62713901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86f696900d4222bf2837e3b49ef63fc1177cb3ecebfcfa488c398c25b057bd61`  
		Last Modified: Tue, 17 Mar 2026 02:18:26 GMT  
		Size: 193.4 MB (193352535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de3a295871957e3f5da8f40d2dbc6855baef24f8b5a9cbae33217e2b5f67a36d`  
		Last Modified: Tue, 17 Mar 2026 16:29:04 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:013e149628163ab2fa92f2d4ca60934dd2f3d5c987b40297210e5cd79588fab9`  
		Last Modified: Tue, 17 Mar 2026 16:29:06 GMT  
		Size: 42.6 MB (42595013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb1b3e8fb9a4fc7c0dc2add3a7e447218ff864a76fd290ad450a29167fb639ff`  
		Last Modified: Tue, 17 Mar 2026 16:29:04 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:4-trixie` - unknown; unknown

```console
$ docker pull ruby@sha256:19283c6192b1f2bf01e4702d7ebff5ebc6bfa77a8509044b772e2ae185a60131
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17114312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d51046dd9a281dfd901e9a668cea1e423e1dbd0f3ca40a27bc55238c1d6eded`

```dockerfile
```

-	Layers:
	-	`sha256:612b71aa70d30a8280c940ea8b6623ba5e79bccc0eb607f663cfaf6ea531253f`  
		Last Modified: Tue, 17 Mar 2026 16:29:05 GMT  
		Size: 17.1 MB (17091147 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f514a3b9d02f85e508f5c66d5ab8ee3a9adbb0b6fe8b1f203740d8a28370be4b`  
		Last Modified: Tue, 17 Mar 2026 16:29:04 GMT  
		Size: 23.2 KB (23165 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:4-trixie` - linux; arm64 variant v8

```console
$ docker pull ruby@sha256:e000033a34edf37b1289bb5e67457dd04df7374aabbb7753f33f18d4ba01238b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **418.1 MB (418057028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ccbc8d2e371d1f0685087a64416f2a0b50066b81fbddcd567f8fdc5edbd8091`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:40:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Mon, 16 Mar 2026 23:30:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 17 Mar 2026 00:20:05 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Tue, 17 Mar 2026 16:24:51 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 17 Mar 2026 16:26:58 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 16:26:58 GMT
ENV RUBY_VERSION=4.0.2
# Tue, 17 Mar 2026 16:26:58 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/4.0/ruby-4.0.2.tar.xz
# Tue, 17 Mar 2026 16:26:58 GMT
ENV RUBY_DOWNLOAD_SHA256=4618db85bb9ec04d8152d0099db488694a3d3c4f52106625e4ad547f1318db87
# Tue, 17 Mar 2026 16:26:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 		${rustArch:+--enable-zjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 17 Mar 2026 16:26:58 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 17 Mar 2026 16:26:58 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 17 Mar 2026 16:26:58 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 16:26:59 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 17 Mar 2026 16:26:59 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:deab8db42772fcfeb45003461fe0eb7bf63bdb29199a4fb76242b9493437c28b`  
		Last Modified: Mon, 16 Mar 2026 21:53:03 GMT  
		Size: 49.7 MB (49664953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6778b62bd97b31237948877e89abc29ad2b2c003f3b965027457c8c90d4f44e0`  
		Last Modified: Mon, 16 Mar 2026 22:40:45 GMT  
		Size: 25.0 MB (25023728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d16813bdedcf0a1acbd78336c5bed6fbfaee2674574408140ba7e896cd49cb95`  
		Last Modified: Mon, 16 Mar 2026 23:31:00 GMT  
		Size: 67.6 MB (67584568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86cdc6c7463a47d1f18421cbc086ad744c8d50c71a79c199d3f739370d14f166`  
		Last Modified: Tue, 17 Mar 2026 00:20:49 GMT  
		Size: 226.2 MB (226205219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e205e257a81ea26ce689996be9d00df4a970227113863062ea09dc6251442cf`  
		Last Modified: Tue, 17 Mar 2026 16:27:23 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65068655342816aa04404876406bdb892121f8e6ec04518143d4c87f1163fa90`  
		Last Modified: Tue, 17 Mar 2026 16:27:25 GMT  
		Size: 49.6 MB (49578229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d47c48ba23ce9722fb4fe47da25d7b33f66e30d0e19afb0de56b4225fb712950`  
		Last Modified: Tue, 17 Mar 2026 16:27:23 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:4-trixie` - unknown; unknown

```console
$ docker pull ruby@sha256:d48d20dbc7dad94348e1c7d870a6a3a8a4bb8d29764253b15ec8a6d374852167
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 MB (17430682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47943e30d9fc6d9c3f69d233816485b8e459d90df643be8d8d59952c68e5bdb1`

```dockerfile
```

-	Layers:
	-	`sha256:a69813b7f066c5a46e5844429692210e211b10f536d77f480d512324252810f9`  
		Last Modified: Tue, 17 Mar 2026 16:27:24 GMT  
		Size: 17.4 MB (17407473 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2cca709f10ce28eddb5b858a4d25be65570b77c6cb4fc2347497ce36973c274a`  
		Last Modified: Tue, 17 Mar 2026 16:27:23 GMT  
		Size: 23.2 KB (23209 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:4-trixie` - linux; 386

```console
$ docker pull ruby@sha256:12ca01eebc2a142b442f80f840dee1d788f70766752151efbcde43599becc71f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **430.1 MB (430060189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6316a35e57c434bf174869df9efe66a45036b5bf5c1fb611b50f02414ae914b`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:44:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Mon, 16 Mar 2026 23:42:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 17 Mar 2026 00:20:17 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Tue, 17 Mar 2026 16:25:34 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 17 Mar 2026 16:27:25 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 16:27:25 GMT
ENV RUBY_VERSION=4.0.2
# Tue, 17 Mar 2026 16:27:25 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/4.0/ruby-4.0.2.tar.xz
# Tue, 17 Mar 2026 16:27:25 GMT
ENV RUBY_DOWNLOAD_SHA256=4618db85bb9ec04d8152d0099db488694a3d3c4f52106625e4ad547f1318db87
# Tue, 17 Mar 2026 16:27:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 		${rustArch:+--enable-zjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 17 Mar 2026 16:27:25 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 17 Mar 2026 16:27:25 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 17 Mar 2026 16:27:25 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 16:27:25 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 17 Mar 2026 16:27:25 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:a59dab062b6e61bf7c8c44e3e14585d36526de4560825ba7d4c8196503c6eb87`  
		Last Modified: Mon, 16 Mar 2026 21:53:40 GMT  
		Size: 50.8 MB (50818792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:027db2aaf35fd2a2c9adf573b12a548dde1e9e6733b0a9d987c465038a81dcb2`  
		Last Modified: Mon, 16 Mar 2026 22:44:31 GMT  
		Size: 26.8 MB (26783539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd35fd6ac345d92e539dc7dc49dc31742923ebf394762120d349ae52e655e6ff`  
		Last Modified: Mon, 16 Mar 2026 23:42:21 GMT  
		Size: 69.8 MB (69795316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54d7c1fbe7b89b6f8e3ca46b0be894caed5dcab48c010ed0634eef84c1573a21`  
		Last Modified: Tue, 17 Mar 2026 00:21:03 GMT  
		Size: 240.2 MB (240175291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f84ebada2e9bc1e06774a45e332a3f3ff6c0663efae62f29e3c3051102c3bd69`  
		Last Modified: Tue, 17 Mar 2026 16:27:48 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca806ae5605b6cc4bd356a6e81ffa21cb06e8b50ff70ed1324b7891faa837fc0`  
		Last Modified: Tue, 17 Mar 2026 16:27:49 GMT  
		Size: 42.5 MB (42486919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22649a97c221ae1389ac477c30fa5448673cd485aacda0221f0ac1b0bf0ab1a8`  
		Last Modified: Tue, 17 Mar 2026 16:27:47 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:4-trixie` - unknown; unknown

```console
$ docker pull ruby@sha256:559b6785b73e8fef2522d8de58dd5adec40229937d8ae18738607e6624d02959
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17315654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6544502eec3f2fe3223dcc51ff00ceddf3ff608b21680d46ebbdc12894ffa690`

```dockerfile
```

-	Layers:
	-	`sha256:fdab23ee8b7b5a2881da1ec445fe969659486da03b4a4718bac2115294660412`  
		Last Modified: Tue, 17 Mar 2026 16:27:48 GMT  
		Size: 17.3 MB (17292686 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb98ad1fb8dbf4aef5b8e7f53e9995cd77eebbab70af8a6e12f630c4051c1901`  
		Last Modified: Tue, 17 Mar 2026 16:27:47 GMT  
		Size: 23.0 KB (22968 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:4-trixie` - linux; ppc64le

```console
$ docker pull ruby@sha256:53943762d8327774ccd7a53598b1962562f79d03f758bc471b3fb8de36c737d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **428.9 MB (428851476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3015eb23fa9929cb7b95e7d14a787c3979e28dcd854259fcf86534f0bca52ba5`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 21:23:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 25 Feb 2026 02:58:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 25 Feb 2026 06:21:59 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Wed, 25 Feb 2026 13:28:27 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 25 Feb 2026 13:31:53 GMT
ENV LANG=C.UTF-8
# Wed, 25 Feb 2026 13:31:53 GMT
ENV RUBY_VERSION=4.0.1
# Wed, 25 Feb 2026 13:31:53 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/4.0/ruby-4.0.1.tar.xz
# Wed, 25 Feb 2026 13:31:53 GMT
ENV RUBY_DOWNLOAD_SHA256=0531fe57dfdb56bf591620d2450642ea0e0964f3512a6ebee7dc9305de69395f
# Wed, 25 Feb 2026 13:31:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 		${rustArch:+--enable-zjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 25 Feb 2026 13:31:53 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 25 Feb 2026 13:31:53 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 25 Feb 2026 13:31:53 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 25 Feb 2026 13:31:53 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 25 Feb 2026 13:31:53 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:468eb7cd0e9ceb9e5b1c4c9daadd36c2fd1f1ee82c667dc1a7d70fa95600a20f`  
		Last Modified: Tue, 24 Feb 2026 18:45:11 GMT  
		Size: 53.1 MB (53112261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b88c878e5079331d2b0e1bf13313604e6e446232728ee7b159499795ff9def2`  
		Last Modified: Tue, 24 Feb 2026 21:23:39 GMT  
		Size: 27.0 MB (27004375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8078b8ed13f55a8d2e3bc098e87fe680e2a4289c11315d3e460db7bcd51cc93f`  
		Last Modified: Wed, 25 Feb 2026 02:59:03 GMT  
		Size: 73.0 MB (73022125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08b482eeddecf4913e539ab73ef4ec7381bf7e26b57350ac4748a751869d3c04`  
		Last Modified: Wed, 25 Feb 2026 06:23:39 GMT  
		Size: 231.2 MB (231182217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:318b652ca4594c86d95540a30a540260748093c675f46cee7851d1a9db5c80ee`  
		Last Modified: Wed, 25 Feb 2026 13:32:38 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a62caf92865eeb079d77bdd58845d4d3b9892d9674e710bbd50f58165fc46b`  
		Last Modified: Wed, 25 Feb 2026 13:32:40 GMT  
		Size: 44.5 MB (44530165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acebec0123587263210b51f336b7a5f7c37edec7f8c67978034ef9a0667ad8cf`  
		Last Modified: Wed, 25 Feb 2026 13:32:38 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:4-trixie` - unknown; unknown

```console
$ docker pull ruby@sha256:6c8c7c2cc09423ba89688a3428a346f5d8827c04e691f732c74a9b87b2f2f28e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17331704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fab021b6913bfe7ff7362b6909c9fc8395dce3674ec92e46443324898cbab7f`

```dockerfile
```

-	Layers:
	-	`sha256:1bea011fe2385fefbbca8f06eecf85373006e4468f662b54035740bc236d43ba`  
		Last Modified: Wed, 25 Feb 2026 13:32:39 GMT  
		Size: 17.3 MB (17308606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:781896658bf2393c272ff64ff096f2d9bedca16bbc8f1682f3bd894ea6e0afe2`  
		Last Modified: Wed, 25 Feb 2026 13:32:38 GMT  
		Size: 23.1 KB (23098 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:4-trixie` - linux; riscv64

```console
$ docker pull ruby@sha256:30443d331842eacb3beda67130570d2841d8ab2baccce2b28fc9e0fe1bbbdb37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **506.6 MB (506616857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaebcc28baccacb1df1e3f6e5d932509910290a1a69edebe94d8a8f2a7c1cba0`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1771804800'
# Thu, 26 Feb 2026 21:43:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Sat, 28 Feb 2026 19:58:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 03 Mar 2026 00:52:23 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Wed, 04 Mar 2026 03:26:43 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 04 Mar 2026 05:21:12 GMT
ENV LANG=C.UTF-8
# Wed, 04 Mar 2026 05:21:12 GMT
ENV RUBY_VERSION=4.0.1
# Wed, 04 Mar 2026 05:21:12 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/4.0/ruby-4.0.1.tar.xz
# Wed, 04 Mar 2026 05:21:12 GMT
ENV RUBY_DOWNLOAD_SHA256=0531fe57dfdb56bf591620d2450642ea0e0964f3512a6ebee7dc9305de69395f
# Wed, 04 Mar 2026 05:21:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 		${rustArch:+--enable-zjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 04 Mar 2026 05:21:12 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 04 Mar 2026 05:21:12 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 04 Mar 2026 05:21:12 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Mar 2026 05:21:13 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 04 Mar 2026 05:21:13 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:3be247472b67578a1d05739722d8adeca41098796e5d6210800176db58046fa7`  
		Last Modified: Tue, 24 Feb 2026 18:57:42 GMT  
		Size: 47.8 MB (47776936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:115c3a1cec8ab5f3346656c92bb6a04391222dacf945336ca2f360cb9afa1d32`  
		Last Modified: Thu, 26 Feb 2026 21:45:21 GMT  
		Size: 25.0 MB (24951819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be1aad3c88d849328eee587bd71226c07edf0e2f5081fc7ec8dc66c3ee7e1d0c`  
		Last Modified: Sat, 28 Feb 2026 20:02:17 GMT  
		Size: 66.7 MB (66662373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b768d5fae96437f49666800f255760898ac05cd739d42fa59bdb1cc293ec5a79`  
		Last Modified: Tue, 03 Mar 2026 01:08:01 GMT  
		Size: 323.0 MB (322984592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff249f5fe17ba9436787aceb728a3c1da155771d14806176f46ba14be278c741`  
		Last Modified: Wed, 04 Mar 2026 05:29:33 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a24b6fdb2bd4d56cfebdf1e1758b83e17656bf317179a3f749724ec276bf0bb`  
		Last Modified: Wed, 04 Mar 2026 05:29:42 GMT  
		Size: 44.2 MB (44240803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6cdd5e637508df478acc312d555830b9fbedd369a1c40afc7181275290927ff`  
		Last Modified: Wed, 04 Mar 2026 05:29:32 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:4-trixie` - unknown; unknown

```console
$ docker pull ruby@sha256:8012301729dd02321eb3253d030433e0bf9a5f4cd1c759550bf6b7f608bff292
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 MB (17402294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9392e087e8ab138f1195a37ad0a1d2768a98c96f2872ec0f801ba0030d8b9197`

```dockerfile
```

-	Layers:
	-	`sha256:c8c54d482401f4f70ba48bbaf0af060e8199e5d09c9287e15fecc1c9ca3d2387`  
		Last Modified: Wed, 04 Mar 2026 05:29:37 GMT  
		Size: 17.4 MB (17379195 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1fd77da4ef1ca99f8fe70b12b9d3bd914069e632d812fd232e29a782dc9edc31`  
		Last Modified: Wed, 04 Mar 2026 05:29:32 GMT  
		Size: 23.1 KB (23099 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:4-trixie` - linux; s390x

```console
$ docker pull ruby@sha256:85397d00bc2487a47e508086326685a60ca38aee6f58169224d4496029bf4b70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **395.8 MB (395754948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67b327d2ebf52aa8c29a2deff637771899339178fc8c7a653f3c3955bcfc3152`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 23:45:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 17 Mar 2026 01:34:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 17 Mar 2026 02:17:59 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Tue, 17 Mar 2026 09:22:37 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 17 Mar 2026 16:27:38 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 16:27:38 GMT
ENV RUBY_VERSION=4.0.2
# Tue, 17 Mar 2026 16:27:38 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/4.0/ruby-4.0.2.tar.xz
# Tue, 17 Mar 2026 16:27:38 GMT
ENV RUBY_DOWNLOAD_SHA256=4618db85bb9ec04d8152d0099db488694a3d3c4f52106625e4ad547f1318db87
# Tue, 17 Mar 2026 16:27:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 		${rustArch:+--enable-zjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 17 Mar 2026 16:27:38 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 17 Mar 2026 16:27:38 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 17 Mar 2026 16:27:38 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 16:27:39 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 17 Mar 2026 16:27:39 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:7bc76783a6155f9347e92234e4b5c38bd02638c6de782f4623d0736c769250f0`  
		Last Modified: Mon, 16 Mar 2026 21:52:57 GMT  
		Size: 49.4 MB (49364775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8371259f6819197ae08830e46db090d1aad241011f8c2483f8e3205359263dcd`  
		Last Modified: Mon, 16 Mar 2026 23:45:50 GMT  
		Size: 26.8 MB (26803190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6990bcd0cd48258f05a5e1da913e50e516d08ed7812badfbb9d8451ec894a6a6`  
		Last Modified: Tue, 17 Mar 2026 01:34:59 GMT  
		Size: 68.6 MB (68628445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47057cfd6a92f3d99db284d930f4e069c4ad4f63f130f90e61f4d7667173d2e1`  
		Last Modified: Tue, 17 Mar 2026 02:19:02 GMT  
		Size: 206.6 MB (206580881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbe7a2ebe0299afce1aee34544143faa06cf7c73d66f574f9f397aa5fdd50e47`  
		Last Modified: Tue, 17 Mar 2026 09:32:28 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff829a15394a0b01b6fbd99434b9af596761b55b0431fdd5ddd25b9fb0943cf8`  
		Last Modified: Tue, 17 Mar 2026 16:29:50 GMT  
		Size: 44.4 MB (44377326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae03de571ce12b0692651f7b43cfdad7895bfae26e67c3c0b3d789636a67ae0a`  
		Last Modified: Tue, 17 Mar 2026 16:29:32 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:4-trixie` - unknown; unknown

```console
$ docker pull ruby@sha256:987ff5c51122cce2ff780352e1934a9d41ac7b9b4f8a778fe03bb3ec25bd79ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17123378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11eb7b2c73ed97647564283cb809e78ef948bfd2374304f80572854e13828cd6`

```dockerfile
```

-	Layers:
	-	`sha256:cf0628aebecc40a4d0364a9f0968ac36acc58eb467b75137c026aafcd4a587fa`  
		Last Modified: Tue, 17 Mar 2026 16:29:45 GMT  
		Size: 17.1 MB (17100352 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a2eb160c29f64657a19a764e08f366b54c32da422a50da476c3ff035a9f2c2c`  
		Last Modified: Tue, 17 Mar 2026 16:29:34 GMT  
		Size: 23.0 KB (23026 bytes)  
		MIME: application/vnd.in-toto+json
