## `ruby:3-slim-bullseye`

```console
$ docker pull ruby@sha256:36e152e745e4661b2535de6d7ee35796cdf57ebf4c877256a88faee2c7f0ad7f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `ruby:3-slim-bullseye` - linux; amd64

```console
$ docker pull ruby@sha256:51aa30812cb749a05c5a061b25f9d9448c82d504047fd3fda6b785093bfa2adc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.7 MB (72667586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f87e5e336a5ed38f334a1d33d37f4108a12031e57be4333a6f44840217d713b`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 14 May 2025 23:03:19 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1749513600'
# Wed, 14 May 2025 23:03:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 May 2025 23:03:19 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 14 May 2025 23:03:19 GMT
ENV LANG=C.UTF-8
# Wed, 14 May 2025 23:03:19 GMT
ENV RUBY_VERSION=3.4.4
# Wed, 14 May 2025 23:03:19 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.4.tar.xz
# Wed, 14 May 2025 23:03:19 GMT
ENV RUBY_DOWNLOAD_SHA256=f76d63efe9499dedd8526b74365c0c811af00dc9feb0bed7f5356488476e28f4
# Wed, 14 May 2025 23:03:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 14 May 2025 23:03:19 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 14 May 2025 23:03:19 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 14 May 2025 23:03:19 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 May 2025 23:03:19 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 14 May 2025 23:03:19 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:3d79ccbe0210f4986821cddffc5c7fc6551d938e282044db7571e448bde1e24a`  
		Last Modified: Tue, 10 Jun 2025 23:27:03 GMT  
		Size: 30.3 MB (30256064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c1c5c808e0a06cf4db3b3da5b9acc4af880405ae75e92f83c0ba0c5bb76459d`  
		Last Modified: Tue, 10 Jun 2025 23:43:54 GMT  
		Size: 1.1 MB (1068023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:709773962f8dc113edcfed5028da8b00dec800bec68247c3e7523cbb02cdf7ca`  
		Last Modified: Tue, 10 Jun 2025 23:43:54 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2569a2817a2ce46b50e7499a0c4eeea02da646a7c20755ccd51212e93da18cc6`  
		Last Modified: Tue, 10 Jun 2025 23:43:56 GMT  
		Size: 41.3 MB (41343166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8786137f13f9f88b7ab0e615405f3e8ff10691f8cfb6148f1a4bf6303ed9c8a1`  
		Last Modified: Tue, 10 Jun 2025 23:43:54 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-slim-bullseye` - unknown; unknown

```console
$ docker pull ruby@sha256:759232724e0d65795e2060931c8c5b84759a2c8cc5d7d06497fb4f840ec3d7ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2913550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e566a48b12604be821e179c70b9ec46b8ef758fbd6c92d7a09187adc1ed123f0`

```dockerfile
```

-	Layers:
	-	`sha256:f4fc891a2395482b5523989dec9e7064ef83e680197f23ebbe88f40485af37bf`  
		Last Modified: Wed, 11 Jun 2025 02:57:34 GMT  
		Size: 2.9 MB (2890755 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b8298882393d4fd125f913d2818a5fe4d74c0dab8fe3c237e16db5fa5e178ba`  
		Last Modified: Wed, 11 Jun 2025 02:57:35 GMT  
		Size: 22.8 KB (22795 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-slim-bullseye` - linux; arm variant v7

```console
$ docker pull ruby@sha256:93760839f69c83abebc11a33f3e2b50c0fe3f42ade682bf484a2969ca2ace4d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.2 MB (63191123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:879ecee1270c4435092aa8781c31686abd0d8b0a2e65888f5f296187a99915c0`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 14 May 2025 23:03:19 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1747699200'
# Wed, 14 May 2025 23:03:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 May 2025 23:03:19 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 14 May 2025 23:03:19 GMT
ENV LANG=C.UTF-8
# Wed, 14 May 2025 23:03:19 GMT
ENV RUBY_VERSION=3.4.4
# Wed, 14 May 2025 23:03:19 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.4.tar.xz
# Wed, 14 May 2025 23:03:19 GMT
ENV RUBY_DOWNLOAD_SHA256=f76d63efe9499dedd8526b74365c0c811af00dc9feb0bed7f5356488476e28f4
# Wed, 14 May 2025 23:03:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 14 May 2025 23:03:19 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 14 May 2025 23:03:19 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 14 May 2025 23:03:19 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 May 2025 23:03:19 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 14 May 2025 23:03:19 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:2091b63a268a34467e23520ae27c312421298f420abd278e760061e42a678899`  
		Last Modified: Tue, 03 Jun 2025 13:50:37 GMT  
		Size: 25.5 MB (25543902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:997ad955c63ff728048717610fc1c414e0b2c22e37b829d424a560bf53323d1f`  
		Last Modified: Thu, 05 Jun 2025 09:36:48 GMT  
		Size: 1.0 MB (1032969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0cd707b98d8a61932d1bf9d3e2b551fb77aeea19bf872fe67fc785191da1c1b`  
		Last Modified: Sat, 07 Jun 2025 08:34:31 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:102413557cbca70e6fb1d8445c164e508ca5856c3e69f9eb180120929ef2ebbb`  
		Last Modified: Mon, 09 Jun 2025 16:14:52 GMT  
		Size: 36.6 MB (36613921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28aa26e05077b7911756c282713b9e0b22e4b4818959a9b4a076346b7714354c`  
		Last Modified: Mon, 09 Jun 2025 16:14:51 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-slim-bullseye` - unknown; unknown

```console
$ docker pull ruby@sha256:009221333baa2972fe1009aa6f304a67a262596627000a6ac0243f480bfe0d02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2824643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05733d67fd8b53dcd84e94aa616e05fb0c6ecd6d56d4788552e7b683134b0894`

```dockerfile
```

-	Layers:
	-	`sha256:2d987ee8d486a339f5bbbd8483b2a16e8e9c0084935730f84c96c6a088ff4ffc`  
		Last Modified: Mon, 09 Jun 2025 16:14:50 GMT  
		Size: 2.8 MB (2801733 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3fefab7cbfc2e40b1c0d273f13489a96a377f22d842cc2df0676589c8c81b22d`  
		Last Modified: Mon, 09 Jun 2025 16:14:50 GMT  
		Size: 22.9 KB (22910 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull ruby@sha256:e7d16806678fc4b273c40ef80100b8b82f1cc50c1d160998bab054f8383f2269
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (70999205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35da88b6942b6a7ea03c0d5e5db1291327a8a72c6d55f1e37950c792296eae1f`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 14 May 2025 23:03:19 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1749513600'
# Wed, 14 May 2025 23:03:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 May 2025 23:03:19 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 14 May 2025 23:03:19 GMT
ENV LANG=C.UTF-8
# Wed, 14 May 2025 23:03:19 GMT
ENV RUBY_VERSION=3.4.4
# Wed, 14 May 2025 23:03:19 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.4.tar.xz
# Wed, 14 May 2025 23:03:19 GMT
ENV RUBY_DOWNLOAD_SHA256=f76d63efe9499dedd8526b74365c0c811af00dc9feb0bed7f5356488476e28f4
# Wed, 14 May 2025 23:03:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 14 May 2025 23:03:19 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 14 May 2025 23:03:19 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 14 May 2025 23:03:19 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 May 2025 23:03:19 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 14 May 2025 23:03:19 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:1efb2a16e6255fa81193190b623ba0668ffa777ab1de41ac5c5d2d2060a47784`  
		Last Modified: Wed, 11 Jun 2025 00:07:31 GMT  
		Size: 28.7 MB (28744185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f170247f0fc28e54d216a322c77e15b08d1349e546dce7928259b11513ff4bf1`  
		Last Modified: Wed, 11 Jun 2025 07:23:30 GMT  
		Size: 1.1 MB (1055210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f802e3c2f56939b242c9c6c3d3679377e76c2fbf4f00f12b511ec41025f4d397`  
		Last Modified: Wed, 11 Jun 2025 07:23:30 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d00b90a43d5498d91c4b3afd6ad812473b14c32588c0a31e5436d312b8ee1153`  
		Last Modified: Wed, 11 Jun 2025 09:24:17 GMT  
		Size: 41.2 MB (41199478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ade90f46349ad39ad1452cf5aed21e9be58f0ac30a4685a23bcd3c85668b9fc`  
		Last Modified: Wed, 11 Jun 2025 09:24:14 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-slim-bullseye` - unknown; unknown

```console
$ docker pull ruby@sha256:e471beb0c43b41d8db19fc67f8636e2ed4ab072a3e0c203293cccb7a97ae423d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2913950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:225d4607ae890caee0947f56ad3863c6c266518952cd510199727aacaf94402c`

```dockerfile
```

-	Layers:
	-	`sha256:990bd640f5fdae1ce73f49b4de7a886277f6ce3b8648ba1226cb6a228a6d035a`  
		Last Modified: Wed, 11 Jun 2025 08:57:48 GMT  
		Size: 2.9 MB (2891007 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1d62d5f4ced7222530c721f65394ff8dda6541aa9c7278eda09118beb0af3e4`  
		Last Modified: Wed, 11 Jun 2025 08:57:49 GMT  
		Size: 22.9 KB (22943 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-slim-bullseye` - linux; 386

```console
$ docker pull ruby@sha256:b1a1a8a87ad6f36dce07df1a4b86c3c6f183b3d56275f8683662bdc8165c0796
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.0 MB (68983785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c0e952a957b5af43ef486fd31f8362587a535a5338599694d895c0c268f1e2a`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 14 May 2025 23:03:19 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1749513600'
# Wed, 14 May 2025 23:03:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 May 2025 23:03:19 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 14 May 2025 23:03:19 GMT
ENV LANG=C.UTF-8
# Wed, 14 May 2025 23:03:19 GMT
ENV RUBY_VERSION=3.4.4
# Wed, 14 May 2025 23:03:19 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.4.tar.xz
# Wed, 14 May 2025 23:03:19 GMT
ENV RUBY_DOWNLOAD_SHA256=f76d63efe9499dedd8526b74365c0c811af00dc9feb0bed7f5356488476e28f4
# Wed, 14 May 2025 23:03:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 14 May 2025 23:03:19 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 14 May 2025 23:03:19 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 14 May 2025 23:03:19 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 May 2025 23:03:19 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 14 May 2025 23:03:19 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:1294ecac50b0f4fe7018ad5e666e6e3c43bd85fbdc4ff68322834fcc70904e3c`  
		Last Modified: Tue, 10 Jun 2025 23:26:42 GMT  
		Size: 31.2 MB (31189682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:227f90b160d4022742f30dfe93ea834582f695816695428f99073ac9d3bad7f9`  
		Last Modified: Tue, 10 Jun 2025 23:46:06 GMT  
		Size: 1.1 MB (1080102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a3208647f8923dc3b7fe5d43d84271ad04c5ad788a2954a2a0634067d547909`  
		Last Modified: Tue, 10 Jun 2025 23:46:07 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dee89257769199a3320ecc4a4316ccdcb7a1899df0d35a6e21a297217c9c6834`  
		Last Modified: Tue, 10 Jun 2025 23:46:09 GMT  
		Size: 36.7 MB (36713667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cefa8ca0fe323d4948e7f70704f38e64ab80310871e56c3ca58a57ab020f10b8`  
		Last Modified: Tue, 10 Jun 2025 23:46:07 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-slim-bullseye` - unknown; unknown

```console
$ docker pull ruby@sha256:c1b51403ba579e0c6e3b682f42fbf26038ee2ded02d3f862abd2f7f75a292150
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2910689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d5cb3f768a4dd3ea7c3fc2a24cdedf016a77a7a90aa2b42c8df69152133b810`

```dockerfile
```

-	Layers:
	-	`sha256:eb585a502e5e61a90114e2f5322acc665e9ce9d440f8c2e0765868c80d9a593a`  
		Last Modified: Tue, 10 Jun 2025 23:59:21 GMT  
		Size: 2.9 MB (2887932 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33d9c7cdd7fb41d77bd62d2abcd4c8a1f2040882fcdc9afcbf14dd40a537998d`  
		Last Modified: Tue, 10 Jun 2025 23:59:22 GMT  
		Size: 22.8 KB (22757 bytes)  
		MIME: application/vnd.in-toto+json
