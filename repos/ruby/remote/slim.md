## `ruby:slim`

```console
$ docker pull ruby@sha256:7e98b0446142b30dd4bbf298d13a09735c27abc93d1eece0ca787b19cdac20b2
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

### `ruby:slim` - linux; amd64

```console
$ docker pull ruby@sha256:a999dafec96ed9550294e0839bf8aa03f0bdb5757b2959b932826f58e9507d74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73204908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c8daae4f1bd9b59966fd5b1f4acbaab1511cfa89db94a482cef075e216ce2f1`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
# Tue, 16 Sep 2025 05:03:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 16 Sep 2025 05:03:19 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 16 Sep 2025 05:03:19 GMT
ENV LANG=C.UTF-8
# Tue, 16 Sep 2025 05:03:19 GMT
ENV RUBY_VERSION=3.4.6
# Tue, 16 Sep 2025 05:03:19 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.6.tar.xz
# Tue, 16 Sep 2025 05:03:19 GMT
ENV RUBY_DOWNLOAD_SHA256=804995bc22938aa475127000d3103cb133409ad3955edfc0e7412be66a4859b8
# Tue, 16 Sep 2025 05:03:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 16 Sep 2025 05:03:19 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 16 Sep 2025 05:03:19 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 16 Sep 2025 05:03:19 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Sep 2025 05:03:19 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 16 Sep 2025 05:03:19 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:ce1261c6d567efa8e3b457673eeeb474a0a8066df6bb95ca9a6a94a31e219dd3`  
		Last Modified: Mon, 08 Sep 2025 21:12:35 GMT  
		Size: 29.8 MB (29773495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1feea5fc2ae33b0a4b825846c8e26a354f80887f1279d73b48ceb27585e3cbc6`  
		Last Modified: Tue, 16 Sep 2025 17:08:41 GMT  
		Size: 1.3 MB (1279284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f4ef17867cd58f87d70bc4070d1784eae5b6d6f00d161f74a5af7e3282ff269`  
		Last Modified: Tue, 16 Sep 2025 17:08:41 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84c6b5c8420fba13bbccbbd25f54ba7cd24a322437d4befc583d1125f8331f73`  
		Last Modified: Tue, 16 Sep 2025 17:08:45 GMT  
		Size: 42.2 MB (42151794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60ff1d346d9a03fbb2a9bb71a3c4cbfdc7d83da635b43871dbfeb9fb1e3f992e`  
		Last Modified: Tue, 16 Sep 2025 17:08:41 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim` - unknown; unknown

```console
$ docker pull ruby@sha256:7e51ee7ff389bca68f6a64e4deaf0ad8d7774a5eb733e0b662bcb6c205ce522d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2244127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb54794f0e77c3a2659f57dc2c9b33704973797eee813a6453c22cb9ec04da99`

```dockerfile
```

-	Layers:
	-	`sha256:57f2b8a9d2b25693307c07513d98a5e1f0aa49788dd1a5c274ab15937392e51a`  
		Last Modified: Tue, 16 Sep 2025 17:59:23 GMT  
		Size: 2.2 MB (2219877 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3580717eb3baa880b5426740e4e3d39d20eb8696be5026410c7538d0dd97ecaa`  
		Last Modified: Tue, 16 Sep 2025 17:59:24 GMT  
		Size: 24.2 KB (24250 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:slim` - linux; arm variant v5

```console
$ docker pull ruby@sha256:ae578eaeb123538b2a76883d7af02d17061904868151a91622104b9fe59bf4f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.2 MB (67195316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:080aef97107628706e28f82ffefb5f48d889a7b6a25ad3c1f779ef4105f4fd92`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1757289600'
# Tue, 16 Sep 2025 05:03:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 16 Sep 2025 05:03:19 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 16 Sep 2025 05:03:19 GMT
ENV LANG=C.UTF-8
# Tue, 16 Sep 2025 05:03:19 GMT
ENV RUBY_VERSION=3.4.6
# Tue, 16 Sep 2025 05:03:19 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.6.tar.xz
# Tue, 16 Sep 2025 05:03:19 GMT
ENV RUBY_DOWNLOAD_SHA256=804995bc22938aa475127000d3103cb133409ad3955edfc0e7412be66a4859b8
# Tue, 16 Sep 2025 05:03:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 16 Sep 2025 05:03:19 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 16 Sep 2025 05:03:19 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 16 Sep 2025 05:03:19 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Sep 2025 05:03:19 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 16 Sep 2025 05:03:19 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:5d61fc20e756831552727f89a087e2b45b07dace604ad2cda0a2afa80ace388d`  
		Last Modified: Mon, 08 Sep 2025 21:13:29 GMT  
		Size: 27.9 MB (27941760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16251884281942f8c1a727b86764c32d2dbda49656bbdca3ee64a771a772d738`  
		Last Modified: Tue, 16 Sep 2025 17:05:44 GMT  
		Size: 1.3 MB (1262781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86b88ee2e6ca1509675e0d2eacd371cab4c2a561631cc7a1c85439adf8cfdb62`  
		Last Modified: Tue, 16 Sep 2025 17:05:44 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c17fdd5776c6451952e8fd97ebf127657cd25958c922b71f3b4c4c47d28fccc`  
		Last Modified: Tue, 16 Sep 2025 17:05:47 GMT  
		Size: 38.0 MB (37990442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a911e815f7b735733fcfa5618982846751aa99d1d05a16bbd5b11f8ca53b6053`  
		Last Modified: Tue, 16 Sep 2025 17:05:44 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim` - unknown; unknown

```console
$ docker pull ruby@sha256:1cc60d5626659da24c7eb7c62a739b8a851a81785bae954d726d342ef6405dfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2247272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaed6f8576d8f6fb4dee02cbb2c944e1c10a90053bce71f6272db9407ed24213`

```dockerfile
```

-	Layers:
	-	`sha256:617cba68cde3887f07768a0e7518f4bd56e13e10026043bda3532cc90318e944`  
		Last Modified: Tue, 16 Sep 2025 17:59:27 GMT  
		Size: 2.2 MB (2222872 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:967194b5a2e1507325ff72558427063ae08b68a25adc39ad6af5ae8674c58213`  
		Last Modified: Tue, 16 Sep 2025 17:59:28 GMT  
		Size: 24.4 KB (24400 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:slim` - linux; arm variant v7

```console
$ docker pull ruby@sha256:fb83b65800b68fb2b7042871c76d2547e47b893a730768bddc3d7b6bdb6d4261
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.3 MB (65301735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fa367bc364bc10eaaa783317f471628ab5e60d35d5fb4691ee9ce334e759439`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1757289600'
# Tue, 16 Sep 2025 05:03:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 16 Sep 2025 05:03:19 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 16 Sep 2025 05:03:19 GMT
ENV LANG=C.UTF-8
# Tue, 16 Sep 2025 05:03:19 GMT
ENV RUBY_VERSION=3.4.6
# Tue, 16 Sep 2025 05:03:19 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.6.tar.xz
# Tue, 16 Sep 2025 05:03:19 GMT
ENV RUBY_DOWNLOAD_SHA256=804995bc22938aa475127000d3103cb133409ad3955edfc0e7412be66a4859b8
# Tue, 16 Sep 2025 05:03:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 16 Sep 2025 05:03:19 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 16 Sep 2025 05:03:19 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 16 Sep 2025 05:03:19 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Sep 2025 05:03:19 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 16 Sep 2025 05:03:19 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:c01338083e94735040ac705e73d3207fecb1a829de94334396239199538796bd`  
		Last Modified: Mon, 08 Sep 2025 21:13:56 GMT  
		Size: 26.2 MB (26207847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96565be4d07605304ab01ed88ddb2422c09d2c097a7a6bd9e908ecc538bc41b6`  
		Last Modified: Tue, 16 Sep 2025 17:54:46 GMT  
		Size: 1.2 MB (1235933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89241ff1b55720625ba104e27a7ae55ed5d7f05f7cc70232c509ad4e8c98a25a`  
		Last Modified: Tue, 16 Sep 2025 17:54:45 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f16cfac0646ebc1380322334d36097689728babfc80127206b89b48da79bb9f1`  
		Last Modified: Tue, 16 Sep 2025 17:54:49 GMT  
		Size: 37.9 MB (37857621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85f2c1c0258f47c00e65e5e3ad5da5d3b1bcb59afa40ef39f4100c885d6657d9`  
		Last Modified: Tue, 16 Sep 2025 17:54:46 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim` - unknown; unknown

```console
$ docker pull ruby@sha256:f98f7d6d18d73a3c09dbb669be7e41813f42ac7bcb67f917d14bdc3a80449100
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2245714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9d564577b7ca08161efd89e29fbf6ccb34107e5cdfa61a92010344b3acd53b6`

```dockerfile
```

-	Layers:
	-	`sha256:310bae59f05120f4fa5bba38026bfb791e2e2a0c658db09342586c0b02d5b533`  
		Last Modified: Tue, 16 Sep 2025 17:59:32 GMT  
		Size: 2.2 MB (2221313 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48888f22b94bf541cd86a39f947cce8bae25789b69a2b409f0bf7ded7accc5c5`  
		Last Modified: Tue, 16 Sep 2025 17:59:32 GMT  
		Size: 24.4 KB (24401 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:slim` - linux; arm64 variant v8

```console
$ docker pull ruby@sha256:6bafa232f6dc8b3c1f91914541c665f8e76d7919143121a288f6b0a516a49d4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.5 MB (73531361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c37c2c84be10eaecf4039bea593acbc6a6183272d960e55b68a13defda6c73f`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1757289600'
# Tue, 16 Sep 2025 05:03:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 16 Sep 2025 05:03:19 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 16 Sep 2025 05:03:19 GMT
ENV LANG=C.UTF-8
# Tue, 16 Sep 2025 05:03:19 GMT
ENV RUBY_VERSION=3.4.6
# Tue, 16 Sep 2025 05:03:19 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.6.tar.xz
# Tue, 16 Sep 2025 05:03:19 GMT
ENV RUBY_DOWNLOAD_SHA256=804995bc22938aa475127000d3103cb133409ad3955edfc0e7412be66a4859b8
# Tue, 16 Sep 2025 05:03:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 16 Sep 2025 05:03:19 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 16 Sep 2025 05:03:19 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 16 Sep 2025 05:03:19 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Sep 2025 05:03:19 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 16 Sep 2025 05:03:19 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:b2feff975e6dd2ebaf182772fb9ee26274648387b061e821e0bb5026735dd094`  
		Last Modified: Mon, 08 Sep 2025 21:13:54 GMT  
		Size: 30.1 MB (30136631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e34425e9a9c6e82827dc5ccbdc05696ab59c93c6a3f9037bb6cbe805a7f5abde`  
		Last Modified: Tue, 16 Sep 2025 17:07:41 GMT  
		Size: 1.3 MB (1260872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:390acc4c37285a6ee478f4264f2ed3d9213800b2014c5e93735666031c27f238`  
		Last Modified: Tue, 16 Sep 2025 17:07:35 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80fd0f854246fa6759c30ec6ea097df9bd3949fbdecd97382a03be0640882a4d`  
		Last Modified: Tue, 16 Sep 2025 17:07:40 GMT  
		Size: 42.1 MB (42133523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d3945d4c7194481fe1acfb2b5afb156034f860a15810a9f917eeaa6e2d5b0fb`  
		Last Modified: Tue, 16 Sep 2025 17:07:35 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim` - unknown; unknown

```console
$ docker pull ruby@sha256:24756d7d24de08f524ae557e5734a236207f77bd6712487fcbfabc4d730aec7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2244632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5ca669dd654a4e46c37d2a46235b7d8d92d640b5956f20cb96653f78205c62d`

```dockerfile
```

-	Layers:
	-	`sha256:c435599732ae26527c1c6a4f6a15b1449e6052457af9f44d351d892f76ce20e2`  
		Last Modified: Tue, 16 Sep 2025 17:59:36 GMT  
		Size: 2.2 MB (2220185 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:902bf0000aad41cf9493f3647c7860eec02ab959334bd49732a43ea5eb7bf650`  
		Last Modified: Tue, 16 Sep 2025 17:59:37 GMT  
		Size: 24.4 KB (24447 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:slim` - linux; 386

```console
$ docker pull ruby@sha256:72f5f12e8a348e8c89187ea5deb069362f07e348f1139fb47eea65ec8e528bc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.3 MB (70319195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71eaa974e9ff2ed8d3c15f981b1533a69121176c589e93360901cd1226702954`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1757289600'
# Tue, 16 Sep 2025 05:03:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 16 Sep 2025 05:03:19 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 16 Sep 2025 05:03:19 GMT
ENV LANG=C.UTF-8
# Tue, 16 Sep 2025 05:03:19 GMT
ENV RUBY_VERSION=3.4.6
# Tue, 16 Sep 2025 05:03:19 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.6.tar.xz
# Tue, 16 Sep 2025 05:03:19 GMT
ENV RUBY_DOWNLOAD_SHA256=804995bc22938aa475127000d3103cb133409ad3955edfc0e7412be66a4859b8
# Tue, 16 Sep 2025 05:03:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 16 Sep 2025 05:03:19 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 16 Sep 2025 05:03:19 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 16 Sep 2025 05:03:19 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Sep 2025 05:03:19 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 16 Sep 2025 05:03:19 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:d6e01c57fc6d674eef68e6bfe57a080b0a70c1c25810b7d6e769151bad3645bf`  
		Last Modified: Mon, 08 Sep 2025 21:12:32 GMT  
		Size: 31.3 MB (31289784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cfccc11597466802b93739e3d293a397b5bdc82c0e43753fe3cc62c820b7958`  
		Last Modified: Tue, 16 Sep 2025 17:09:46 GMT  
		Size: 1.3 MB (1286800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ccefcd32ae12ecf4f8dd90718ebb85b8cf8940b8bcb73918615776a27a94ee2`  
		Last Modified: Tue, 16 Sep 2025 17:09:35 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:178850de12fba3b2bf8c9636b61297567adca5831fd3e5169c9e25978c9f2fd8`  
		Last Modified: Tue, 16 Sep 2025 17:09:50 GMT  
		Size: 37.7 MB (37742275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc1d23e5ffb1c85d87cd53dae6c4bd0635888f6e7f02b5288011fb836ba296c9`  
		Last Modified: Tue, 16 Sep 2025 17:09:46 GMT  
		Size: 145.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim` - unknown; unknown

```console
$ docker pull ruby@sha256:9abe150f00c0b1170fdd852b126745219d1dea9091cc644f623ad81f995868ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2241242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a2e5aca695c2d75ca778f26e99a06afd790e8b4686dbaa66d02569c879ffe06`

```dockerfile
```

-	Layers:
	-	`sha256:dee0b1003d08c9e26c0c088723cdb82f37cb0077a62727aee39c597f9d3eeb2b`  
		Last Modified: Tue, 16 Sep 2025 17:59:40 GMT  
		Size: 2.2 MB (2217050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce1e7aff34b8533b0bb5b4a7367e628f7a56899fb064e365241e703107bd1251`  
		Last Modified: Tue, 16 Sep 2025 17:59:41 GMT  
		Size: 24.2 KB (24192 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:slim` - linux; ppc64le

```console
$ docker pull ruby@sha256:85332b1d0572c83c1b937134c28a908e713dbc7f0ea180953d161c043b74765e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.5 MB (74500195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1f1f9273719719e6b3f9ce768a35afd7cfd75aa47e8b08144d3fd88b610d05a`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1757289600'
# Tue, 16 Sep 2025 05:03:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 16 Sep 2025 05:03:19 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 16 Sep 2025 05:03:19 GMT
ENV LANG=C.UTF-8
# Tue, 16 Sep 2025 05:03:19 GMT
ENV RUBY_VERSION=3.4.6
# Tue, 16 Sep 2025 05:03:19 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.6.tar.xz
# Tue, 16 Sep 2025 05:03:19 GMT
ENV RUBY_DOWNLOAD_SHA256=804995bc22938aa475127000d3103cb133409ad3955edfc0e7412be66a4859b8
# Tue, 16 Sep 2025 05:03:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 16 Sep 2025 05:03:19 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 16 Sep 2025 05:03:19 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 16 Sep 2025 05:03:19 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Sep 2025 05:03:19 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 16 Sep 2025 05:03:19 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:d11c44105444ef722eccd8c92c6b2fce9986e3274ba9b346e044a458c0425852`  
		Last Modified: Mon, 08 Sep 2025 22:03:02 GMT  
		Size: 33.6 MB (33594351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ba702f0f51333fc2712ffc50d66684ef842dd2f30e7e612a7085b6264c7d0c0`  
		Last Modified: Tue, 16 Sep 2025 17:27:46 GMT  
		Size: 1.3 MB (1309688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:902b9bcf1c68a9433fa734e7f77d0062d7271f532391ae56abbef8e2820cf828`  
		Last Modified: Tue, 16 Sep 2025 17:27:46 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00eeb6308e90b8bb2e276d4c0017af677089a878c4fc04021ec60abaf88b633b`  
		Last Modified: Tue, 16 Sep 2025 17:27:49 GMT  
		Size: 39.6 MB (39595821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52aa59464570e58df18efecb42c30257cdea420248e5b8999bbed0be72c06831`  
		Last Modified: Tue, 16 Sep 2025 17:27:46 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim` - unknown; unknown

```console
$ docker pull ruby@sha256:e43de7d6a0cf165d8fa4f8c358f3ba111b9e14e2a72e3eb0de2f6778f2823046
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2247753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:877ac1de7141bb26cb689f30bf2fea972d597abeb5b94afb9ffc914d21a4f6a7`

```dockerfile
```

-	Layers:
	-	`sha256:685a2a10d64db836a6a690dfee29c845dd90f96f4183bb5518fed1e4a2978064`  
		Last Modified: Tue, 16 Sep 2025 17:59:45 GMT  
		Size: 2.2 MB (2223430 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d870545a55ca059625964e6b0113fd1d7c2330b73d448aeb059a9ce891802f36`  
		Last Modified: Tue, 16 Sep 2025 17:59:46 GMT  
		Size: 24.3 KB (24323 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:slim` - linux; riscv64

```console
$ docker pull ruby@sha256:984cea9854ffaffdf2fa3def5efd0ecd47e402d07ecb0d384a89911fb5ee79a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.5 MB (67532018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cc05cc32a7759d5aed297accfc979a76b0b191e9b73d1dd4e76f36a60a2b1d8`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1757289600'
# Tue, 16 Sep 2025 05:03:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 16 Sep 2025 05:03:19 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 16 Sep 2025 05:03:19 GMT
ENV LANG=C.UTF-8
# Tue, 16 Sep 2025 05:03:19 GMT
ENV RUBY_VERSION=3.4.6
# Tue, 16 Sep 2025 05:03:19 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.6.tar.xz
# Tue, 16 Sep 2025 05:03:19 GMT
ENV RUBY_DOWNLOAD_SHA256=804995bc22938aa475127000d3103cb133409ad3955edfc0e7412be66a4859b8
# Tue, 16 Sep 2025 05:03:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 16 Sep 2025 05:03:19 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 16 Sep 2025 05:03:19 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 16 Sep 2025 05:03:19 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Sep 2025 05:03:19 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 16 Sep 2025 05:03:19 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:dd4e3fb8766f676c414c0c55be0f5d9f6e6359dc2628caa804016b0f2ba461f2`  
		Last Modified: Tue, 09 Sep 2025 01:07:45 GMT  
		Size: 28.3 MB (28271372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd476495e7b776fe14b60dadece872c3e15e1f1b6725bcc38aeb4b9a2632308e`  
		Last Modified: Sat, 13 Sep 2025 18:42:45 GMT  
		Size: 1.2 MB (1247474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e08b0d8d8cf2476e391ce6c97dcf28e6215c9eb31048f48f2ab384c9932961d7`  
		Last Modified: Sat, 13 Sep 2025 18:42:45 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:676523187cec2033608575a8679e49e5d7bf830fcc29d3823df6a02aff66c294`  
		Last Modified: Wed, 17 Sep 2025 05:51:55 GMT  
		Size: 38.0 MB (38012837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc5c16556c98ee64c9af468f903aaf82c9727ac36aa6584632f10e5e905ffb39`  
		Last Modified: Wed, 17 Sep 2025 05:51:40 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim` - unknown; unknown

```console
$ docker pull ruby@sha256:fd7aeea710814d114b11f05bafc25367a9762ed3143c4fcc421fe389130efb73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2238148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb2e426945eb63b25656235d9a88b1dc75c14587e9d05612c6f71f20129018cd`

```dockerfile
```

-	Layers:
	-	`sha256:ac2df7eb6002a3244d231ee1631b4e869c294503d982e1827a5eb08d5afdfb3f`  
		Last Modified: Wed, 17 Sep 2025 08:57:47 GMT  
		Size: 2.2 MB (2213825 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0ed39c1d76b96fb2a1817ec22890e17bed1ae605ab5dfcf400e3715f4f99814`  
		Last Modified: Wed, 17 Sep 2025 08:57:48 GMT  
		Size: 24.3 KB (24323 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:slim` - linux; s390x

```console
$ docker pull ruby@sha256:662f9515e5c2a4cba63a45b3165ff464fec952373863afd1e684f76c00e33277
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.4 MB (70414517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2b52250f10d584bbd0339640ea1b7bd53eec52f85c529e02f9a5e04b5be8bb3`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1757289600'
# Tue, 16 Sep 2025 05:03:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 16 Sep 2025 05:03:19 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 16 Sep 2025 05:03:19 GMT
ENV LANG=C.UTF-8
# Tue, 16 Sep 2025 05:03:19 GMT
ENV RUBY_VERSION=3.4.6
# Tue, 16 Sep 2025 05:03:19 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.6.tar.xz
# Tue, 16 Sep 2025 05:03:19 GMT
ENV RUBY_DOWNLOAD_SHA256=804995bc22938aa475127000d3103cb133409ad3955edfc0e7412be66a4859b8
# Tue, 16 Sep 2025 05:03:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 16 Sep 2025 05:03:19 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 16 Sep 2025 05:03:19 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 16 Sep 2025 05:03:19 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Sep 2025 05:03:19 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 16 Sep 2025 05:03:19 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:8af003c0cb712f415b555d33f1c4a9cc3fad82782766d388f3426c4d807a5ab2`  
		Last Modified: Mon, 08 Sep 2025 21:53:51 GMT  
		Size: 29.8 MB (29832904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70370253f1ce091fe730c380a58bcad6c984318332f9815450f5cfaa70aa87f5`  
		Last Modified: Tue, 16 Sep 2025 17:17:49 GMT  
		Size: 1.3 MB (1294292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7ec12509a32b107309b0e8ad0dd5f247db0a2ca036489efbfcf07069855b56d`  
		Last Modified: Tue, 16 Sep 2025 17:17:49 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e95e9b1c0885cb28c05fa772e1873d7827da80a057035afb16216bb0e18774ea`  
		Last Modified: Tue, 16 Sep 2025 17:17:57 GMT  
		Size: 39.3 MB (39286986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:160aaf92b9681375fe7aaa71ed89f2fa889c9ed589628572f762bc3bde9e15e7`  
		Last Modified: Tue, 16 Sep 2025 17:17:49 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim` - unknown; unknown

```console
$ docker pull ruby@sha256:e6020b9d06275d34b2390a32b53236b540bbbc061ae0768d3b0048c9907b74db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2245572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f53267e56e9d2f85fa7b4ca68d73542c63ec07276863f334b7fa482e9daf84bb`

```dockerfile
```

-	Layers:
	-	`sha256:aa68874c750b726a83722d8fc1c77659e7c5d18c220574490b2ba2018a2d88ea`  
		Last Modified: Tue, 16 Sep 2025 17:59:53 GMT  
		Size: 2.2 MB (2221322 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67ff5e59bbba33316af0e4dea350d7d94d8faf2c75b715067bf089b85cb9cd46`  
		Last Modified: Tue, 16 Sep 2025 17:59:53 GMT  
		Size: 24.2 KB (24250 bytes)  
		MIME: application/vnd.in-toto+json
