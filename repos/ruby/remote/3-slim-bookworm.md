## `ruby:3-slim-bookworm`

```console
$ docker pull ruby@sha256:8dba3b1bf6b1bdd3aefb0deef9d866fa16f8eb346566d9d592e78af7e6d34d4e
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

### `ruby:3-slim-bookworm` - linux; amd64

```console
$ docker pull ruby@sha256:3f4dae8d18578b860b4e9f13c7482cbd81ec1f9c40b7a15b779627610b935cc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73229868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9ccb9998fa2f77afd16c1dbddde2f5af16de8081dc38ffd03dee8323f226684`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:41:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:41:43 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Mon, 08 Dec 2025 23:44:07 GMT
ENV LANG=C.UTF-8
# Mon, 08 Dec 2025 23:44:07 GMT
ENV RUBY_VERSION=3.4.7
# Mon, 08 Dec 2025 23:44:07 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Mon, 08 Dec 2025 23:44:07 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Mon, 08 Dec 2025 23:44:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Mon, 08 Dec 2025 23:44:07 GMT
ENV GEM_HOME=/usr/local/bundle
# Mon, 08 Dec 2025 23:44:07 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Mon, 08 Dec 2025 23:44:07 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 23:44:07 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Mon, 08 Dec 2025 23:44:07 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:ae4ce04d0e1ccb5db08fa441b79635de5590399fae652d10bd3379b231be0ead`  
		Last Modified: Mon, 08 Dec 2025 22:17:22 GMT  
		Size: 28.2 MB (28228418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b79b0f87f0bd4905042cdc0283d0c7004e7273ef4bf11b988ab5e198692cd4c7`  
		Last Modified: Mon, 08 Dec 2025 23:44:22 GMT  
		Size: 3.5 MB (3509676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf43ced354398e8ce6e96f44e78583b7a76a402dc558b031e014239bda8fed60`  
		Last Modified: Mon, 08 Dec 2025 23:44:22 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46f8d9deffff428b70be5ca7e0e3844e047ea4b7dc4d33f828e625c9abbbb995`  
		Last Modified: Mon, 08 Dec 2025 23:44:27 GMT  
		Size: 41.5 MB (41491442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ffd9d5c5180d7d4861797f277465160d797936e4d1ee204e0b43b9b2a0abfdd`  
		Last Modified: Mon, 08 Dec 2025 23:44:22 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-slim-bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:5abc62a02ae4b7770baa2d06d2c5035e140ca0221cf2fd7fd07cfd81aea4e33e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2624728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:254e0592c32bd865fb398818d7157ece53102004f63112f8af8aaeb670f93966`

```dockerfile
```

-	Layers:
	-	`sha256:c1f7cf7bf99bda269ef86d4c05853c5049343988dab4152160902efedbde1c63`  
		Last Modified: Tue, 09 Dec 2025 03:58:37 GMT  
		Size: 2.6 MB (2601641 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38065a5eaad718d49cc0ae3380d4d9c940672f1f88614203fea9707bb11620b7`  
		Last Modified: Tue, 09 Dec 2025 03:58:38 GMT  
		Size: 23.1 KB (23087 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-slim-bookworm` - linux; arm variant v5

```console
$ docker pull ruby@sha256:eeab1c70bc2c36664617f18fd5d3eb38f7072977de03043655ce40767e2a853a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.1 MB (66115124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62662005d0f03a97bf6acfa0590d8f5b47fdebe7f91ec26bd290939fddbebabd`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 00:37:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:37:45 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 09 Dec 2025 00:40:21 GMT
ENV LANG=C.UTF-8
# Tue, 09 Dec 2025 00:40:21 GMT
ENV RUBY_VERSION=3.4.7
# Tue, 09 Dec 2025 00:40:21 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Tue, 09 Dec 2025 00:40:21 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Tue, 09 Dec 2025 00:40:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 09 Dec 2025 00:40:21 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 09 Dec 2025 00:40:21 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 09 Dec 2025 00:40:21 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 00:40:22 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 09 Dec 2025 00:40:22 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:20ca79728ab9e4eb574872cf271bd965c51cf4e8ac84660ef17b281a3aeb750e`  
		Last Modified: Mon, 08 Dec 2025 22:16:26 GMT  
		Size: 25.8 MB (25757588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8856da5e72ee7b631ce46c1669ab2c12f98210818c285be84c5c0dc4700fd9c5`  
		Last Modified: Tue, 09 Dec 2025 00:40:43 GMT  
		Size: 3.1 MB (3079829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:760456c9a275fd3acddbdfb3d2008f1d0367a6ac4daa682a720131304ce3543d`  
		Last Modified: Tue, 09 Dec 2025 00:40:40 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4914eb1f60b23bf5ba922dce25680e43c14f4a6afb6d00c29c1b1d86e7e4d7db`  
		Last Modified: Tue, 09 Dec 2025 00:40:44 GMT  
		Size: 37.3 MB (37277374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76e176909b20496c4e3660fdabcd1106d295cd8f06f424a91c7afcc2fce4adb4`  
		Last Modified: Tue, 09 Dec 2025 00:40:40 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-slim-bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:93233f2e679fc0d6717893084003db54738322d2423e5adc5e041a4cc48858fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2628652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e4d04e62e292af2fb356b6d1c751de2243f5de218c41170d8b1291ac84bf0a1`

```dockerfile
```

-	Layers:
	-	`sha256:78e596ed838d274d052918357878ecef44af7adc6e7c802e941f3ed7c930206b`  
		Last Modified: Tue, 09 Dec 2025 03:58:42 GMT  
		Size: 2.6 MB (2605446 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef0af0c0499e1baeb196f710f14cc3d00a7dc1cd95fe72f0afecf753ffe8fc82`  
		Last Modified: Tue, 09 Dec 2025 03:58:43 GMT  
		Size: 23.2 KB (23206 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-slim-bookworm` - linux; arm variant v7

```console
$ docker pull ruby@sha256:54896ebff3ce5efd3f40b853cef57811f02a11833d72505c614f4ad638619691
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.0 MB (63961634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21bc88bee4db9ef75a3daa12f9a7dc3c051e52d849010925b31b34d7d37534f0`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 01:11:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 01:11:43 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 09 Dec 2025 01:14:17 GMT
ENV LANG=C.UTF-8
# Tue, 09 Dec 2025 01:14:17 GMT
ENV RUBY_VERSION=3.4.7
# Tue, 09 Dec 2025 01:14:17 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Tue, 09 Dec 2025 01:14:17 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Tue, 09 Dec 2025 01:14:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 09 Dec 2025 01:14:17 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 09 Dec 2025 01:14:17 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 09 Dec 2025 01:14:17 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 01:14:17 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 09 Dec 2025 01:14:17 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:e12d446114182318769a6ca4adfc14d21fbb73f898de1d765662812d9f21c3a6`  
		Last Modified: Mon, 08 Dec 2025 22:16:03 GMT  
		Size: 23.9 MB (23934020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02de29e9d2084c8f4bcf3d05f55ba04d8a1cc047065ea85490e3d21227ef28ca`  
		Last Modified: Tue, 09 Dec 2025 01:14:34 GMT  
		Size: 2.9 MB (2912772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19dcbc5dd06606dad91c77e136912f8481677bdebb2a03b76d40deed4ccd814b`  
		Last Modified: Tue, 09 Dec 2025 01:14:34 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5f9dd9625eb5792d47fc0528f6b352d70aed6799f9bf6deaf29ed07104c6c44`  
		Last Modified: Tue, 09 Dec 2025 01:14:44 GMT  
		Size: 37.1 MB (37114509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:747141717064494039a544d44d90bbc0f35ccea4612ed18b130b067898eeee56`  
		Last Modified: Tue, 09 Dec 2025 01:14:34 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-slim-bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:ea709e4033f971a0501ef1e78b9beea294e6153d8c45e03917a5d9a4ba7b1ab9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2627071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30b4134081cc58c575ad08208205e3d96b368ed0160ad258987e1f1a0638239d`

```dockerfile
```

-	Layers:
	-	`sha256:3ee00f74f4e340f9d450870e3e80d0fbbb0f3e6c404fb5bd1460dbd3fd066ba4`  
		Last Modified: Tue, 09 Dec 2025 03:58:47 GMT  
		Size: 2.6 MB (2603865 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b7d33681ae5ada49bfa3ca80fe603c715e29bd2f4e8b849cdb859d4c8eb1e41`  
		Last Modified: Tue, 09 Dec 2025 03:58:47 GMT  
		Size: 23.2 KB (23206 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull ruby@sha256:febee76262733ba71990247b3283d6b10ef4e54bf83e81f3e8e5016121f38cf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.8 MB (72847430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13e3289b9564bb908ec8bb87a734eb3797669854df6e17db763873e3e7f45340`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:50:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:50:50 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Mon, 08 Dec 2025 23:53:17 GMT
ENV LANG=C.UTF-8
# Mon, 08 Dec 2025 23:53:17 GMT
ENV RUBY_VERSION=3.4.7
# Mon, 08 Dec 2025 23:53:17 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Mon, 08 Dec 2025 23:53:17 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Mon, 08 Dec 2025 23:53:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Mon, 08 Dec 2025 23:53:17 GMT
ENV GEM_HOME=/usr/local/bundle
# Mon, 08 Dec 2025 23:53:17 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Mon, 08 Dec 2025 23:53:17 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 23:53:17 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Mon, 08 Dec 2025 23:53:17 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:8a4a7306158c2bef7a131de3110e384f4822829cbcce20bc6b4ba32dd82a1d87`  
		Last Modified: Mon, 08 Dec 2025 22:16:51 GMT  
		Size: 28.1 MB (28102229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a868ac7eb442cdf579d97319517248c57a0caac107a864ce28863496927fbe9`  
		Last Modified: Mon, 08 Dec 2025 23:53:31 GMT  
		Size: 3.3 MB (3340656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e05f11deca2d8c653ba59d7301d413641fad948726efe4625b6cc85d44b39b05`  
		Last Modified: Mon, 08 Dec 2025 23:53:31 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d0ba17ca510a21855e0f3ee1bebbbc30e84167e4ff4bfb46b9ac6c3f2b27ea7`  
		Last Modified: Mon, 08 Dec 2025 23:53:35 GMT  
		Size: 41.4 MB (41404212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93c364ab1781b984eec80e8accaf287dea38fd17f24e4affd2f288e3d8a102c1`  
		Last Modified: Mon, 08 Dec 2025 23:53:31 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-slim-bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:6b98edf8234682643dc669773b8386dd57f8847ea88e7f8e873bb653342b48ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2625135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4580e18a32a80c861a91bf704677bd541a4005b48fc128e16f1ac83b0e7ae2b1`

```dockerfile
```

-	Layers:
	-	`sha256:b94f92a5f6cc5cc9f27f502798f65cbf53cce689b3e25834ab537b6c19e2a526`  
		Last Modified: Tue, 09 Dec 2025 03:58:51 GMT  
		Size: 2.6 MB (2601899 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5fe6c28e6b4f23110848650ae5ce8cca25ae2acba83d3428f816cb70127b42ae`  
		Last Modified: Tue, 09 Dec 2025 03:58:52 GMT  
		Size: 23.2 KB (23236 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-slim-bookworm` - linux; 386

```console
$ docker pull ruby@sha256:4f99159925fe830a9e54dcef301f90775429c04c47a8d62836a5f498bd87793c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.8 MB (69796290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd8528918f0cc21bc954af7e366755f11a54f9ead5508b34dc04734d5dc00c86`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:38:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:38:55 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Mon, 08 Dec 2025 23:41:05 GMT
ENV LANG=C.UTF-8
# Mon, 08 Dec 2025 23:41:05 GMT
ENV RUBY_VERSION=3.4.7
# Mon, 08 Dec 2025 23:41:05 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Mon, 08 Dec 2025 23:41:05 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Mon, 08 Dec 2025 23:41:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Mon, 08 Dec 2025 23:41:05 GMT
ENV GEM_HOME=/usr/local/bundle
# Mon, 08 Dec 2025 23:41:05 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Mon, 08 Dec 2025 23:41:05 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 23:41:05 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Mon, 08 Dec 2025 23:41:05 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:e28a7f622a043206041afc8ed0d2b3d1b9bbffe3b724b994051e9d6dbc2f8a1e`  
		Last Modified: Mon, 08 Dec 2025 22:16:30 GMT  
		Size: 29.2 MB (29209729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:547a4662e7f50e213e8e24f13f09604abbd66c9e9b4cf88c5cef217cebd5d8a6`  
		Last Modified: Mon, 08 Dec 2025 23:41:19 GMT  
		Size: 3.5 MB (3510957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95e3bcd14d40d9d64a5c6249cb3fee0824a6eb1a43223560eb8fdb2e5f4d5770`  
		Last Modified: Mon, 08 Dec 2025 23:41:19 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e81942e893447cc90f67595ff3f52fb390797cb2b3ff9bd7267793ac60fd26bb`  
		Last Modified: Mon, 08 Dec 2025 23:41:22 GMT  
		Size: 37.1 MB (37075272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55cd6775a0b00c8a11331e2065f62bf32ac9afc9f71de3ba4479417042bf80b1`  
		Last Modified: Mon, 08 Dec 2025 23:41:19 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-slim-bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:5705ef877a409035c7f3c2187ea7052d2f4f0ab88c852cae7b89d99a14382fe0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2621871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f008078b086fdc55a0b3873c5484549565a54d28b85a838b534767e9dad3943d`

```dockerfile
```

-	Layers:
	-	`sha256:01e18f76e6dd311a1b37ff4f13c8a7c014410776aeb4cc5d1f2b183ffcc7dc2e`  
		Last Modified: Tue, 09 Dec 2025 00:58:25 GMT  
		Size: 2.6 MB (2598822 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6ce64325c7f38d3e916922e9f30b65602c357ebff01951017358c307466f7f5`  
		Last Modified: Tue, 09 Dec 2025 00:58:26 GMT  
		Size: 23.0 KB (23049 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-slim-bookworm` - linux; mips64le

```console
$ docker pull ruby@sha256:faad31d9156c62ea1318d98291680a314f46b4cf96eba71e4ebf6fbd243ec952
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69890085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28a3d006d8bf3d61106274af34dd144949bef8da8c5b5e19e0e8f6fbe579758f`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1763337600'
# Wed, 19 Nov 2025 02:49:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 19 Nov 2025 02:49:33 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 19 Nov 2025 03:21:02 GMT
ENV LANG=C.UTF-8
# Wed, 19 Nov 2025 03:21:02 GMT
ENV RUBY_VERSION=3.4.7
# Wed, 19 Nov 2025 03:21:02 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Wed, 19 Nov 2025 03:21:02 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Wed, 19 Nov 2025 03:21:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 19 Nov 2025 03:21:02 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 19 Nov 2025 03:21:02 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 19 Nov 2025 03:21:02 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 19 Nov 2025 03:21:04 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 19 Nov 2025 03:21:04 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:099882631f3c0c5583696bbb377a83dca2faf014da28b08add3482e4678d2872`  
		Last Modified: Tue, 18 Nov 2025 01:11:53 GMT  
		Size: 28.5 MB (28513764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8e35b9956b1cbe95065991e8ae4c2d28a30c072c7fb47ace96566c8b096e40d`  
		Last Modified: Wed, 19 Nov 2025 03:05:39 GMT  
		Size: 2.9 MB (2900501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd6681ec6179d65a66270a0e6f10cf068efdc2368e59d7f757212573bbaff6e`  
		Last Modified: Wed, 19 Nov 2025 03:05:38 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b879ddc7b9b6817671a7eb4f93cebbdf95e7f05163747fe30ef6b1f9ee584245`  
		Last Modified: Wed, 19 Nov 2025 03:22:02 GMT  
		Size: 38.5 MB (38475486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4346e6198b6fa3e875727802a5db6a2da408dd3f71095e7aac3586213f29816`  
		Last Modified: Wed, 19 Nov 2025 03:21:54 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-slim-bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:1a04083d52f54748d5b30f5a44a5db9c324a44be9d97d6584a84d5f0097e863d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.9 KB (22947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ad5c2978dc46be9db07fa6e3807847d5ac3c610e540767f266094c1e4de949d`

```dockerfile
```

-	Layers:
	-	`sha256:481814826e258a4cc5e112c830d5f08deee822ddffb921d832c4ca0fd8498cc4`  
		Last Modified: Wed, 19 Nov 2025 06:57:43 GMT  
		Size: 22.9 KB (22947 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-slim-bookworm` - linux; ppc64le

```console
$ docker pull ruby@sha256:3d89764b0b9e1578a4d8e2ed379a8e1e73caa80ec4862ef1b93f0ef63863da63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74723931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c0e17f1a72208e6bf4f859fafae35b760cbfb5e6b47c1070fbbf6ea29146e21`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 05:56:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:56:14 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 18 Nov 2025 06:05:46 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 06:05:46 GMT
ENV RUBY_VERSION=3.4.7
# Tue, 18 Nov 2025 06:05:46 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Tue, 18 Nov 2025 06:05:46 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Tue, 18 Nov 2025 06:05:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 18 Nov 2025 06:05:46 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 18 Nov 2025 06:05:46 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 18 Nov 2025 06:05:46 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 06:05:47 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 18 Nov 2025 06:05:47 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:ec7a1a15d2a3b24a68856f8ea1e0b4ced75acf51647ebb533587594c649f3a5b`  
		Last Modified: Tue, 18 Nov 2025 01:56:01 GMT  
		Size: 32.1 MB (32068826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b7c3256cf347ab6b6a418c4e50ff4e79b212be8ebcba139b73b0d7a77d8a838`  
		Last Modified: Tue, 18 Nov 2025 06:01:10 GMT  
		Size: 3.7 MB (3709070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f335ae6f41ee5bac5c8c7103ef44dad3d973bccfddc68ea5180a3c3df5134479`  
		Last Modified: Tue, 18 Nov 2025 06:01:10 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33c603aa9e00274f7aa532afff1189400c729424ce4b7a4cd22dd4126a55b1b7`  
		Last Modified: Tue, 18 Nov 2025 06:06:34 GMT  
		Size: 38.9 MB (38945702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46846a66b1ed5074f4ba464a55bff1bb7f9c5a1d90b738f461f4a79fb25b72f6`  
		Last Modified: Tue, 18 Nov 2025 06:06:31 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-slim-bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:0e86733b75ff72ab4f87f42912f4e28e8ffb97ac44c84032f9a049cf1019dc55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2629169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f403731a1f3e6c2855769db6693ccf6b3fe1ef38f1fd3d0b0f65bc70bda0209`

```dockerfile
```

-	Layers:
	-	`sha256:02ea77c902ecf266cc4b74a33d53efb847bf478dad833c049ae335aeb4424c43`  
		Last Modified: Tue, 18 Nov 2025 06:59:17 GMT  
		Size: 2.6 MB (2606032 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68adcda7cd678ed4e58efd78d098a06df9c0c0b91fbedb578bea2cd393018507`  
		Last Modified: Tue, 18 Nov 2025 06:59:18 GMT  
		Size: 23.1 KB (23137 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-slim-bookworm` - linux; s390x

```console
$ docker pull ruby@sha256:a8617c3ab5e1e1ee80f18196687738ea0e0f0aa923255265e7480d33090e8110
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.2 MB (68187538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de2ba1b4fc0ec441fdaa934e27476957fe0a4580319ed2af9e7bacc3223552a5`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 01:20:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 01:20:17 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 09 Dec 2025 01:23:05 GMT
ENV LANG=C.UTF-8
# Tue, 09 Dec 2025 01:23:05 GMT
ENV RUBY_VERSION=3.4.7
# Tue, 09 Dec 2025 01:23:05 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Tue, 09 Dec 2025 01:23:05 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Tue, 09 Dec 2025 01:23:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 09 Dec 2025 01:23:05 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 09 Dec 2025 01:23:05 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 09 Dec 2025 01:23:05 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 01:23:05 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 09 Dec 2025 01:23:05 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:00a29f44cb5b31bbcf043ec5426ee1c018bb26435350712cb5e48d56c6d95792`  
		Last Modified: Mon, 08 Dec 2025 22:15:04 GMT  
		Size: 26.9 MB (26884429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c68f0ebe313b468387e42a6bbf8b5b855c42d1a9aecca5d1e79d1513386fde7`  
		Last Modified: Tue, 09 Dec 2025 01:23:28 GMT  
		Size: 3.2 MB (3170271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaa348aa4bda397502f2be230364b9fab79e0917fc3a7af75372bb9389759fb2`  
		Last Modified: Tue, 09 Dec 2025 01:23:27 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a4982c74dfbcba203fdbd55bc2cca45b5307d972e25c4530b6214964155865c`  
		Last Modified: Tue, 09 Dec 2025 01:23:31 GMT  
		Size: 38.1 MB (38132506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cc679a298e4ebf41767a4a74083c6666d07e1adf8fe39d4ac7c176dbed7b730`  
		Last Modified: Tue, 09 Dec 2025 01:23:27 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-slim-bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:ccef6e369c57cc2382bc14aaadfa03f1bb90b2404e4908858b14f9952d7cf3fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2621559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76514fe9eef9ff8981d3bd6d97959dd800bf7c5225b0d5bbc8aa87ccee6b0380`

```dockerfile
```

-	Layers:
	-	`sha256:29c51b4079a97cdeee38bfb01a857d9cc8d150bd1df66f17b4a3a06a6f17b78c`  
		Last Modified: Tue, 09 Dec 2025 03:59:03 GMT  
		Size: 2.6 MB (2598472 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f907df1e1cbca42a67a98f73599c9b26a486cc9e4b3a789a4e82e2ae6bb13b4`  
		Last Modified: Tue, 09 Dec 2025 03:59:03 GMT  
		Size: 23.1 KB (23087 bytes)  
		MIME: application/vnd.in-toto+json
