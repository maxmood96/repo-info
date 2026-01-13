## `ruby:slim-trixie`

```console
$ docker pull ruby@sha256:a94f84365c5e3bbf4bc2731527e45bd3477751f33b7da2043d755660774bd3b3
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

### `ruby:slim-trixie` - linux; amd64

```console
$ docker pull ruby@sha256:5d4dac01a81dcc671842355e5a32396eb9f4758ba8517ec8cd1133b580e09ba9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.6 MB (80644864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6eb5d2deafd200e6912651a1cf862f387de85e624da26feba15a87749f5b38f0`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 03:13:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 03:13:42 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 13 Jan 2026 03:16:00 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 03:16:00 GMT
ENV RUBY_VERSION=4.0.0
# Tue, 13 Jan 2026 03:16:00 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/4.0/ruby-4.0.0.tar.xz
# Tue, 13 Jan 2026 03:16:00 GMT
ENV RUBY_DOWNLOAD_SHA256=a72bacee9de07283ebc19baa4ac243b193129f21aa4e168c7186fb1fe7d07fe1
# Tue, 13 Jan 2026 03:16:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 		${rustArch:+--enable-zjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 13 Jan 2026 03:16:00 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 13 Jan 2026 03:16:00 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 13 Jan 2026 03:16:00 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:16:00 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 13 Jan 2026 03:16:00 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:119d43eec815e5f9a47da3a7d59454581b1e204b0c34db86f171b7ceb3336533`  
		Last Modified: Tue, 13 Jan 2026 00:42:34 GMT  
		Size: 29.8 MB (29773685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:673dca31808606a3c24067b1714841fc49fbf882e124a1d7d099e036eafc2ca0`  
		Last Modified: Tue, 13 Jan 2026 03:16:16 GMT  
		Size: 1.3 MB (1279351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34732783c723d9f375d67b9d091a7dbd598169edabbd1fbce5d0d2b77bf80779`  
		Last Modified: Tue, 13 Jan 2026 03:16:16 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:891c757f2f7a221efc8fea9fd0a029bfe642721025c6ff2bb57d1649af832375`  
		Last Modified: Tue, 13 Jan 2026 03:16:22 GMT  
		Size: 49.6 MB (49591497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d725832902b6979f134e5dbb1fc2a9feefaf970eabf8810e0d3c0bf312f4864`  
		Last Modified: Tue, 13 Jan 2026 03:16:17 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim-trixie` - unknown; unknown

```console
$ docker pull ruby@sha256:a091a06fc2abdad9b3ce8b3d14ed94195d3907fa9939d6bb209658fa3fc67df6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2240318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61c7bd1dbd3376253b9dd9e6edb1da9420ebbd3d2fe025b2b5461e0b52d052bd`

```dockerfile
```

-	Layers:
	-	`sha256:e198779519c9b217c7a285e24d84a3b8ca8b35d612c4f626ebe6043b4ea547ce`  
		Last Modified: Tue, 13 Jan 2026 07:04:31 GMT  
		Size: 2.2 MB (2215998 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8c13682cc9ddea61ed0284472b0df98dd6cad5549b971e6b5d4c3a7aedb55af`  
		Last Modified: Tue, 13 Jan 2026 07:04:32 GMT  
		Size: 24.3 KB (24320 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:slim-trixie` - linux; arm variant v5

```console
$ docker pull ruby@sha256:8e013b624f8f88b21328c3a2061a272b65fcf48c64c459d00fc86d2206cce316
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.8 MB (71836005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:facb2a254c53ece0457e06b35c806238f1ff62366079e0ef4d4834c23a6a9bed`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 03:22:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 03:22:20 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 13 Jan 2026 03:25:25 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 03:25:25 GMT
ENV RUBY_VERSION=4.0.0
# Tue, 13 Jan 2026 03:25:25 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/4.0/ruby-4.0.0.tar.xz
# Tue, 13 Jan 2026 03:25:25 GMT
ENV RUBY_DOWNLOAD_SHA256=a72bacee9de07283ebc19baa4ac243b193129f21aa4e168c7186fb1fe7d07fe1
# Tue, 13 Jan 2026 03:25:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 		${rustArch:+--enable-zjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 13 Jan 2026 03:25:25 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 13 Jan 2026 03:25:25 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 13 Jan 2026 03:25:25 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:25:25 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 13 Jan 2026 03:25:25 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:c113d410d30c2c035a105b56d3937958c81fbe2530f44add3bae903be6864324`  
		Last Modified: Tue, 13 Jan 2026 00:42:30 GMT  
		Size: 27.9 MB (27942724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d99f8b7095beb17f383de2c4db5f74239f5ed601a639951f427aefb184a5afff`  
		Last Modified: Tue, 13 Jan 2026 03:25:40 GMT  
		Size: 1.3 MB (1263006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d8ef493b924180a76cdfd106cd1a4f4f4b7145a80eca8a23dc22b7be9228e30`  
		Last Modified: Tue, 13 Jan 2026 03:25:40 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecb80145af4ffc3f4cd3b95dae35ae7098c1f5c6397d67fea794471bacd59831`  
		Last Modified: Tue, 13 Jan 2026 03:25:43 GMT  
		Size: 42.6 MB (42629942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32aa3b822f4a708b040ff995d8d85935f217f6cd80acda31aa02ccf4822347c8`  
		Last Modified: Tue, 13 Jan 2026 03:25:40 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim-trixie` - unknown; unknown

```console
$ docker pull ruby@sha256:e849fdea66527339ac4a599434e6befdcf2993e6d362ef8ab9b5ae3ea7918b67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2243464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:513f90b386f69b94f3cf28fe5ecc88350e0d2f6b562df2d303cc55c4f9ded251`

```dockerfile
```

-	Layers:
	-	`sha256:6ff0b80ff27a4b3390b50bfb4887ee527b0f8d148e9bb8d714733835b8bc6b8a`  
		Last Modified: Tue, 13 Jan 2026 07:04:35 GMT  
		Size: 2.2 MB (2218993 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3142094e127b28e56b859a93a156fe7358737ee933ce619f82abee2681adafe`  
		Last Modified: Tue, 13 Jan 2026 07:04:36 GMT  
		Size: 24.5 KB (24471 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:slim-trixie` - linux; arm variant v7

```console
$ docker pull ruby@sha256:429fb42f5fa2b306e271e2823db5dd43b7201391c7db8ea06195a2384bc95eb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69914287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd3426042d42b2379a0a2b2ad6b2fedb1a77e77d862905cecb59dd10240b5e5b`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 04:00:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 04:00:02 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 13 Jan 2026 04:02:45 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 04:02:45 GMT
ENV RUBY_VERSION=4.0.0
# Tue, 13 Jan 2026 04:02:45 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/4.0/ruby-4.0.0.tar.xz
# Tue, 13 Jan 2026 04:02:45 GMT
ENV RUBY_DOWNLOAD_SHA256=a72bacee9de07283ebc19baa4ac243b193129f21aa4e168c7186fb1fe7d07fe1
# Tue, 13 Jan 2026 04:02:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 		${rustArch:+--enable-zjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 13 Jan 2026 04:02:45 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 13 Jan 2026 04:02:45 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 13 Jan 2026 04:02:45 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 04:02:45 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 13 Jan 2026 04:02:45 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:7c33f0ee8e5c8636ae24c5685841e42e721bbb2973888f046a05ab9eb619e682`  
		Last Modified: Tue, 13 Jan 2026 00:42:33 GMT  
		Size: 26.2 MB (26208578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc9f3a993b032ae2df6760d37be2b162686768138751833f72bc72c075ef44e8`  
		Last Modified: Tue, 13 Jan 2026 04:03:00 GMT  
		Size: 1.2 MB (1236548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97eaf59aa3966a29eb361f41453e81fb7b1b556b3abf8e7fe8d638d7277d7625`  
		Last Modified: Tue, 13 Jan 2026 04:03:01 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a822d40c00df80f3016fd983cf7044d4816753bd1ffaf6602b292a38c378bb25`  
		Last Modified: Tue, 13 Jan 2026 04:03:03 GMT  
		Size: 42.5 MB (42468829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85d99d3d5edd8f942094a5c25f8ffb2d032d7fda1734552bbbc1277eaed27a73`  
		Last Modified: Tue, 13 Jan 2026 04:03:00 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim-trixie` - unknown; unknown

```console
$ docker pull ruby@sha256:2ee1543c55f64a659a7edf8cc9e7746931424fb95deacd7fb2ce0d84ad703f9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2241905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c9c0050e6df9b15e23ee73ffbcd5c8b6290af6599f5ae4543c7a2e9e1854867`

```dockerfile
```

-	Layers:
	-	`sha256:0708061ce9973afd0e1b4034db96d1ef16cf9482797dcd4f24313449ff78d775`  
		Last Modified: Tue, 13 Jan 2026 07:04:40 GMT  
		Size: 2.2 MB (2217434 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3126bfd7ab85fdc16e8e6b842f4c1a30ed2228c01e2e20935ec8effd1f4e3131`  
		Last Modified: Tue, 13 Jan 2026 07:04:41 GMT  
		Size: 24.5 KB (24471 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:slim-trixie` - linux; arm64 variant v8

```console
$ docker pull ruby@sha256:092fd458d9a255f9de9e82d624743603b9743610670cdcff2f09d59fdcb87622
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.9 MB (80853112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c39b58b10bae3eb418a96f0972576b21f4a552868ffceae6ef1810947603572`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 03:22:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 03:22:35 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 13 Jan 2026 03:25:01 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 03:25:01 GMT
ENV RUBY_VERSION=4.0.0
# Tue, 13 Jan 2026 03:25:01 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/4.0/ruby-4.0.0.tar.xz
# Tue, 13 Jan 2026 03:25:01 GMT
ENV RUBY_DOWNLOAD_SHA256=a72bacee9de07283ebc19baa4ac243b193129f21aa4e168c7186fb1fe7d07fe1
# Tue, 13 Jan 2026 03:25:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 		${rustArch:+--enable-zjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 13 Jan 2026 03:25:01 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 13 Jan 2026 03:25:01 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 13 Jan 2026 03:25:01 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:25:01 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 13 Jan 2026 03:25:01 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:d637807aba98f742a62ad9b0146579ceb0297a3c831f56b2361664b7f5fbc75b`  
		Last Modified: Tue, 13 Jan 2026 00:42:49 GMT  
		Size: 30.1 MB (30134042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26fa3a326a7462c8b631985adf338258e251160ae1d9a0c003bdcc7c949de647`  
		Last Modified: Tue, 13 Jan 2026 03:25:17 GMT  
		Size: 1.3 MB (1261700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4120573054c800769a7e8b6c3749b1f888a26623150eca45fe708dd657b95c0e`  
		Last Modified: Tue, 13 Jan 2026 03:25:17 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:286a8187559bfc4a5129bfdcaf07d0a07a0a375187e6364a08801173e9203083`  
		Last Modified: Tue, 13 Jan 2026 03:25:21 GMT  
		Size: 49.5 MB (49457036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b89812b1ed5211854de8af05c56cc2fb2700e4978f813bca649751836d510533`  
		Last Modified: Tue, 13 Jan 2026 03:25:17 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim-trixie` - unknown; unknown

```console
$ docker pull ruby@sha256:3ff6fcc925df21efd012ac58265e0e88c0bfb24288ac6847cf4abf6747a10a2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2240822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa3e64b7ec2c909d5db347035e1f4b6c4028412d216dac20ca6b58833b37c83e`

```dockerfile
```

-	Layers:
	-	`sha256:6dbb9870cd34ae676759d0fbfee9959f37a6f686ef56893bcadc3204e8a93bab`  
		Last Modified: Tue, 13 Jan 2026 07:04:44 GMT  
		Size: 2.2 MB (2216306 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4645225d6fdc59a83a3c7fc75a9a923c7013ea3a2978709b042766a200922e1`  
		Last Modified: Tue, 13 Jan 2026 07:04:45 GMT  
		Size: 24.5 KB (24516 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:slim-trixie` - linux; 386

```console
$ docker pull ruby@sha256:4cad849f6d6f691b3b1ad380ae3d4110bc89330219454f9f42deada5be53538a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.9 MB (74945586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f646a1f6bd8045666e6a59c8b88e2c3d36bad9de3fb92abb18355403c824d06a`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:44:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 02:44:59 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 13 Jan 2026 02:47:11 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 02:47:11 GMT
ENV RUBY_VERSION=4.0.0
# Tue, 13 Jan 2026 02:47:11 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/4.0/ruby-4.0.0.tar.xz
# Tue, 13 Jan 2026 02:47:11 GMT
ENV RUBY_DOWNLOAD_SHA256=a72bacee9de07283ebc19baa4ac243b193129f21aa4e168c7186fb1fe7d07fe1
# Tue, 13 Jan 2026 02:47:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 		${rustArch:+--enable-zjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 13 Jan 2026 02:47:11 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 13 Jan 2026 02:47:11 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 13 Jan 2026 02:47:11 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 02:47:12 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 13 Jan 2026 02:47:12 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:27bb6d39eda5ced7626db280c3902aacdfade5acd11a16ef9618e3185f69b102`  
		Last Modified: Tue, 13 Jan 2026 00:43:03 GMT  
		Size: 31.3 MB (31288476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e470826b1db3717d973009cb3ce4fc6393d08e471f061b87fe01d15ce53427e9`  
		Last Modified: Tue, 13 Jan 2026 02:47:27 GMT  
		Size: 1.3 MB (1287223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f4fa0e56904d070b17360e13c6f32d6983c1d018528e7a06e857ead63c49c62`  
		Last Modified: Tue, 13 Jan 2026 02:47:27 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f468f6c3926fa015dcafdc853aea37f6b04eb6449be31c59038e29239ef57aed`  
		Last Modified: Tue, 13 Jan 2026 02:47:30 GMT  
		Size: 42.4 MB (42369556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4d2ac9dbddba5ac0e5e88b52f4bdba5de915975504673d7308cf800b9a739fa`  
		Last Modified: Tue, 13 Jan 2026 02:47:27 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim-trixie` - unknown; unknown

```console
$ docker pull ruby@sha256:9305b9a29ee58c051d315058fbdded880ba92fcd1b3d1aa59cabeb23fec7fab6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2237431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ece2aced1afb7e81293a6909a8175e0806a7585f2305f65e4d81adf1b638a468`

```dockerfile
```

-	Layers:
	-	`sha256:e8e3e4edd5f5cadcda215e575490a550e50bde522f7103dfce872a9172cb0f3b`  
		Last Modified: Tue, 13 Jan 2026 04:02:29 GMT  
		Size: 2.2 MB (2213171 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:629115c9f71b3cdbc280ad2ad7fda32285accb0911383d96cc0d7f1f8352f20e`  
		Last Modified: Tue, 13 Jan 2026 04:02:30 GMT  
		Size: 24.3 KB (24260 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:slim-trixie` - linux; ppc64le

```console
$ docker pull ruby@sha256:de975004623652b86768edcd998455cdf3456995b199f682e91006d40523d8d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.3 MB (79337393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b051572a65144b20d25bee5fcc9f195324f966eb15d1fd26315c4027406356c`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 05:13:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 05:13:58 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 13 Jan 2026 05:19:02 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 05:19:02 GMT
ENV RUBY_VERSION=4.0.0
# Tue, 13 Jan 2026 05:19:02 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/4.0/ruby-4.0.0.tar.xz
# Tue, 13 Jan 2026 05:19:02 GMT
ENV RUBY_DOWNLOAD_SHA256=a72bacee9de07283ebc19baa4ac243b193129f21aa4e168c7186fb1fe7d07fe1
# Tue, 13 Jan 2026 05:19:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 		${rustArch:+--enable-zjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 13 Jan 2026 05:19:02 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 13 Jan 2026 05:19:02 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 13 Jan 2026 05:19:02 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 05:19:03 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 13 Jan 2026 05:19:03 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:9a275bb13cf8b3e9db52a41b6b4ff22ee1ffed00394f6deddd2de45044bd3bae`  
		Last Modified: Tue, 13 Jan 2026 00:57:13 GMT  
		Size: 33.6 MB (33595600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbd359a7e5d3b012a0e1f773e5ca872b7185e1ae4c53f7a9a7d797ae3eaaf8fb`  
		Last Modified: Tue, 13 Jan 2026 05:19:33 GMT  
		Size: 1.3 MB (1309726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49eeff64fa1ee2c5a20375771788d22ec3d5ad95481b75598a70ada63b47d8fb`  
		Last Modified: Tue, 13 Jan 2026 05:19:33 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:399af5b6d2141012bb42556f03ccbffcf1ec521afaaa7e51d80d45381f9cc936`  
		Last Modified: Tue, 13 Jan 2026 05:19:38 GMT  
		Size: 44.4 MB (44431734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d6649a4def52f6369b7b4787619e5db36f1414bc5abf04839b1127baef0ebc8`  
		Last Modified: Tue, 13 Jan 2026 05:19:33 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim-trixie` - unknown; unknown

```console
$ docker pull ruby@sha256:4e8b6e16c1bce425d86828ef240de63e30b7f398fbe7151868f865147f733770
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2243945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2901748e8885d4c57afb0f6a670609a85629bcc695c9e4b5c1b54e0bc92258c5`

```dockerfile
```

-	Layers:
	-	`sha256:1577f2e154fdb8b2fcf48f4afd8bcd86a07a68f7a7ce3305d91c887e0e8a1bac`  
		Last Modified: Tue, 13 Jan 2026 07:04:51 GMT  
		Size: 2.2 MB (2219551 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c7c227698ad81c7782371bdfd51471adbbf990378cea4e36f931f4cb8f242a5`  
		Last Modified: Tue, 13 Jan 2026 07:04:52 GMT  
		Size: 24.4 KB (24394 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:slim-trixie` - linux; riscv64

```console
$ docker pull ruby@sha256:c9cd73ac3095689b9799bc73d0c91436f24e669dec859b895182980c6eb6cca7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.7 MB (73651761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acfea62e2808ffa2be779629831176ec1a1a53e1be8d969b89680a10cd474ac6`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1766966400'
# Thu, 01 Jan 2026 00:48:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Thu, 01 Jan 2026 00:48:48 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 01 Jan 2026 02:48:10 GMT
ENV LANG=C.UTF-8
# Thu, 01 Jan 2026 02:48:10 GMT
ENV RUBY_VERSION=4.0.0
# Thu, 01 Jan 2026 02:48:10 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/4.0/ruby-4.0.0.tar.xz
# Thu, 01 Jan 2026 02:48:10 GMT
ENV RUBY_DOWNLOAD_SHA256=a72bacee9de07283ebc19baa4ac243b193129f21aa4e168c7186fb1fe7d07fe1
# Thu, 01 Jan 2026 02:48:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 		${rustArch:+--enable-zjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 01 Jan 2026 02:48:10 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 01 Jan 2026 02:48:10 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 01 Jan 2026 02:48:10 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Jan 2026 02:48:10 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 01 Jan 2026 02:48:10 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:96d8ad310358e2403b7b44cf38db606dc1ea6b58b915684d38e13f573860f64e`  
		Last Modified: Tue, 30 Dec 2025 00:53:22 GMT  
		Size: 28.3 MB (28273129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1ce77dcf592ef0e38ea136a7a369fefa0b1f7344af06ddda7fe23bdc6137c01`  
		Last Modified: Thu, 01 Jan 2026 02:50:19 GMT  
		Size: 1.2 MB (1247995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16c437f0ef83daf3a2b76a2c51d38c272b6e91fed0d67191ae359042c82544b7`  
		Last Modified: Thu, 01 Jan 2026 02:50:19 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01ff002d765f2b57945d23334ee6dc53a9180218f61de6a49a6b3c0a85aa301f`  
		Last Modified: Thu, 01 Jan 2026 02:50:24 GMT  
		Size: 44.1 MB (44130303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58b49befd780dae9a51922c3a6a845f5f1bc892bd06354aa7dab40b76ef023ff`  
		Last Modified: Thu, 01 Jan 2026 02:50:19 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim-trixie` - unknown; unknown

```console
$ docker pull ruby@sha256:0ba73ada672e8fce61b1dc5e6bee276c5457f02e53ec7b0ba5cdce2a66020827
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2234278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05789acecf110baadbbbdcdb796a18bda23f5007127b6e267b451ec399005e75`

```dockerfile
```

-	Layers:
	-	`sha256:d464563755eb5a534e1fd0a252c18b45ee91543a67e8a1660e6b2b778acbaa4c`  
		Last Modified: Thu, 01 Jan 2026 03:59:11 GMT  
		Size: 2.2 MB (2209884 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ed63242ace56221c29f739334f761f775d64f51eb50c6fa97a7f24f6e3c9067`  
		Last Modified: Thu, 01 Jan 2026 03:59:12 GMT  
		Size: 24.4 KB (24394 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:slim-trixie` - linux; s390x

```console
$ docker pull ruby@sha256:6f4a20bff04a2d7762882293652b2e3f1f3e3ffc4ea74958140b2bd3fee17219
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75393144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2636c807d8c8c2fdd47729f84fafb66030aa26bb11cc6bb09912f018970927a1`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 15:29:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 15:29:54 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 13 Jan 2026 15:32:35 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 15:32:35 GMT
ENV RUBY_VERSION=4.0.0
# Tue, 13 Jan 2026 15:32:35 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/4.0/ruby-4.0.0.tar.xz
# Tue, 13 Jan 2026 15:32:35 GMT
ENV RUBY_DOWNLOAD_SHA256=a72bacee9de07283ebc19baa4ac243b193129f21aa4e168c7186fb1fe7d07fe1
# Tue, 13 Jan 2026 15:32:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 		${rustArch:+--enable-zjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 13 Jan 2026 15:32:35 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 13 Jan 2026 15:32:35 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 13 Jan 2026 15:32:35 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 15:32:35 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 13 Jan 2026 15:32:35 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:2b46bc94baaae0a37e5e04b1babf7e1f37c4390b83d49c3c6820188deba770e3`  
		Last Modified: Tue, 13 Jan 2026 13:10:43 GMT  
		Size: 29.8 MB (29833411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:565d59f5e4a35f20c4a13bf7c026d7d351d091ee74371507d8e03a1d10a08ff2`  
		Last Modified: Tue, 13 Jan 2026 15:32:53 GMT  
		Size: 1.3 MB (1294308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a775b7229bcd359e4b03cb3ebbc34fd6e5733561031ec3a97ce984765d7a6fd`  
		Last Modified: Tue, 13 Jan 2026 15:32:53 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b56402deba6b80e840b8c948d2214b3ffde2612f4c410a909f56d528b8e64753`  
		Last Modified: Tue, 13 Jan 2026 15:32:57 GMT  
		Size: 44.3 MB (44265092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb07633fca3e67aa506facb80cf58933758e761e119a8bd451f684f2076ba460`  
		Last Modified: Tue, 13 Jan 2026 15:32:53 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim-trixie` - unknown; unknown

```console
$ docker pull ruby@sha256:23d19985f26f4b07afff3eacc3ddf60c4ff83e6e8a995130ee963f3a16e547a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2241763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baffdef02df5230f224a9d7b69c14f396ea3819be546c1a3b47525bc7ff94125`

```dockerfile
```

-	Layers:
	-	`sha256:46a9b66dea92950c1b36beaec1d9b5bd256dc3193b14f1d65f09cd833f7a444f`  
		Last Modified: Tue, 13 Jan 2026 15:32:49 GMT  
		Size: 2.2 MB (2217443 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f80dd5696c67397deda7614503c52fe2850ee7d2b46ce35ef06f48be561f5d8`  
		Last Modified: Tue, 13 Jan 2026 15:32:49 GMT  
		Size: 24.3 KB (24320 bytes)  
		MIME: application/vnd.in-toto+json
