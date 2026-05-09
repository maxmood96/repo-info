## `ruby:3-bookworm`

```console
$ docker pull ruby@sha256:d577a7f848f3b66ea0ef482e1b7d1604d2abf21e9abc87fe27f5e511dddef0c3
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

### `ruby:3-bookworm` - linux; amd64

```console
$ docker pull ruby@sha256:03af893543f4b396f101b80e3093a6bfbbf9fd0bdaba8a03e27daea24d55915e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **390.1 MB (390057173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ac2ea87f930d13af2e79f919fe7b6a39b5a2b374bae67f9205fd4123720d361`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:40:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:26:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 21:16:55 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 22:45:01 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 08 May 2026 22:47:07 GMT
ENV LANG=C.UTF-8
# Fri, 08 May 2026 22:47:07 GMT
ENV RUBY_VERSION=3.4.9
# Fri, 08 May 2026 22:47:07 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Fri, 08 May 2026 22:47:07 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Fri, 08 May 2026 22:47:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 08 May 2026 22:47:07 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 08 May 2026 22:47:07 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 08 May 2026 22:47:07 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 22:47:07 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 08 May 2026 22:47:07 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:9104793a826a01456b0ba567a92064e85a029816661fbb4524da7913f0123ab5`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 48.5 MB (48488676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d055cea50c88c57fc27fcd44845ebabfe5b830ea8a0a621b89d38a2b650b7ff3`  
		Last Modified: Fri, 08 May 2026 19:40:29 GMT  
		Size: 24.0 MB (24042180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0869e5c4dac5849d3555a38db741288a16528478145da8dcb95b8dba2464d55d`  
		Last Modified: Fri, 08 May 2026 20:26:25 GMT  
		Size: 64.4 MB (64397036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a38666e026a9ba370d6b97aece24065a5298edbcb9f76e967a0a2633f72ead24`  
		Last Modified: Fri, 08 May 2026 21:17:33 GMT  
		Size: 211.6 MB (211580060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:424efaf2745ebcdd0e9b5c480a8f88390033118e17ec9dcffbc063ac0f609edd`  
		Last Modified: Fri, 08 May 2026 22:47:25 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b5bfead92e96dbf77bfdd00ccd1b3e1b589153b094d2e8a0441d0ef1514cf81`  
		Last Modified: Fri, 08 May 2026 22:47:27 GMT  
		Size: 41.5 MB (41548887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebab025f5a7e25f71eed0753845f4557009b8bc273a3f1ffd52d5a713f9180b2`  
		Last Modified: Fri, 08 May 2026 22:47:25 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:429b60ae1abfd907277ec13d73b3484c9f6f4b923be751b1c2304cfecf9c5315
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (16006633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d37589890c1bb1dc1a01fe4ef1c4a28db1f9b1f483e11c8e36ca6adc7af8338`

```dockerfile
```

-	Layers:
	-	`sha256:ea849e88cafced46f3fe3a63c69b60b13d10347212e475c82678e6482bb71e52`  
		Last Modified: Fri, 08 May 2026 22:47:26 GMT  
		Size: 16.0 MB (15985130 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc7b9a2b4d7fe1006891e002ba4f2ff2c21e04c58b911b8ab3eb1ca40a9d15ee`  
		Last Modified: Fri, 08 May 2026 22:47:25 GMT  
		Size: 21.5 KB (21503 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-bookworm` - linux; arm variant v5

```console
$ docker pull ruby@sha256:3cde37c1582543c4f03b7f9edd5504649e8164de36c3aff2f1a9bcdee809e59b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.9 MB (352895837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a84efb0f5b8ba82b008dbfa94c8db5ec4765d04d692c857e7b3dfe5ab8e417d`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 20:57:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 21:56:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 22:13:27 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 22:52:43 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 08 May 2026 22:54:54 GMT
ENV LANG=C.UTF-8
# Fri, 08 May 2026 22:54:54 GMT
ENV RUBY_VERSION=3.4.9
# Fri, 08 May 2026 22:54:54 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Fri, 08 May 2026 22:54:54 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Fri, 08 May 2026 22:54:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 08 May 2026 22:54:54 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 08 May 2026 22:54:54 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 08 May 2026 22:54:54 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 22:54:54 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 08 May 2026 22:54:54 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:ec18a0651074f3ac740b1a061140a88c16cce1b8118aeae02a5868a4ebdd3ef3`  
		Last Modified: Fri, 08 May 2026 18:33:05 GMT  
		Size: 46.0 MB (46021587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c6a0421f0b3bd4d0ba350f2693e0eb96a367c792e68487d0d1bd64fd9b90938`  
		Last Modified: Fri, 08 May 2026 20:57:12 GMT  
		Size: 22.7 MB (22716396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fcd8dde96688af04e04a192eeb3519a53f8cb70ed393ae3996eb1202809d3d8`  
		Last Modified: Fri, 08 May 2026 21:56:33 GMT  
		Size: 62.0 MB (62008645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93bba1a20457dabb9421580ec0c5ab0a6aad8a1606c61d1e25e8ec2ab88fa2e2`  
		Last Modified: Fri, 08 May 2026 22:14:07 GMT  
		Size: 184.8 MB (184840663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61a5d59fe8c395815276658734d94e74ac078829c86f8f9a14d5da493ce88a6d`  
		Last Modified: Fri, 08 May 2026 22:55:12 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e44915ea6aa462bf2c6537ed2bbd31d755e1b6362e6ef0bd4413765047348c0c`  
		Last Modified: Fri, 08 May 2026 22:55:14 GMT  
		Size: 37.3 MB (37308211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfcdc3a0ed64b011d3d9c61b43baffd6b4b32a349887286521ad7f12f5c8302e`  
		Last Modified: Fri, 08 May 2026 22:55:12 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:f0cbd64fad4557e73ddc166780bebe4cb5d7d363c7e66192bf67f8afdbd24309
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.8 MB (15803722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bcb5fa5cd7fd78cc8be4e68552ba2b69e8376f28637674ace865250e70437f9`

```dockerfile
```

-	Layers:
	-	`sha256:c1a5638b01486991ba0811fc88d880fa2ce65a4034567f28c6daa1c723e78ab8`  
		Last Modified: Fri, 08 May 2026 22:55:13 GMT  
		Size: 15.8 MB (15782122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d66c2c6bab0bf0840ec61c21e69ee72208aa208454f294963fa5282d06bce21`  
		Last Modified: Fri, 08 May 2026 22:55:12 GMT  
		Size: 21.6 KB (21600 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-bookworm` - linux; arm variant v7

```console
$ docker pull ruby@sha256:8f4ae6829ee9e89b0b975faa32894a4fd4c971310f113bed2d5c47a276bd4a3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.4 MB (338431299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25a0aa7c90bc87e8709fca6fb468ca3546b360e8679bb5cb809365738d12d3a7`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:44:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 21:34:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 22:12:47 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 23:48:58 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 08 May 2026 23:51:08 GMT
ENV LANG=C.UTF-8
# Fri, 08 May 2026 23:51:08 GMT
ENV RUBY_VERSION=3.4.9
# Fri, 08 May 2026 23:51:08 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Fri, 08 May 2026 23:51:08 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Fri, 08 May 2026 23:51:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 08 May 2026 23:51:08 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 08 May 2026 23:51:08 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 08 May 2026 23:51:08 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 23:51:08 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 08 May 2026 23:51:08 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:752ba895535a5b96e621b623e0a11ff696fe28fb2110ab16de49e150423d0a89`  
		Last Modified: Fri, 08 May 2026 18:36:54 GMT  
		Size: 44.2 MB (44207696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b0504388ca2bf72a5fec3556b58015e5dce736337a948976b22cd4cce283cb0`  
		Last Modified: Fri, 08 May 2026 19:44:39 GMT  
		Size: 21.9 MB (21946392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbef2e4eed112ac2d8730e2603fe97cab1d0ce708d52061992fd2f72e1db7e12`  
		Last Modified: Fri, 08 May 2026 21:35:07 GMT  
		Size: 59.7 MB (59653543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d7eff5eea100df13a745e92b9a950fdfe28a9d8d117e60044d04691c9f2792e`  
		Last Modified: Fri, 08 May 2026 22:13:22 GMT  
		Size: 175.5 MB (175482472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca30251d5af2a8eb7842e850ae073c5ae9c89ccd5ee0426b2ee527755d9dab9`  
		Last Modified: Fri, 08 May 2026 23:51:27 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db51ed7649f4eb828d8e5af8fc2075ddb18791a60b3a9f7fc42202e13f193477`  
		Last Modified: Fri, 08 May 2026 23:51:29 GMT  
		Size: 37.1 MB (37140862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f8fe44c3b3027c042bc0050e2429eeabf17bcb30ea67ab348ce1552a559da48`  
		Last Modified: Fri, 08 May 2026 23:51:27 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:d04a1113d37fc6800da1d2d95ad3d243c6bc39f2ede8543c2f637fd10b039738
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.8 MB (15809199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3642709931ae000ed536072d4d1ebce1400131092467a210216942f11a0e51c`

```dockerfile
```

-	Layers:
	-	`sha256:01a38b4dd532d012382ce48964097049c10d7b48027d68ec7b958e17abc19699`  
		Last Modified: Fri, 08 May 2026 23:51:28 GMT  
		Size: 15.8 MB (15787598 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c39e2de753496ba280463f96f37dc1eec47315d31f4ef450509252e4026bb2a2`  
		Last Modified: Fri, 08 May 2026 23:51:27 GMT  
		Size: 21.6 KB (21601 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-bookworm` - linux; arm64 variant v8

```console
$ docker pull ruby@sha256:92fd96e9a2973f7bbed3356452ff2e1d7ba1aea7ddaa376ce4fc2fb5fd53d5f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **381.0 MB (381003730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:729116046bba915dacfc1010fe3fbaee56d04494062ea65c81655aad8ea81c1f`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:42:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:31:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 21:16:58 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 22:45:15 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 08 May 2026 22:47:16 GMT
ENV LANG=C.UTF-8
# Fri, 08 May 2026 22:47:16 GMT
ENV RUBY_VERSION=3.4.9
# Fri, 08 May 2026 22:47:16 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Fri, 08 May 2026 22:47:16 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Fri, 08 May 2026 22:47:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 08 May 2026 22:47:16 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 08 May 2026 22:47:16 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 08 May 2026 22:47:16 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 22:47:16 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 08 May 2026 22:47:16 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:8eda28c6ece628fdff982fd6c7c1cd1f5eeccc51cfd0a3ee9155b2ccbdcc68a3`  
		Last Modified: Fri, 08 May 2026 18:24:51 GMT  
		Size: 48.4 MB (48373150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19f56578c9577bd69a05b2319baacd770a986ae61a8568047ddd91db1a1893b4`  
		Last Modified: Fri, 08 May 2026 19:42:30 GMT  
		Size: 23.6 MB (23609357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd5c3bf1fab727b805a2f735f33789c10938680bdeb2f8922a44aa2738df91f`  
		Last Modified: Fri, 08 May 2026 20:32:11 GMT  
		Size: 64.5 MB (64479741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eed4832944bb2d9c7650aef5babd468bb68e1074f57006ca0880412d4a70c940`  
		Last Modified: Fri, 08 May 2026 21:17:38 GMT  
		Size: 203.1 MB (203103995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2009cf5742a80e47af6daae76940bd171fc6c8ca386e242fbaeef0700e301b4e`  
		Last Modified: Fri, 08 May 2026 22:47:34 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e7f8872d6a18e261ec5a45dc6fc306c37c4af7a0b69f461a13c8d5437ba9f1d`  
		Last Modified: Fri, 08 May 2026 22:47:36 GMT  
		Size: 41.4 MB (41437152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f417ee29a408130c390a3693fd9235dd8851760cfba3e2bc12c0ad49f87db189`  
		Last Modified: Fri, 08 May 2026 22:47:34 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:31f64739c72c4ff0c6c8f3b73af80e4c320280c02919f75091733f541e495876
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (16035269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df63f694842a9fdb6b87050f374f8e41f986d5fa4bf8bf74e3bf1e97c31f9414`

```dockerfile
```

-	Layers:
	-	`sha256:6a8bab529d8f2dd3db1ca70d26fb9c1fdba41046ed78318d351d209b5425daf7`  
		Last Modified: Fri, 08 May 2026 22:47:35 GMT  
		Size: 16.0 MB (16013644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9fef0d5283cc9d0176d175893eb075f7213dd0514233c84ef269dd1f12f5e7e5`  
		Last Modified: Fri, 08 May 2026 22:47:34 GMT  
		Size: 21.6 KB (21625 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-bookworm` - linux; 386

```console
$ docker pull ruby@sha256:ba02ffc9510e428854de3061bfe3f0986706175bd7e721e1a7b474efd7c21993
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **388.2 MB (388160286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31d107be017eb7c87d745f85d621fe0f1ad33442118a7766abe3ac7119162328`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:42:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 05:02:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 08:19:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 09:47:29 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 22 Apr 2026 09:49:31 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 09:49:31 GMT
ENV RUBY_VERSION=3.4.9
# Wed, 22 Apr 2026 09:49:31 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Wed, 22 Apr 2026 09:49:31 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Wed, 22 Apr 2026 09:49:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 22 Apr 2026 09:49:31 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 22 Apr 2026 09:49:31 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 22 Apr 2026 09:49:31 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 09:49:31 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 22 Apr 2026 09:49:31 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:1f607c56991d572a9c9e62692330777522b959fe17a14367be35d12959214fa4`  
		Last Modified: Wed, 22 Apr 2026 00:16:17 GMT  
		Size: 49.5 MB (49477718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5d771f6f5a1356deff0c1540de8894e5249a2f8c97ba7961a41235129f48c60`  
		Last Modified: Wed, 22 Apr 2026 01:42:30 GMT  
		Size: 24.9 MB (24875723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dd81f3dc271c0572c6da562bcce13d5c0a8f379729949fde98b0b1e57ca2e4c`  
		Last Modified: Wed, 22 Apr 2026 05:02:53 GMT  
		Size: 66.2 MB (66235084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd1be51e246f00329f40c9ef8eca7bc1cfa31a9c7c2682672c63705ce9f093cf`  
		Last Modified: Wed, 22 Apr 2026 08:20:11 GMT  
		Size: 210.5 MB (210480286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e0e2d32846846c361f93eeec2155c72d8ae6cf551c2f7019058dee2361ef58c`  
		Last Modified: Wed, 22 Apr 2026 09:49:52 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f8976d56a1f589610ec1d0d8f6b2afebfb6a755ad3fbe84560654aa6a1939b`  
		Last Modified: Wed, 22 Apr 2026 09:49:53 GMT  
		Size: 37.1 MB (37091144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95dc2932c9c81807339e788948255645457074d9e3bc3ad077568e66e1f847ed`  
		Last Modified: Wed, 22 Apr 2026 09:49:52 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:d11e053c809e723570567aad14125930bc22274a1f5900427aff7b5f39e0d8ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (15984823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4da2e0ce1f383b4f41e44f94c7e7f0e82dd98877edb187d7f5c97de3d68a232`

```dockerfile
```

-	Layers:
	-	`sha256:b8cd547c30fea4f5179af0565ffa991ac78f6a4564443bb4b8736e85809a4e17`  
		Last Modified: Wed, 22 Apr 2026 09:49:53 GMT  
		Size: 16.0 MB (15963351 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abc5ef7e584f86563b73e9b0b7d573eaa256c41ecee0306b72d74a59e655cf1e`  
		Last Modified: Wed, 22 Apr 2026 09:49:52 GMT  
		Size: 21.5 KB (21472 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-bookworm` - linux; mips64le

```console
$ docker pull ruby@sha256:03f6f9ab6226dc304be6d937aff24ebdf1ce2a79cb4929ab0cc55015b646f7b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.5 MB (364516487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:406d0ba837fbaa69d22681348f46f3e36b8e8a1fac158d8eedd1c0946ef8c715`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 13:38:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 18:49:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 19:30:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 Apr 2026 01:07:27 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 23 Apr 2026 01:34:41 GMT
ENV LANG=C.UTF-8
# Thu, 23 Apr 2026 01:34:41 GMT
ENV RUBY_VERSION=3.4.9
# Thu, 23 Apr 2026 01:34:41 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Thu, 23 Apr 2026 01:34:41 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Thu, 23 Apr 2026 01:34:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 23 Apr 2026 01:34:41 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 23 Apr 2026 01:34:41 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 23 Apr 2026 01:34:41 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2026 01:34:43 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 23 Apr 2026 01:34:43 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:d3be957b775aeb19be93537211a85a2a31f49a07f3bbc6044dcea43e1c8ad87b`  
		Last Modified: Wed, 22 Apr 2026 01:25:51 GMT  
		Size: 48.8 MB (48782445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:689fafc394c7107b6f97558e80faf7c6aa5a2d625bf130259c59cbe1f85ed9fb`  
		Last Modified: Wed, 22 Apr 2026 13:39:30 GMT  
		Size: 23.6 MB (23615606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:451e7b3cb9c9d1c48a12fd45433b4710af87bfecf6744a09df7916580c67c305`  
		Last Modified: Wed, 22 Apr 2026 18:50:27 GMT  
		Size: 63.3 MB (63309466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bdfe0f4d11baf93a8ee6e3ae772ec399c6c110426b184f4e14832ebf0dd0047`  
		Last Modified: Wed, 22 Apr 2026 19:33:56 GMT  
		Size: 190.3 MB (190323428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca723e8e8976246a48dd9a535851547fa4a1e4cccdf135cb001e25cd832ae56f`  
		Last Modified: Thu, 23 Apr 2026 01:21:33 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:982ef2c413a3c329b5a618a145258ffc1a7c0f98bc65e12896bf399c4c1a2fe8`  
		Last Modified: Thu, 23 Apr 2026 01:35:53 GMT  
		Size: 38.5 MB (38485208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4af6dd7da87039195bfadba414618aa8852ef87b1903518f4a0900e70b6f74ea`  
		Last Modified: Thu, 23 Apr 2026 01:35:49 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:91e2b5929550c91fd40b8837134abef0221bbb97bf63f283879ffc724e0e05e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.4 KB (21351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6870f64cbeb2b0f765ba1e06e45dc94f918d3ec7b3a276a1eda18ef91822d531`

```dockerfile
```

-	Layers:
	-	`sha256:ad4017fce0d13557bc30c94778acd7965d12c248e53d7913ee81f55f2c56dad8`  
		Last Modified: Thu, 23 Apr 2026 01:35:49 GMT  
		Size: 21.4 KB (21351 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-bookworm` - linux; ppc64le

```console
$ docker pull ruby@sha256:ce0674f9fd73b7f56a34e558268158717ed58adbf4d46a27e31fde5a7f98b4c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **401.4 MB (401429165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe86e1c5929a13c4ea09facae8ba0e069de8d502c7671b2a595f591e76ae2cdd`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 03:38:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 09:36:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 12:12:50 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 20:03:42 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 22 Apr 2026 20:11:20 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 20:11:20 GMT
ENV RUBY_VERSION=3.4.9
# Wed, 22 Apr 2026 20:11:20 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Wed, 22 Apr 2026 20:11:20 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Wed, 22 Apr 2026 20:11:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 22 Apr 2026 20:11:20 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 22 Apr 2026 20:11:20 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 22 Apr 2026 20:11:20 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 20:11:20 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 22 Apr 2026 20:11:20 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:0b84f035435acf0ec33df4748d96fad1243fd6b0ea9917f29eaa507d4c458365`  
		Last Modified: Wed, 22 Apr 2026 00:15:04 GMT  
		Size: 52.3 MB (52336735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8c150273f4a5b502fcc97d9a922e79c7bc7d5035fb9eb1142f5adfbcea709a1`  
		Last Modified: Wed, 22 Apr 2026 03:39:23 GMT  
		Size: 25.7 MB (25679369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db5543a629afcc86e06f307e20d98c8cdd9f2490908cdef00122fb2daf671594`  
		Last Modified: Wed, 22 Apr 2026 09:37:35 GMT  
		Size: 69.8 MB (69846406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77407553cbcc2d4c713e5cabfdcef2048c44ae73e83fb9a96fe610844a4ae05f`  
		Last Modified: Wed, 22 Apr 2026 12:14:13 GMT  
		Size: 214.6 MB (214607471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8deba879300596afbfd6e0c29c6839c352c8faf5b10205ec1239e29d41116079`  
		Last Modified: Wed, 22 Apr 2026 20:07:45 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c2e6dc149c0818827c8c6014f03ef1a94764bca624312af97a398b74073bef3`  
		Last Modified: Wed, 22 Apr 2026 20:12:06 GMT  
		Size: 39.0 MB (38958852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8810e79557f1c28219411c9d7cb1e6827b3ec513f1ce43a7b16819b09dd0ffc`  
		Last Modified: Wed, 22 Apr 2026 20:12:05 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:39e49900c81a2af9406d55649ea19663d79a82c64c2f8e7fe9fe8019bf3c7790
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (15983188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7584852f833267cb98c196a7fe76b791bb5b26b5e06cc0df9216a4668a8d7817`

```dockerfile
```

-	Layers:
	-	`sha256:c04e6de05bf51ee264f439716947eeea73d821a27540644a3a38e6779e62394b`  
		Last Modified: Wed, 22 Apr 2026 20:12:05 GMT  
		Size: 16.0 MB (15961643 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6887079c4819ccfa31f5d2c7845ec598ff6f73d5526dea47ff003b458cf4b419`  
		Last Modified: Wed, 22 Apr 2026 20:12:05 GMT  
		Size: 21.5 KB (21545 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-bookworm` - linux; s390x

```console
$ docker pull ruby@sha256:9c81c8f6f99a3984a4b940c73e1e6b28e856a7c7460d4fc5c7388bde16da40be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **356.4 MB (356395601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d1369a748dc50b9050a12c55ec91d770cd7b1cd7b04a2389088bb72de6e22a0`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 02:31:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 04:20:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 05:13:20 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 09:42:19 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 22 Apr 2026 09:46:39 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 09:46:39 GMT
ENV RUBY_VERSION=3.4.9
# Wed, 22 Apr 2026 09:46:39 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Wed, 22 Apr 2026 09:46:39 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Wed, 22 Apr 2026 09:46:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 22 Apr 2026 09:46:39 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 22 Apr 2026 09:46:39 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 22 Apr 2026 09:46:39 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 09:46:39 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 22 Apr 2026 09:46:39 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:65a8acd2327b0f3316fe8707ebd5c99b15e79306d4eca71f3e635588795ae2bb`  
		Last Modified: Wed, 22 Apr 2026 00:15:31 GMT  
		Size: 47.1 MB (47147970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac385f32c2d6e9209dd9f8ada378863aba00921ac3815f399e84f802ea5ce36e`  
		Last Modified: Wed, 22 Apr 2026 02:32:03 GMT  
		Size: 24.0 MB (24036363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8df5494ce4223646f47cc2e95923748571f15dc98fdcd0c46696a358fa2128f`  
		Last Modified: Wed, 22 Apr 2026 04:20:41 GMT  
		Size: 63.5 MB (63500148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f897cf0b1d07756a3ff6dc04beacb6e6510a8778c56dc69d1a9dd01701400550`  
		Last Modified: Wed, 22 Apr 2026 05:14:17 GMT  
		Size: 183.6 MB (183571818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f34048e23322a094f78fb6d5a8173773f2433082676d7f6f0f43d3c8780257a5`  
		Last Modified: Wed, 22 Apr 2026 09:46:23 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5411f9f25b5d95b3e060b06589b9869df3d951b2c460a19ad2eed7603305f1a0`  
		Last Modified: Wed, 22 Apr 2026 09:47:14 GMT  
		Size: 38.1 MB (38138969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4529f404534b23036cc3ccf8961fb9fca1d670de4a8608c4c2cb343187f0b05`  
		Last Modified: Wed, 22 Apr 2026 09:47:13 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:98eed072ba34f8d219cc4f930a8cc97d546cbcac7437416541c069da1cd0638c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.8 MB (15814231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bafa041cdae452bbd075527589a0c9bdf4c2a1a25e5fef37e9790371906a5f1e`

```dockerfile
```

-	Layers:
	-	`sha256:11f833849368aa22443433ff017e2e72e982f41c8c50cfb7d7b990398bcc6175`  
		Last Modified: Wed, 22 Apr 2026 09:47:13 GMT  
		Size: 15.8 MB (15792728 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb58d5ed2b2307e564c97f890dc2bc6e54bfcd2369a2fe86e79ac63bceaa5d3f`  
		Last Modified: Wed, 22 Apr 2026 09:47:13 GMT  
		Size: 21.5 KB (21503 bytes)  
		MIME: application/vnd.in-toto+json
