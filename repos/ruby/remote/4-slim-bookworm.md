## `ruby:4-slim-bookworm`

```console
$ docker pull ruby@sha256:8e2d29bf7fe1442b1b0ddedf52862c4e6cc6414b0e775511920076d30b6f1350
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

### `ruby:4-slim-bookworm` - linux; amd64

```console
$ docker pull ruby@sha256:a9d95f9aa853c0d818f9f9b31f536adb24fb83d866e8fd1a4d3fcc5a2f229193
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.7 MB (80732196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1487a910d589d2a341e46a5a58bad9da52c576f9cc32844930159cab76a82d11`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Tue, 12 May 2026 00:19:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 May 2026 00:19:53 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 12 May 2026 00:22:09 GMT
ENV LANG=C.UTF-8
# Tue, 12 May 2026 00:22:09 GMT
ENV RUBY_VERSION=4.0.4
# Tue, 12 May 2026 00:22:09 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/4.0/ruby-4.0.4.tar.xz
# Tue, 12 May 2026 00:22:09 GMT
ENV RUBY_DOWNLOAD_SHA256=6ff9d2d6e75f5a6f997222ecc45f79209d663737eceb3689d1f42ab952673fb7
# Tue, 12 May 2026 00:22:09 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 		${rustArch:+--enable-zjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 12 May 2026 00:22:09 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 12 May 2026 00:22:09 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 12 May 2026 00:22:09 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 00:22:09 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 12 May 2026 00:22:09 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:9b02e9fcb40102eae20d9d1fc7594b44328f4a3eb9b8a3bdb7db283d10840a30`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 28.2 MB (28236282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a7a1fb72c8457c9dfd9a45a87711a914dfb3dfae1ad016c36c333cb86db8f77`  
		Last Modified: Tue, 12 May 2026 00:22:19 GMT  
		Size: 3.5 MB (3510920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31a87e1c16ec2e5e7349f9a59d79399f055be93913028c321edd7c3a210f4d6c`  
		Last Modified: Tue, 12 May 2026 00:22:19 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:058f83552abff18dc5e825e9ba5a791d9043f65564ca91e4b10d7b7fa9a618c3`  
		Last Modified: Tue, 12 May 2026 00:22:21 GMT  
		Size: 49.0 MB (48984658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a47d073e308aee6e096b14ca12f9d8bd95042ff300589beb783d5809d7927f2`  
		Last Modified: Tue, 12 May 2026 00:22:19 GMT  
		Size: 145.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:4-slim-bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:27df312658317f9087bd54a795de096042e884f1cc12bc15148364abe966797f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2620875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53567ad63407f803f616ac63bc68f44723843eec8e8d7ddcb692e175374e1bfb`

```dockerfile
```

-	Layers:
	-	`sha256:3e3ac81bc6cee81b2ac99b075c2b672632e237806a2ed6e407c0a574d03866cc`  
		Last Modified: Tue, 12 May 2026 00:22:19 GMT  
		Size: 2.6 MB (2597671 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:858b12a95080db9fb54192182021ad856ea9346038ddde27dabb10a5a674b952`  
		Last Modified: Tue, 12 May 2026 00:22:19 GMT  
		Size: 23.2 KB (23204 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:4-slim-bookworm` - linux; arm variant v5

```console
$ docker pull ruby@sha256:2572b327a1ffd2440c797e22e9e8b3e6767546c5b76343ade9f64b47004dc58f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.8 MB (70813142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b618ba38423c13eee3a1d716b84c11a36d85bdb232e6226565af3d01f1014b1`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1777939200'
# Tue, 12 May 2026 00:07:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 May 2026 00:07:06 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 12 May 2026 00:09:54 GMT
ENV LANG=C.UTF-8
# Tue, 12 May 2026 00:09:54 GMT
ENV RUBY_VERSION=4.0.4
# Tue, 12 May 2026 00:09:54 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/4.0/ruby-4.0.4.tar.xz
# Tue, 12 May 2026 00:09:54 GMT
ENV RUBY_DOWNLOAD_SHA256=6ff9d2d6e75f5a6f997222ecc45f79209d663737eceb3689d1f42ab952673fb7
# Tue, 12 May 2026 00:09:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 		${rustArch:+--enable-zjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 12 May 2026 00:09:54 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 12 May 2026 00:09:54 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 12 May 2026 00:09:54 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 00:09:54 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 12 May 2026 00:09:54 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:0496e5b1fd9475851f8b3578080061a05ea61be300ea5a278a4a08a883855adc`  
		Last Modified: Fri, 08 May 2026 18:33:05 GMT  
		Size: 25.8 MB (25765670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfc084a4f75cc4289751f1e761f1b3fa0b3768ec6f63bd9522f852c3302e33ff`  
		Last Modified: Tue, 12 May 2026 00:10:04 GMT  
		Size: 3.1 MB (3081753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5016fb680695cfc950594d1ecad89c077410f5eb7695c6eea05ed5cd78ffe22`  
		Last Modified: Tue, 12 May 2026 00:09:46 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ee41d23e678624cca0dea16ecfe2ee241c4ef9ccb3ae356457e685db900a064`  
		Last Modified: Tue, 12 May 2026 00:10:05 GMT  
		Size: 42.0 MB (41965385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03674389ec6a63bce8ea384c73dd8137593b7a4958e745d5ac59f33a1c18c5d2`  
		Last Modified: Tue, 12 May 2026 00:10:04 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:4-slim-bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:208c324554f6d4d033b76708cb1cae7a92af6243c525a137b2a7e9a92770861b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2624799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48c0420b364f15c1030484b6b0c5a29aac23d537457edb83034520288cc03b1a`

```dockerfile
```

-	Layers:
	-	`sha256:9f435a7f1ff5fcd1d1a07f738a46f683df0c3e352ef051046381296c3f00d1ef`  
		Last Modified: Tue, 12 May 2026 00:10:04 GMT  
		Size: 2.6 MB (2601476 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7bee4b81aa09791c78ab977e1197e374cbb104083bf6606f7ebb9df50b0825fb`  
		Last Modified: Tue, 12 May 2026 00:10:04 GMT  
		Size: 23.3 KB (23323 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:4-slim-bookworm` - linux; arm variant v7

```console
$ docker pull ruby@sha256:f8b91181a0beeb7b1b138424591ba97e2de4ba7add43048c6145feaf451122bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.6 MB (68633542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:112e8859cc6204cfc1adbe51b4ab8985d5a6fe869f1132996483a7f4bc90af9b`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1777939200'
# Tue, 12 May 2026 00:07:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 May 2026 00:07:06 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 12 May 2026 00:09:36 GMT
ENV LANG=C.UTF-8
# Tue, 12 May 2026 00:09:36 GMT
ENV RUBY_VERSION=4.0.4
# Tue, 12 May 2026 00:09:36 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/4.0/ruby-4.0.4.tar.xz
# Tue, 12 May 2026 00:09:36 GMT
ENV RUBY_DOWNLOAD_SHA256=6ff9d2d6e75f5a6f997222ecc45f79209d663737eceb3689d1f42ab952673fb7
# Tue, 12 May 2026 00:09:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 		${rustArch:+--enable-zjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 12 May 2026 00:09:36 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 12 May 2026 00:09:36 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 12 May 2026 00:09:36 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 00:09:36 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 12 May 2026 00:09:36 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:1c5a0b31b39e45b38b0c73a2e506eb60bb1de512092b4765e565207648f55da2`  
		Last Modified: Fri, 08 May 2026 18:37:03 GMT  
		Size: 23.9 MB (23941406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5582257d31f59a1ccead248c09213a9ef10877b90470b6d5b5347b77abc13114`  
		Last Modified: Tue, 12 May 2026 00:09:46 GMT  
		Size: 2.9 MB (2914562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5016fb680695cfc950594d1ecad89c077410f5eb7695c6eea05ed5cd78ffe22`  
		Last Modified: Tue, 12 May 2026 00:09:46 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a42b5559527d9f932c4ca2e7308662ba150185c1b2e7cda59c5ed65b110cc139`  
		Last Modified: Tue, 12 May 2026 00:09:47 GMT  
		Size: 41.8 MB (41777239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e8a10fafd95be6c269080968b5e86c49acecac9299927b2801f44bfc4852a3a`  
		Last Modified: Tue, 12 May 2026 00:09:46 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:4-slim-bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:db5410c23ae8b423f22dc92f81a6e1cb539e79322ec16013936420e0cbbb117f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2623218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4a959bbb6fd63e7a577001280372cde962df467c83ec61a2cb27960fcd35fa9`

```dockerfile
```

-	Layers:
	-	`sha256:e63af346ced26d9e3438c61a09a35b2e091e31d00e94c05f8bd1d59a7402a631`  
		Last Modified: Tue, 12 May 2026 00:09:46 GMT  
		Size: 2.6 MB (2599895 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e362a8f213e13bd4c82e96c84848135f3674d0317d7113c1f850a4197dfe1336`  
		Last Modified: Tue, 12 May 2026 00:09:46 GMT  
		Size: 23.3 KB (23323 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:4-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull ruby@sha256:e19108daa2a57b7a38d9e8f9d55861d888006a338638e0d5f98780a9d6a06562
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.2 MB (80179090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:689d219fc5c99769637c382ba0b746972a860eec8d70d7663f752e8878d1366d`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Tue, 12 May 2026 00:18:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 May 2026 00:18:35 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 12 May 2026 00:21:05 GMT
ENV LANG=C.UTF-8
# Tue, 12 May 2026 00:21:05 GMT
ENV RUBY_VERSION=4.0.4
# Tue, 12 May 2026 00:21:05 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/4.0/ruby-4.0.4.tar.xz
# Tue, 12 May 2026 00:21:05 GMT
ENV RUBY_DOWNLOAD_SHA256=6ff9d2d6e75f5a6f997222ecc45f79209d663737eceb3689d1f42ab952673fb7
# Tue, 12 May 2026 00:21:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 		${rustArch:+--enable-zjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 12 May 2026 00:21:05 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 12 May 2026 00:21:05 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 12 May 2026 00:21:05 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 00:21:05 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 12 May 2026 00:21:05 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:6a2d07df495cc055bce0251fe801ee08db90750f52e43a555be5dfd8f5023783`  
		Last Modified: Fri, 08 May 2026 18:24:52 GMT  
		Size: 28.1 MB (28116165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2af6244e116a2b44e0117bd32e9296b0c9ccbc49b2e862ef7410a47d5f4a750`  
		Last Modified: Tue, 12 May 2026 00:21:16 GMT  
		Size: 3.3 MB (3343192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b90f10ffd25fda87a3650deac8eff12e050288e08c54d5581bc63349fbe4fa2e`  
		Last Modified: Tue, 12 May 2026 00:21:16 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e274893b1f4e8ce4c2d7133be5d5f1d8090fcc232f6356c3a931f03f689f4b71`  
		Last Modified: Tue, 12 May 2026 00:21:18 GMT  
		Size: 48.7 MB (48719398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c145a544b4547c3747b82c5aa302ce66034c63e1816727c8de76d8fda4797fe2`  
		Last Modified: Tue, 12 May 2026 00:21:16 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:4-slim-bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:e78d07762beed9a0d300115ea5675084d05a3aa30bdf8cba3e5585bd8afc66e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2621282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3388884b886a7fd83f7d1b066becc4c06f98f88207189341697d024312e677bc`

```dockerfile
```

-	Layers:
	-	`sha256:c5ea76b781b81201794b44d87029ad59474afaa7c64943c20fea3ec8477ce43f`  
		Last Modified: Tue, 12 May 2026 00:21:16 GMT  
		Size: 2.6 MB (2597929 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:234c8d20765ef2121c643579ba80ed02288633b22bc12778a774b2434d093068`  
		Last Modified: Tue, 12 May 2026 00:21:16 GMT  
		Size: 23.4 KB (23353 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:4-slim-bookworm` - linux; 386

```console
$ docker pull ruby@sha256:9781ddd27e3c5cb0e1d3efe986aa8068285bc34693865ee295e625c4e9fa7b4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.5 MB (74497554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23c97447fe7414162d2122f12096db94bfa22f2e1568d5293f96f4dc6664b5a9`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1777939200'
# Tue, 12 May 2026 00:05:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 May 2026 00:05:29 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 12 May 2026 00:07:44 GMT
ENV LANG=C.UTF-8
# Tue, 12 May 2026 00:07:44 GMT
ENV RUBY_VERSION=4.0.4
# Tue, 12 May 2026 00:07:44 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/4.0/ruby-4.0.4.tar.xz
# Tue, 12 May 2026 00:07:44 GMT
ENV RUBY_DOWNLOAD_SHA256=6ff9d2d6e75f5a6f997222ecc45f79209d663737eceb3689d1f42ab952673fb7
# Tue, 12 May 2026 00:07:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 		${rustArch:+--enable-zjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 12 May 2026 00:07:44 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 12 May 2026 00:07:44 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 12 May 2026 00:07:44 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 00:07:44 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 12 May 2026 00:07:44 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:d90092c8edd324a692787fd4188906e71211941e12cf7df45f29d2b706aba9ab`  
		Last Modified: Fri, 08 May 2026 18:30:44 GMT  
		Size: 29.2 MB (29221767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac4343ab4dbbab26c84addca2a6440909782c2a37e9f11eae8aaf4490b4bcdf9`  
		Last Modified: Tue, 12 May 2026 00:07:53 GMT  
		Size: 3.5 MB (3514237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c1d26667cc805b3f350facd783a480e58b5da212d462423d06852d0a307a173`  
		Last Modified: Tue, 12 May 2026 00:07:53 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3b289026c451b53756cf8ea42d9389935b7a569f453889ab9de17988da12f2c`  
		Last Modified: Tue, 12 May 2026 00:07:55 GMT  
		Size: 41.8 MB (41761215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caa03ad4c2bf777d44fbd5d723f03dd6819bf137a6c238a21c38c50654d0e5e1`  
		Last Modified: Tue, 12 May 2026 00:07:53 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:4-slim-bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:6c6d1018be07b282ed83cce6010a050325b82d4dce270e26299943cccbf47981
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2618018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3fbc0ff176bb6a57950c9489466516d56022477bb3e72e43e228b4d60c145e9`

```dockerfile
```

-	Layers:
	-	`sha256:2ac54d4fa6e0b81bbe5f46e1127c7ca64ca4e180c5f2e39f15440321e885e268`  
		Last Modified: Tue, 12 May 2026 00:07:53 GMT  
		Size: 2.6 MB (2594852 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05220e38d1b586d1b3a22fe11ae6efdac309ee619d3ebfdb9a2563a7f5913f7a`  
		Last Modified: Tue, 12 May 2026 00:07:53 GMT  
		Size: 23.2 KB (23166 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:4-slim-bookworm` - linux; mips64le

```console
$ docker pull ruby@sha256:2ed8974dd6ebc9c8c7d8078e702ee6cbc8a9d82bd245e6981ad590843496bcbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.8 MB (74767702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d46608cd1111ae27c900ef466404902369256a9121f56fad772a1fc5bb59bf2`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1777939200'
# Sat, 09 May 2026 10:47:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 09 May 2026 10:47:02 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 12 May 2026 00:32:16 GMT
ENV LANG=C.UTF-8
# Tue, 12 May 2026 00:32:16 GMT
ENV RUBY_VERSION=4.0.4
# Tue, 12 May 2026 00:32:16 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/4.0/ruby-4.0.4.tar.xz
# Tue, 12 May 2026 00:32:16 GMT
ENV RUBY_DOWNLOAD_SHA256=6ff9d2d6e75f5a6f997222ecc45f79209d663737eceb3689d1f42ab952673fb7
# Tue, 12 May 2026 00:32:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 		${rustArch:+--enable-zjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 12 May 2026 00:32:16 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 12 May 2026 00:32:16 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 12 May 2026 00:32:16 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 00:32:18 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 12 May 2026 00:32:18 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:8e1a6f4f5a9e9628f902e3c8df639d1691d7f1000dc904f820155d1b9b2fa2ff`  
		Last Modified: Fri, 08 May 2026 18:20:04 GMT  
		Size: 28.5 MB (28526280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03245296ed4c53e7e3243a0fa73f65d2e35b8668cc7e9f3cc6607d0c1eca2a42`  
		Last Modified: Sat, 09 May 2026 11:03:47 GMT  
		Size: 2.9 MB (2902318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b375eb3b507d8c82f2f4acafad10d11d011df27cb70fb48ede1ed2a1978be7c`  
		Last Modified: Sat, 09 May 2026 11:03:46 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:334493b3024a678cb8c061e5c2e72e9b2b5ffb0ad9d37919a1e1f406a6ab3233`  
		Last Modified: Tue, 12 May 2026 00:33:03 GMT  
		Size: 43.3 MB (43338769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:975919265243e4b1c023bf3acb6770264882d99bd4bbaef25bc76516083137ef`  
		Last Modified: Tue, 12 May 2026 00:32:58 GMT  
		Size: 145.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:4-slim-bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:b9c5384b7240ecd07544183c68aa7ecad4e5dc1cf63610e6b8181863b9d692e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 KB (23064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32ab87297e109380de9d80ffea9c517e6ae70f6f8f8549d6f6f5d61534d5bd7a`

```dockerfile
```

-	Layers:
	-	`sha256:bc9a42c03d7a005922d2c56f200b2d65ed6340e79b8b76c22cc2f7f162f74b5b`  
		Last Modified: Tue, 12 May 2026 00:32:58 GMT  
		Size: 23.1 KB (23064 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:4-slim-bookworm` - linux; ppc64le

```console
$ docker pull ruby@sha256:717eff69159fc8c93ff8abcfe7c8db27c5da9e8c7394e4167189c0e743b5f1bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.7 MB (79652207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:974d61b7734088e5fef4f888070565127a51abaa7452ce961393f9890237229f`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1777939200'
# Sat, 09 May 2026 02:02:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 09 May 2026 02:02:28 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 12 May 2026 01:03:26 GMT
ENV LANG=C.UTF-8
# Tue, 12 May 2026 01:03:26 GMT
ENV RUBY_VERSION=4.0.4
# Tue, 12 May 2026 01:03:26 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/4.0/ruby-4.0.4.tar.xz
# Tue, 12 May 2026 01:03:26 GMT
ENV RUBY_DOWNLOAD_SHA256=6ff9d2d6e75f5a6f997222ecc45f79209d663737eceb3689d1f42ab952673fb7
# Tue, 12 May 2026 01:03:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 		${rustArch:+--enable-zjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 12 May 2026 01:03:26 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 12 May 2026 01:03:26 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 12 May 2026 01:03:26 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 01:03:26 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 12 May 2026 01:03:26 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:0e29ea7436ed4beb1c38bcfee44589407e49fc690669b42b35db33a9588e820a`  
		Last Modified: Fri, 08 May 2026 19:44:06 GMT  
		Size: 32.1 MB (32078453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffde109a7f36d8787d6dc2b8602d11b1d3e583896da3f19273d1024e6840ab62`  
		Last Modified: Sat, 09 May 2026 02:06:26 GMT  
		Size: 3.7 MB (3711891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a386e5a54e6ba22141a4bf874e54c80ebac21f8ea950f613ca335c685399549`  
		Last Modified: Sat, 09 May 2026 02:06:26 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68d3ab85fd5a808d410bd6157e010c1ea9d4a37f08168217155a1b18b4d36b5b`  
		Last Modified: Tue, 12 May 2026 01:03:47 GMT  
		Size: 43.9 MB (43861528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb78a04aa8c06cd29aa16bce95f70f86acf22b3e902d7ea27b82dce4d434e4ef`  
		Last Modified: Tue, 12 May 2026 01:03:46 GMT  
		Size: 145.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:4-slim-bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:a50a5d66836d5cd700edb8a05e1105fe6b142af2633ffbd07017ee40edab72d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2625316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44988628f5cf96fea800dee0db62df55ab9d91a760df7d272e69c6aa81d1a0cd`

```dockerfile
```

-	Layers:
	-	`sha256:2e7263441ec85411e8bbc819a95b01ced78cf353fcb9b7b9841b3956c45400ea`  
		Last Modified: Tue, 12 May 2026 01:03:46 GMT  
		Size: 2.6 MB (2602062 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6816a034060f1a5d067899bec985a8f1f870a1d3de7195feedf90c89c8850db`  
		Last Modified: Tue, 12 May 2026 01:03:46 GMT  
		Size: 23.3 KB (23254 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:4-slim-bookworm` - linux; s390x

```console
$ docker pull ruby@sha256:9df217b5f85830296171df84846c9ff06cf3ee80c9605a33beb81c4685bb966a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73155626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:921854be436a8666dc665a253334515f1cb926aeb5699df6529ccc3427793f4c`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1777939200'
# Tue, 12 May 2026 00:06:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 May 2026 00:06:41 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 12 May 2026 00:09:36 GMT
ENV LANG=C.UTF-8
# Tue, 12 May 2026 00:09:36 GMT
ENV RUBY_VERSION=4.0.4
# Tue, 12 May 2026 00:09:36 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/4.0/ruby-4.0.4.tar.xz
# Tue, 12 May 2026 00:09:36 GMT
ENV RUBY_DOWNLOAD_SHA256=6ff9d2d6e75f5a6f997222ecc45f79209d663737eceb3689d1f42ab952673fb7
# Tue, 12 May 2026 00:09:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 		${rustArch:+--enable-zjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 12 May 2026 00:09:36 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 12 May 2026 00:09:36 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 12 May 2026 00:09:36 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 00:09:36 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 12 May 2026 00:09:36 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:8e45267b009b7e1018e83fd0f228ba0ad9b97aea9f10520c2d76c3baa70dfe01`  
		Last Modified: Fri, 08 May 2026 18:27:33 GMT  
		Size: 26.9 MB (26891602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5bbb386086a73fa6455b55838bf67c1540c2367a10d30cb1479d8575fc9b174`  
		Last Modified: Tue, 12 May 2026 00:09:50 GMT  
		Size: 3.2 MB (3172030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86287415afbb6267a1c9a4d289acb50ec8d8df22151b6d80d1040d7295923f44`  
		Last Modified: Tue, 12 May 2026 00:09:50 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10e81293b4e55c48aaa49e3ec75230b118738bd034ee61e91dcdc24925456fb5`  
		Last Modified: Tue, 12 May 2026 00:09:50 GMT  
		Size: 43.1 MB (43091659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e8a10fafd95be6c269080968b5e86c49acecac9299927b2801f44bfc4852a3a`  
		Last Modified: Tue, 12 May 2026 00:09:46 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:4-slim-bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:3db51425518a3a2262825f1dac1a1aafd30cc17049a79fa8ec1a63774d9a76a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2617706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:835d3953d06d1609f8f7da6bbf9464bb145930f21cd68feb53dc687f0650780a`

```dockerfile
```

-	Layers:
	-	`sha256:20acf0ddc72206fbd817f271ca06907aa9796a99fde5689edefa1ccf7c32133f`  
		Last Modified: Tue, 12 May 2026 00:09:50 GMT  
		Size: 2.6 MB (2594502 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed51be14b3cea415e849e9b90aa9d4298b1cf709e753867105ecad0ee0d0c870`  
		Last Modified: Tue, 12 May 2026 00:09:50 GMT  
		Size: 23.2 KB (23204 bytes)  
		MIME: application/vnd.in-toto+json
