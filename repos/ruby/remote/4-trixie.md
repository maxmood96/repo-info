## `ruby:4-trixie`

```console
$ docker pull ruby@sha256:ce53d8dac5d489c29f17f168267e811f9206423eb27ca6c4706853b6b9afd271
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
$ docker pull ruby@sha256:6379934adb867a82d7e9e048c6858a7bf14dd6b793bee33335d44df5f6899686
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **428.3 MB (428348704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2af93c8fec51f477327d632bfb2b955304a398ce8c2ffa25b69b4bdd031db550`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:47:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 01:23:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 02:40:01 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 03:58:29 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 30 Dec 2025 04:00:30 GMT
ENV LANG=C.UTF-8
# Tue, 30 Dec 2025 04:00:30 GMT
ENV RUBY_VERSION=4.0.0
# Tue, 30 Dec 2025 04:00:30 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/4.0/ruby-4.0.0.tar.xz
# Tue, 30 Dec 2025 04:00:30 GMT
ENV RUBY_DOWNLOAD_SHA256=a72bacee9de07283ebc19baa4ac243b193129f21aa4e168c7186fb1fe7d07fe1
# Tue, 30 Dec 2025 04:00:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 		${rustArch:+--enable-zjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 30 Dec 2025 04:00:30 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 30 Dec 2025 04:00:30 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 30 Dec 2025 04:00:30 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 04:00:30 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 30 Dec 2025 04:00:30 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:281b80c799ded5b9a390d2e8c59930db01ee395ab809dd34259897c660751f4e`  
		Last Modified: Mon, 29 Dec 2025 22:31:07 GMT  
		Size: 49.3 MB (49289587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15f14138abe4f09d3ef3953105144728056046ae469ae21e8e42749bacd67cca`  
		Last Modified: Mon, 29 Dec 2025 23:47:42 GMT  
		Size: 25.6 MB (25613989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:378c64c4458002be86f2d86c5768ae9ec0cff69afac7d1444e50206dc4566fa9`  
		Last Modified: Tue, 30 Dec 2025 01:24:00 GMT  
		Size: 67.8 MB (67777233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02e37abc533a09f86edcf3602251a61a6208ddaa131e1a1d5757e5f94a54d645`  
		Last Modified: Tue, 30 Dec 2025 02:41:24 GMT  
		Size: 236.0 MB (235979646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:060ef16f664a273625a35cb45d9ae956e6a4f9caa49d29eca1d5c5153cabc286`  
		Last Modified: Tue, 30 Dec 2025 04:00:57 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a3439cbf2f0308b5199bdefb1add336bdcb170e759dd3b17cfe02b73c1f8727`  
		Last Modified: Tue, 30 Dec 2025 04:01:14 GMT  
		Size: 49.7 MB (49687916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b77d3f9ecdfc04816375ca792a67fc8031bb603a7d22e35c5ac8aaa42b321fb3`  
		Last Modified: Tue, 30 Dec 2025 04:00:57 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:4-trixie` - unknown; unknown

```console
$ docker pull ruby@sha256:53a94387e6d28c73564a40ac50522275d0e14e00a2320195e53903a5063bde10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17344923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24796efce17d51329afd24a278dbfdbf178e5d3a3561d8da1bd9e68c017d0c06`

```dockerfile
```

-	Layers:
	-	`sha256:3dd265f23d5c0d605857e864d565cf2ae56e496a58eceaa81bd3480f24c16507`  
		Last Modified: Tue, 30 Dec 2025 07:01:56 GMT  
		Size: 17.3 MB (17321896 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1dd43659a7871d402379b3be8d6dc74b125a62be7803f526dcf90e434068b289`  
		Last Modified: Tue, 30 Dec 2025 07:01:57 GMT  
		Size: 23.0 KB (23027 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:4-trixie` - linux; arm variant v5

```console
$ docker pull ruby@sha256:dec7560d3efc90f78b44e02c249ed14daaea8126433306b23ff396c6bfef7eb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **385.6 MB (385561579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28fdeb821cb86d119255f877f58c5af4839bad48051e9edde1fbe2bc9f63a643`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 00:29:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 01:50:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 02:32:03 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 04:38:48 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 30 Dec 2025 04:41:26 GMT
ENV LANG=C.UTF-8
# Tue, 30 Dec 2025 04:41:26 GMT
ENV RUBY_VERSION=4.0.0
# Tue, 30 Dec 2025 04:41:26 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/4.0/ruby-4.0.0.tar.xz
# Tue, 30 Dec 2025 04:41:26 GMT
ENV RUBY_DOWNLOAD_SHA256=a72bacee9de07283ebc19baa4ac243b193129f21aa4e168c7186fb1fe7d07fe1
# Tue, 30 Dec 2025 04:41:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 		${rustArch:+--enable-zjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 30 Dec 2025 04:41:26 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 30 Dec 2025 04:41:26 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 30 Dec 2025 04:41:26 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 04:41:26 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 30 Dec 2025 04:41:26 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:34295e8c92d32055cf38cee5aec380c4d26fb9f87d9d69deffe81403a9d5a203`  
		Last Modified: Mon, 29 Dec 2025 22:26:50 GMT  
		Size: 47.4 MB (47448770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13cf1b0fd719c142e9016b7b007d0d982443d9aeedfc75f9de33d17efc3342d9`  
		Last Modified: Tue, 30 Dec 2025 00:29:32 GMT  
		Size: 24.3 MB (24345729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2a515687a5a3da2827aa6a3b8071d1f515ed0d5cba1dbfad9af02797c060c18`  
		Last Modified: Tue, 30 Dec 2025 01:51:10 GMT  
		Size: 65.3 MB (65317909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68072cf099e255739c5dbed1ad6775d11fb11c6212d9e07f276471ca4f471e33`  
		Last Modified: Tue, 30 Dec 2025 03:14:24 GMT  
		Size: 205.7 MB (205708113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa371b4fa2fe384551b4720b1516fc0fe1fa6259c71eeb56b1ed9bf579cd3277`  
		Last Modified: Tue, 30 Dec 2025 04:41:56 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1acd0365b11585869fdfa02da5dcaac01fb42cfa760deb115c3bbb2c2f03c897`  
		Last Modified: Tue, 30 Dec 2025 04:41:58 GMT  
		Size: 42.7 MB (42740725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a33f593922ca1e1ac4078016f1535e7afd0397f4a1973da88d8f4cad5126189`  
		Last Modified: Tue, 30 Dec 2025 04:41:56 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:4-trixie` - unknown; unknown

```console
$ docker pull ruby@sha256:776476321f4d9550756bf106c01373ba3a837680985ce70024acdec162beb883
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17107299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4beb955e18b5a2fe18af206788d204943bca54f4e23c381764d570f48116db0`

```dockerfile
```

-	Layers:
	-	`sha256:565f1d750351b807114c6079d8701f34686987dfb5644b577a1efab767f2f4d8`  
		Last Modified: Tue, 30 Dec 2025 07:02:13 GMT  
		Size: 17.1 MB (17084134 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78e15f5993450ad7e3f2f7013846be44b053e4044e7ea8cf566cc5795fd4941d`  
		Last Modified: Tue, 30 Dec 2025 07:02:14 GMT  
		Size: 23.2 KB (23165 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:4-trixie` - linux; arm variant v7

```console
$ docker pull ruby@sha256:d90113a47f8ad5f4cd8f1cc9104d1326b71c2d7d34e360395e9881e051ce892e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.9 MB (367910704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bfe3a38c37e8758454ae96266129d947adc9469280a3c422a377d68576a86da`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 00:35:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 02:07:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 02:35:49 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 05:06:27 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 30 Dec 2025 05:08:46 GMT
ENV LANG=C.UTF-8
# Tue, 30 Dec 2025 05:08:46 GMT
ENV RUBY_VERSION=4.0.0
# Tue, 30 Dec 2025 05:08:46 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/4.0/ruby-4.0.0.tar.xz
# Tue, 30 Dec 2025 05:08:46 GMT
ENV RUBY_DOWNLOAD_SHA256=a72bacee9de07283ebc19baa4ac243b193129f21aa4e168c7186fb1fe7d07fe1
# Tue, 30 Dec 2025 05:08:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 		${rustArch:+--enable-zjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 30 Dec 2025 05:08:46 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 30 Dec 2025 05:08:46 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 30 Dec 2025 05:08:46 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 05:08:46 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 30 Dec 2025 05:08:46 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:d20050ceedb84a03f8a4208462819500ff366fe1a69cdbba74b118aa8a38a87a`  
		Last Modified: Mon, 29 Dec 2025 22:28:10 GMT  
		Size: 45.7 MB (45718317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1468c2ee0f43e81d6e097b24054de66ae95db50d77cef08d1eabe51a5dab43cd`  
		Last Modified: Tue, 30 Dec 2025 00:36:02 GMT  
		Size: 23.6 MB (23619911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fa494d16bf7a563003db4c95fa508ca504a77c791075afbc16c7f5a1be17761`  
		Last Modified: Tue, 30 Dec 2025 02:07:44 GMT  
		Size: 62.7 MB (62713662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ed5488c5068f5c77a6b4b6f6b02bab38e7073441d08f85d6bab0a94c1cae889`  
		Last Modified: Tue, 30 Dec 2025 02:36:47 GMT  
		Size: 193.3 MB (193259793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:071b3b1c5801ebc5bc2fed8d268ea9221a07571d35b612228a467b8d788d28bc`  
		Last Modified: Tue, 30 Dec 2025 05:09:12 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a6c37d439ed5b1a7de3ac288a29e6879396d4534c5e6b4ca740fcdb41e73c26`  
		Last Modified: Tue, 30 Dec 2025 05:09:16 GMT  
		Size: 42.6 MB (42598688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2c684446498eb774e5d226903fbe5aeaad2ec9540a69c343538016adce86d7d`  
		Last Modified: Tue, 30 Dec 2025 05:09:13 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:4-trixie` - unknown; unknown

```console
$ docker pull ruby@sha256:0eb9a6d27d6b1bc6ee7936dd9716f3df7e5a3b8b7192cf82b12d5c3818851ff5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17113089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f68c8e04b95b80e5bc3766e537017f4e31f1632f5176f9d0558e46967018e22c`

```dockerfile
```

-	Layers:
	-	`sha256:f47e7914d326587e3e30f3b66fe9a059f174acc59b3683c606cbb1bf0d727894`  
		Last Modified: Tue, 30 Dec 2025 07:02:30 GMT  
		Size: 17.1 MB (17089924 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef43910e74ee5b6341ccd037cbb82c6295013d80975bed7cbdd9b296a5b2f1e0`  
		Last Modified: Tue, 30 Dec 2025 07:02:31 GMT  
		Size: 23.2 KB (23165 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:4-trixie` - linux; arm64 variant v8

```console
$ docker pull ruby@sha256:22860f3514c83e30fd8f6094810a12707c621ba5633afb2be7fbad307ea1d591
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **417.9 MB (417929081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b39f501670cb6b9f3e122640c4ba67b4ccb33d6e967e08e6dd394841a73a96f`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:47:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 01:25:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 02:38:57 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 04:01:18 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 30 Dec 2025 04:03:26 GMT
ENV LANG=C.UTF-8
# Tue, 30 Dec 2025 04:03:26 GMT
ENV RUBY_VERSION=4.0.0
# Tue, 30 Dec 2025 04:03:26 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/4.0/ruby-4.0.0.tar.xz
# Tue, 30 Dec 2025 04:03:26 GMT
ENV RUBY_DOWNLOAD_SHA256=a72bacee9de07283ebc19baa4ac243b193129f21aa4e168c7186fb1fe7d07fe1
# Tue, 30 Dec 2025 04:03:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 		${rustArch:+--enable-zjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 30 Dec 2025 04:03:26 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 30 Dec 2025 04:03:26 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 30 Dec 2025 04:03:26 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 04:03:26 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 30 Dec 2025 04:03:26 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:5785abec2864dcd8d343ccd872458a50ffb2a61739bc46a79709c68c455cb8fc`  
		Last Modified: Mon, 29 Dec 2025 22:30:57 GMT  
		Size: 49.7 MB (49650193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dce2d1ead36d47118631ae52b25fc39c1aa005c68093dd34e456927908318c52`  
		Last Modified: Mon, 29 Dec 2025 23:47:57 GMT  
		Size: 25.0 MB (25021045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5d9404781930ac9b1a80bc4d3e616b480ed1eeab70b8545e9988a3a11d00783`  
		Last Modified: Tue, 30 Dec 2025 01:26:07 GMT  
		Size: 67.6 MB (67583784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ba313b9abd0e83099c56d61a9c6454295140adbe52f5e05df85e9dc33574fe4`  
		Last Modified: Tue, 30 Dec 2025 02:39:58 GMT  
		Size: 226.1 MB (226105906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b483cfb6d1db67a385a2c3e8ddd8c5967aa924d5cd0e8f704a7a4305c0fdc2b`  
		Last Modified: Tue, 30 Dec 2025 04:03:56 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc1311c9cf338181012c4e421d8df31b33c60c5cb2d3a906bdd7588a581bb028`  
		Last Modified: Tue, 30 Dec 2025 04:04:00 GMT  
		Size: 49.6 MB (49567820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dc9a34530cfaf4c14f7ecc674d52016d28b2d8aa186f3babfe752652d68a1ef`  
		Last Modified: Tue, 30 Dec 2025 04:03:56 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:4-trixie` - unknown; unknown

```console
$ docker pull ruby@sha256:53a9679dd404c77fdb43336b034149bda8460ee84c6b8e8b50997f2c013532b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 MB (17429458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18cf799c63e9c0f9c5ad345296969e57a8c304d5a8ada2264d52daa51e7f3ea1`

```dockerfile
```

-	Layers:
	-	`sha256:ab01978bcce7c7da8fc0fb6ce050c59c9f5e27ae33ec85b7adee835cdf72d4eb`  
		Last Modified: Tue, 30 Dec 2025 07:02:46 GMT  
		Size: 17.4 MB (17406250 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:893f99a53db20acf4d70deadac0658cc2a1639dca26730cbeafad2e8472f7ef2`  
		Last Modified: Tue, 30 Dec 2025 07:02:47 GMT  
		Size: 23.2 KB (23208 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:4-trixie` - linux; 386

```console
$ docker pull ruby@sha256:02ace14cb9fb4d3401257c8a18aeadd4fd4edb4c186469faa90781962ef2017a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **429.9 MB (429933404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b0234af36f21a3bb811dee45effc0b8e1cd50f8664ac570a7cc48b383026beb`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:47:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 00:34:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 01:52:40 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 02:43:33 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 30 Dec 2025 02:45:35 GMT
ENV LANG=C.UTF-8
# Tue, 30 Dec 2025 02:45:35 GMT
ENV RUBY_VERSION=4.0.0
# Tue, 30 Dec 2025 02:45:35 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/4.0/ruby-4.0.0.tar.xz
# Tue, 30 Dec 2025 02:45:35 GMT
ENV RUBY_DOWNLOAD_SHA256=a72bacee9de07283ebc19baa4ac243b193129f21aa4e168c7186fb1fe7d07fe1
# Tue, 30 Dec 2025 02:45:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 		${rustArch:+--enable-zjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 30 Dec 2025 02:45:35 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 30 Dec 2025 02:45:35 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 30 Dec 2025 02:45:35 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 02:45:35 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 30 Dec 2025 02:45:35 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:7ba68d5e03a08e607fe00d0a9f5d3925adc34700fc401165e5513c0d55ae9d2e`  
		Last Modified: Mon, 29 Dec 2025 22:27:39 GMT  
		Size: 50.8 MB (50801684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fabb00c990eb2d1ca8a4037bb0b9c6e0d0d8b6c6fb47372c8ec75cd65588cdd8`  
		Last Modified: Mon, 29 Dec 2025 23:47:40 GMT  
		Size: 26.8 MB (26776375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fc67c159b6d502873d04e7b21d326f226b1fd89576f5d5cd1b817d74d68fee4`  
		Last Modified: Tue, 30 Dec 2025 00:34:34 GMT  
		Size: 69.8 MB (69794792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93b502d5bfabc8613c27931d0c9c661d4d6c91e79ad218bc5c52c7134f82acd5`  
		Last Modified: Tue, 30 Dec 2025 01:53:41 GMT  
		Size: 240.1 MB (240075297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43cac5c40d93e67bcdb40ba141fc2d80b024b0a1a70ab19b3c6d7e563bc4f732`  
		Last Modified: Tue, 30 Dec 2025 02:46:00 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2afea1f40fb33f3dd81d23aea8d2d1ddec2c5835520e3ab1e9edc8f2c95b65f`  
		Last Modified: Tue, 30 Dec 2025 02:46:03 GMT  
		Size: 42.5 MB (42484922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:785c18df91c6bdb917c8de219126680860c913dbffa86761b5b5e242edbbeae1`  
		Last Modified: Tue, 30 Dec 2025 02:46:00 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:4-trixie` - unknown; unknown

```console
$ docker pull ruby@sha256:8e416cfc209c925097e0700d70b147c6d35ec639b0435abeaee4d9f81dc86103
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17314435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce2cfb9b60fd6be5912213de8dfb8c928ec60f824edd43f7827bb85628d12048`

```dockerfile
```

-	Layers:
	-	`sha256:045500844a5bbf29c1a820073240a3439934e609d1e4902793eca48ca064b2e2`  
		Last Modified: Tue, 30 Dec 2025 04:05:14 GMT  
		Size: 17.3 MB (17291464 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b547e2de316957ab19d86baaa1cec83d4db527abb1432cf1fdd5ec91e0ad641`  
		Last Modified: Tue, 30 Dec 2025 04:05:15 GMT  
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
$ docker pull ruby@sha256:0b89f393c65c527fafe47caea46a555dff603eff4aff35de5636231fb0bc27ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **506.5 MB (506514481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bb8f73881318770950bf3849428bdf049aae61d902741e866a29adc1dd90d1c`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1765152000'
# Thu, 11 Dec 2025 08:39:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Sun, 14 Dec 2025 08:46:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 15 Dec 2025 06:42:20 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Tue, 16 Dec 2025 05:18:48 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 26 Dec 2025 05:01:25 GMT
ENV LANG=C.UTF-8
# Fri, 26 Dec 2025 05:01:25 GMT
ENV RUBY_VERSION=4.0.0
# Fri, 26 Dec 2025 05:01:25 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/4.0/ruby-4.0.0.tar.xz
# Fri, 26 Dec 2025 05:01:25 GMT
ENV RUBY_DOWNLOAD_SHA256=a72bacee9de07283ebc19baa4ac243b193129f21aa4e168c7186fb1fe7d07fe1
# Fri, 26 Dec 2025 05:01:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 		${rustArch:+--enable-zjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 26 Dec 2025 05:01:25 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 26 Dec 2025 05:01:25 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 26 Dec 2025 05:01:25 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Dec 2025 05:01:25 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 26 Dec 2025 05:01:25 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:e8961870af39130e72e5dc66bd3574bb074dffc7989fd5e909f55fefadae8a30`  
		Last Modified: Tue, 09 Dec 2025 02:05:05 GMT  
		Size: 47.8 MB (47771135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2088c9d98910c38f13b1907a28647a9e78cc7ea821df93ab45af07ce2813dcab`  
		Last Modified: Thu, 11 Dec 2025 08:40:59 GMT  
		Size: 25.0 MB (24953834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a60a42ed8727e43dc5cd180abfcc19a18468941394808f724b1f4dc00352352`  
		Last Modified: Sun, 14 Dec 2025 08:50:41 GMT  
		Size: 66.7 MB (66660499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d89b1e152c7f5b34657f3a6e97a87170ecf850bc400696de74b3929bc238f0d3`  
		Last Modified: Mon, 15 Dec 2025 06:59:37 GMT  
		Size: 322.9 MB (322886042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2114268f3d73ac6e6812ed9e846feb368dc8488be99494d1d9229005370e088b`  
		Last Modified: Tue, 16 Dec 2025 07:23:03 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b3f2500170f2b442e0086af733f46b93d16f3ca3182af12564ff2bdc0fb7ce6`  
		Last Modified: Fri, 26 Dec 2025 05:10:20 GMT  
		Size: 44.2 MB (44242638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:719f9880861ec26a8da459a4684a0db49f62c5a4241a025f93b4e4a08a1272d5`  
		Last Modified: Fri, 26 Dec 2025 05:10:16 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:4-trixie` - unknown; unknown

```console
$ docker pull ruby@sha256:774efbc579a228f03bf078ecb5c94f4f6281702f82f7eb9c6d29381bf3dab204
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 MB (17401163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54ea1a2de3879eb6a84a3519bc262ddfbd02db2f54269610f9a106d776a3e375`

```dockerfile
```

-	Layers:
	-	`sha256:415f516719086c97e41c91076a70fed7944c4eac3656ce24ff946666e3cee8f6`  
		Last Modified: Fri, 26 Dec 2025 07:01:03 GMT  
		Size: 17.4 MB (17378064 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4905c0981c14d9ce7966c1baff7a8f4ae202b14a044bd96028f2b0c3ee1fa3b9`  
		Last Modified: Fri, 26 Dec 2025 07:01:04 GMT  
		Size: 23.1 KB (23099 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:4-trixie` - linux; s390x

```console
$ docker pull ruby@sha256:555bf8681fb53241113470ca0e9d79ebe97fb68f66c91ece4377de10e8a68747
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **395.6 MB (395593976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4133a9ee3d209148ff9049f92441c58bb1f2648654e4c3b659bfbbdd32a1006`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 04:14:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 06:03:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 06:20:30 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 08:18:56 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 30 Dec 2025 08:21:59 GMT
ENV LANG=C.UTF-8
# Tue, 30 Dec 2025 08:21:59 GMT
ENV RUBY_VERSION=4.0.0
# Tue, 30 Dec 2025 08:21:59 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/4.0/ruby-4.0.0.tar.xz
# Tue, 30 Dec 2025 08:21:59 GMT
ENV RUBY_DOWNLOAD_SHA256=a72bacee9de07283ebc19baa4ac243b193129f21aa4e168c7186fb1fe7d07fe1
# Tue, 30 Dec 2025 08:21:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 		${rustArch:+--enable-zjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 30 Dec 2025 08:21:59 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 30 Dec 2025 08:21:59 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 30 Dec 2025 08:21:59 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 08:22:00 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 30 Dec 2025 08:22:00 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:85bc4a4d1f4e52a33d42907057e0ab87c5eb2560b332d94f6e9d7da79c0c76b8`  
		Last Modified: Tue, 30 Dec 2025 03:26:29 GMT  
		Size: 49.3 MB (49345959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7ac6efd7cfec1d611dcf0011d64b56f69fe5f6fe47195e090cb8c04e2584e93`  
		Last Modified: Tue, 30 Dec 2025 04:14:36 GMT  
		Size: 26.8 MB (26786464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:978ec2f50f1462efd64a546370da30e382c7f6044ad53993a4af33689f25341a`  
		Last Modified: Tue, 30 Dec 2025 06:04:24 GMT  
		Size: 68.6 MB (68630336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7510272003138b4eb0f922cea049042f2f1e20a0f674fdc6eeff4c3134a833ca`  
		Last Modified: Tue, 30 Dec 2025 06:25:45 GMT  
		Size: 206.5 MB (206470896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:920e0557073decf6dbe148fa0b1954ba71d0524929febbc78cfdd84d22df8141`  
		Last Modified: Tue, 30 Dec 2025 08:22:42 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f60fc3736939c6efd3cfd410573ffd5c2ce1e3c4a7ee37d65b4c45bcdedb415`  
		Last Modified: Tue, 30 Dec 2025 08:22:46 GMT  
		Size: 44.4 MB (44359988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4db8d1e221ce7289312f83ed7867a26146c81e93d066efd940414a5cdc626d2b`  
		Last Modified: Tue, 30 Dec 2025 08:22:42 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:4-trixie` - unknown; unknown

```console
$ docker pull ruby@sha256:10770317eb0a63310114cdf8a978dcc423b2ddd942b0e487321d0d607a497f8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17122156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a502e5c6f282a10b7411a8fa154b2458e735215018eb9090ab7ee6c35c306aa`

```dockerfile
```

-	Layers:
	-	`sha256:5f80bc95a09045578570b0182edb2bb2f14e166d7fa1133f11b107f2123c8f08`  
		Last Modified: Tue, 30 Dec 2025 10:00:56 GMT  
		Size: 17.1 MB (17099129 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c01006badc5995ae4652295237a918457440ac7c9586b219f636eaaafeacfec`  
		Last Modified: Tue, 30 Dec 2025 10:00:57 GMT  
		Size: 23.0 KB (23027 bytes)  
		MIME: application/vnd.in-toto+json
