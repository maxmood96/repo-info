## `ruby:slim`

```console
$ docker pull ruby@sha256:98e208daf93d40485edf2f5e1a1527202ae0824cdc1619b6659674a84aa197ba
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

### `ruby:slim` - linux; amd64

```console
$ docker pull ruby@sha256:481caa4760a7df5782f2b64462de7a4cd882f5bdd780c6a45d8bcc7491be1c1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.1 MB (73057622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4078585d90851aa01bc3b93084c51926654b87fc67b060916eddb7a0f283d450`
-	Default Command: `["irb"]`

```dockerfile
# Sat, 15 Feb 2025 00:00:36 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
# Sat, 15 Feb 2025 00:00:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 15 Feb 2025 00:00:36 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Sat, 15 Feb 2025 00:00:36 GMT
ENV LANG=C.UTF-8
# Sat, 15 Feb 2025 00:00:36 GMT
ENV RUBY_VERSION=3.4.2
# Sat, 15 Feb 2025 00:00:36 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.2.tar.xz
# Sat, 15 Feb 2025 00:00:36 GMT
ENV RUBY_DOWNLOAD_SHA256=ebf1c2eb58f5da17c23e965d658dd7e6202c5c50f5179154c5574452bef4b3e0
# Sat, 15 Feb 2025 00:00:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Sat, 15 Feb 2025 00:00:36 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 15 Feb 2025 00:00:36 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 15 Feb 2025 00:00:36 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 15 Feb 2025 00:00:36 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Sat, 15 Feb 2025 00:00:36 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:6e909acdb790c5a1989d9cfc795fda5a246ad6664bb27b5c688e2b734b2c5fad`  
		Last Modified: Mon, 17 Mar 2025 22:17:24 GMT  
		Size: 28.2 MB (28204865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d641b0f84d4c573b933ccf4fe08790a510437cc7f6ef2254007088005659598`  
		Last Modified: Mon, 17 Mar 2025 23:19:36 GMT  
		Size: 3.5 MB (3499355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e62b3be2dd4b538e65e7143f6cab945a34ced69c33ec92638fe685d1c49e3545`  
		Last Modified: Mon, 17 Mar 2025 23:19:36 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98a5e9a05e2d731a8aebdd191a0021cb553be3b6d44afeb384ff3fade4af6394`  
		Last Modified: Mon, 17 Mar 2025 23:19:37 GMT  
		Size: 41.4 MB (41353069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce40c1a84fcfa921dfa3a984eb037ce9704dfe98c531804e3d463438f66ec12e`  
		Last Modified: Mon, 17 Mar 2025 23:19:36 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim` - unknown; unknown

```console
$ docker pull ruby@sha256:9e421d5348fdababc898a9e00157728bf1efa9f1ef1d6d41f29e2c5928a5a676
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2507883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d892e988c5d10419bcd4e2f544634b3bedf5dbfd31933ff9fbab22abb2f09b8b`

```dockerfile
```

-	Layers:
	-	`sha256:be303802b26631768c218be4bd8b0385ab3043643d1fd8e2548603de109451fb`  
		Last Modified: Mon, 17 Mar 2025 23:19:36 GMT  
		Size: 2.5 MB (2483904 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10477ea706ed9d945897a7c66fdbade28051bf14ee03a9e72d5c1994f7a05acb`  
		Last Modified: Mon, 17 Mar 2025 23:19:35 GMT  
		Size: 24.0 KB (23979 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:slim` - linux; arm variant v5

```console
$ docker pull ruby@sha256:84e3b971f964d75ed972decd9c17fefdc1bdffd4b2d379cd93f3271f2f666f8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.9 MB (65921731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78e682a3ca9a6b761323eb86dc6d800d87820512da855a5830bf59c6dbb46aa6`
-	Default Command: `["irb"]`

```dockerfile
# Sat, 15 Feb 2025 00:00:36 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1742169600'
# Sat, 15 Feb 2025 00:00:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 15 Feb 2025 00:00:36 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Sat, 15 Feb 2025 00:00:36 GMT
ENV LANG=C.UTF-8
# Sat, 15 Feb 2025 00:00:36 GMT
ENV RUBY_VERSION=3.4.2
# Sat, 15 Feb 2025 00:00:36 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.2.tar.xz
# Sat, 15 Feb 2025 00:00:36 GMT
ENV RUBY_DOWNLOAD_SHA256=ebf1c2eb58f5da17c23e965d658dd7e6202c5c50f5179154c5574452bef4b3e0
# Sat, 15 Feb 2025 00:00:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Sat, 15 Feb 2025 00:00:36 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 15 Feb 2025 00:00:36 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 15 Feb 2025 00:00:36 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 15 Feb 2025 00:00:36 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Sat, 15 Feb 2025 00:00:36 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:87c352465466fcf04c9686fee29c2541af5fc39172801545bb24d9faa8cdeabb`  
		Last Modified: Mon, 17 Mar 2025 22:17:36 GMT  
		Size: 25.7 MB (25735853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a06bf00a22e98835898fabeb6f4b4e688d5e3dd40a63cf933c7a8f01f50907`  
		Last Modified: Mon, 17 Mar 2025 23:15:23 GMT  
		Size: 3.1 MB (3073487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47491093163753c8af27297703757839575e4b6c77291db467bfb40c61a24740`  
		Last Modified: Mon, 17 Mar 2025 23:15:22 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b894fcb5241969e7564ecbc4545764d803047ae22f68da639dc0fc1889dc6e0`  
		Last Modified: Tue, 18 Mar 2025 01:29:03 GMT  
		Size: 37.1 MB (37112058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3ce593f40684b114637f16f46445e9f4e8ae01cfe14f5db25a800cbf1c5cbaf`  
		Last Modified: Tue, 18 Mar 2025 01:29:01 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim` - unknown; unknown

```console
$ docker pull ruby@sha256:9f33ae2beac283f078b07c1477041e6a1fe892ac619cadda5295ac2b00a4bd3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2511559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1fc97c597d8fcb1555b0098f837615e587836e361a1e05c5649d54905601374`

```dockerfile
```

-	Layers:
	-	`sha256:85f58460df12e330e46e6971d968fcff0925a202ed95a48ab44200b7c5e5f0f4`  
		Last Modified: Tue, 18 Mar 2025 01:29:01 GMT  
		Size: 2.5 MB (2487433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf7c9ae2ae74dfefdd755494fa4abd4d98a28a347031bbf0dabcbe1ac02ca6e8`  
		Last Modified: Tue, 18 Mar 2025 01:29:01 GMT  
		Size: 24.1 KB (24126 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:slim` - linux; arm variant v7

```console
$ docker pull ruby@sha256:7c8e955cd33e121a88bc35313de240bdd0ba490faa2a146bda1ccb058a605bd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.8 MB (63760864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cbe1e6981a577ef6182b6b2211895fc5e03340ce27169a41ab37b3fe331a2a6`
-	Default Command: `["irb"]`

```dockerfile
# Sat, 15 Feb 2025 00:00:36 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1742169600'
# Sat, 15 Feb 2025 00:00:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 15 Feb 2025 00:00:36 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Sat, 15 Feb 2025 00:00:36 GMT
ENV LANG=C.UTF-8
# Sat, 15 Feb 2025 00:00:36 GMT
ENV RUBY_VERSION=3.4.2
# Sat, 15 Feb 2025 00:00:36 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.2.tar.xz
# Sat, 15 Feb 2025 00:00:36 GMT
ENV RUBY_DOWNLOAD_SHA256=ebf1c2eb58f5da17c23e965d658dd7e6202c5c50f5179154c5574452bef4b3e0
# Sat, 15 Feb 2025 00:00:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Sat, 15 Feb 2025 00:00:36 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 15 Feb 2025 00:00:36 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 15 Feb 2025 00:00:36 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 15 Feb 2025 00:00:36 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Sat, 15 Feb 2025 00:00:36 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:676cf117f557880ff2e894692781cbce1b2a04502aff2e34b58c230b14731b8f`  
		Last Modified: Mon, 17 Mar 2025 22:18:43 GMT  
		Size: 23.9 MB (23915088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90de84afec6d4f313e7bf277c66cdcd6136876e4c4965613cc67e1980d1444fb`  
		Last Modified: Mon, 17 Mar 2025 23:43:15 GMT  
		Size: 2.9 MB (2907809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a73b798bb0e7139852833719de73453b77fd4d1365a02d6a7edbe7a1316b7dad`  
		Last Modified: Mon, 17 Mar 2025 23:43:15 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:024e00a021d6106a1678a30e886a8bed4ad1adea1d1370f7a0dd8a9370319fcb`  
		Last Modified: Tue, 18 Mar 2025 00:13:03 GMT  
		Size: 36.9 MB (36937635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d19a47a79f46c29b9d9a3c7f555107f4088e601dad2840fa0dab63fdb0e26cd`  
		Last Modified: Tue, 18 Mar 2025 00:13:02 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim` - unknown; unknown

```console
$ docker pull ruby@sha256:c717ea9ae9d6eca07e12a2e4b14adf8cb72922391425d88a462e5191bf3774ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2510286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14ccef9571862ab405d017e368ea1088393863d01240957a23ea85b10a86e80d`

```dockerfile
```

-	Layers:
	-	`sha256:d705c546ebd01764aba0b3da949d9bb04337c2d1b52b22a2d0b38df2817d0419`  
		Last Modified: Tue, 18 Mar 2025 00:13:02 GMT  
		Size: 2.5 MB (2486160 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:158d5c6cb94d1a52b641f894482943bf2ca868b539092ee1286cb068eaf4537a`  
		Last Modified: Tue, 18 Mar 2025 00:13:02 GMT  
		Size: 24.1 KB (24126 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:slim` - linux; arm64 variant v8

```console
$ docker pull ruby@sha256:ac0c82d5d5acf7eace78a4410465f8cfef2531790a5c8307c7b88f7195fe60b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.6 MB (72612051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f3296329801b4e03bc4c1f0d3126c0cc108a3b1e50edd8f9a2c52072a75e679`
-	Default Command: `["irb"]`

```dockerfile
# Sat, 15 Feb 2025 00:00:36 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
# Sat, 15 Feb 2025 00:00:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 15 Feb 2025 00:00:36 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Sat, 15 Feb 2025 00:00:36 GMT
ENV LANG=C.UTF-8
# Sat, 15 Feb 2025 00:00:36 GMT
ENV RUBY_VERSION=3.4.2
# Sat, 15 Feb 2025 00:00:36 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.2.tar.xz
# Sat, 15 Feb 2025 00:00:36 GMT
ENV RUBY_DOWNLOAD_SHA256=ebf1c2eb58f5da17c23e965d658dd7e6202c5c50f5179154c5574452bef4b3e0
# Sat, 15 Feb 2025 00:00:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Sat, 15 Feb 2025 00:00:36 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 15 Feb 2025 00:00:36 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 15 Feb 2025 00:00:36 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 15 Feb 2025 00:00:36 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Sat, 15 Feb 2025 00:00:36 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:d9b6365477446a79987b20560ae52637be6f54d6d2f801e16aaa0ca25dd0964b`  
		Last Modified: Mon, 17 Mar 2025 22:17:34 GMT  
		Size: 28.0 MB (28044037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3f1f5b37bd6494f4c979734eddbf38ec3c9d650a090b347a2d957a8954d0749`  
		Last Modified: Tue, 18 Mar 2025 00:23:40 GMT  
		Size: 3.3 MB (3322905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb042444c12b759079305dd1cac7c315803bfb9f000bdc2b4e985de08a8419d1`  
		Last Modified: Tue, 18 Mar 2025 00:23:40 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca25bd205cdde8dff7cd43e4c8b21aef6acf0443738c2dd74a12a436be2a3a28`  
		Last Modified: Tue, 18 Mar 2025 00:33:19 GMT  
		Size: 41.2 MB (41244776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef392ccca3800d9543390d5b8c4848b3d4d2506206ca5213970cf3336e93e0dc`  
		Last Modified: Tue, 18 Mar 2025 00:33:18 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim` - unknown; unknown

```console
$ docker pull ruby@sha256:b585ef964f6ff6db91876016bb2dbd7a34bf29d3da51ee544e70e4cfa269c2e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2508386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:351416726ac174599fba6632853d0293ebe517ab92630ae0ab23cd39e15507a5`

```dockerfile
```

-	Layers:
	-	`sha256:1a7af144e06ef40157445337cafaf94893625d977cbd62a2494c5f775ac18a3a`  
		Last Modified: Tue, 18 Mar 2025 00:33:18 GMT  
		Size: 2.5 MB (2484210 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3bbf08db4efc52408fdfab8c95ac20d5a1580dd8bf30187383aa78e45ef676d`  
		Last Modified: Tue, 18 Mar 2025 00:33:18 GMT  
		Size: 24.2 KB (24176 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:slim` - linux; 386

```console
$ docker pull ruby@sha256:2000616ef19f124f1c75c9e5fd0dfb8d2332bf3d2115fa5d2083f37a07fe38bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.6 MB (69634319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e1f9e46f77fa0b429d0bee658b4fc398113944322d9004c51314249e8e1f3ef`
-	Default Command: `["irb"]`

```dockerfile
# Sat, 15 Feb 2025 00:00:36 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1742169600'
# Sat, 15 Feb 2025 00:00:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 15 Feb 2025 00:00:36 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Sat, 15 Feb 2025 00:00:36 GMT
ENV LANG=C.UTF-8
# Sat, 15 Feb 2025 00:00:36 GMT
ENV RUBY_VERSION=3.4.2
# Sat, 15 Feb 2025 00:00:36 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.2.tar.xz
# Sat, 15 Feb 2025 00:00:36 GMT
ENV RUBY_DOWNLOAD_SHA256=ebf1c2eb58f5da17c23e965d658dd7e6202c5c50f5179154c5574452bef4b3e0
# Sat, 15 Feb 2025 00:00:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Sat, 15 Feb 2025 00:00:36 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 15 Feb 2025 00:00:36 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 15 Feb 2025 00:00:36 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 15 Feb 2025 00:00:36 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Sat, 15 Feb 2025 00:00:36 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:bdeb081d427d7feac6a8c0bd36a2c34506a1aa38143fe43a5c5a8c162698a854`  
		Last Modified: Mon, 17 Mar 2025 22:17:35 GMT  
		Size: 29.2 MB (29189528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b02f2ef2685aff2221b803c04d2c600c6de347f70f9458127bab038e8172b0`  
		Last Modified: Mon, 17 Mar 2025 23:32:56 GMT  
		Size: 3.5 MB (3503417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f12f7a25b5baf09c983140de7d504278859ccc8a017e346409b41b299fd5aac`  
		Last Modified: Mon, 17 Mar 2025 23:32:55 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4719d6a5bebc36c2d058b6b6e774da00b8379cee6dd27064e583e620549fae7b`  
		Last Modified: Mon, 17 Mar 2025 23:32:57 GMT  
		Size: 36.9 MB (36941042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403b887dcb9cd5f1c198bea6d248208d1d5fa25f647d7870fc763b9978759537`  
		Last Modified: Mon, 17 Mar 2025 23:32:55 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim` - unknown; unknown

```console
$ docker pull ruby@sha256:bbc8f3a620bc65efd19f3c5019cf26870414b371808d4543622140eac1e8e70b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2504945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09b2d2fa537f45951def063f863df93e7ea812d5ff471cf8ced5342522a93545`

```dockerfile
```

-	Layers:
	-	`sha256:63daa540b806c398952a958d57e7026f4e2533fdce1d6421b0f445c3e65ff40e`  
		Last Modified: Mon, 17 Mar 2025 23:32:56 GMT  
		Size: 2.5 MB (2481024 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1cf6a45978157f730999fc7a9fc289bb1b6082134512d258b296144ace2c4e25`  
		Last Modified: Mon, 17 Mar 2025 23:32:55 GMT  
		Size: 23.9 KB (23921 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:slim` - linux; mips64le

```console
$ docker pull ruby@sha256:193fa44e55f6fd24079bbb8d29db8fa0442e3c47a8a411d028568eb301e44243
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.7 MB (69723791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02c1f4ffc5168b22490fc8a1d1fd05becd5126b0497b01c33e00d2a38a49a822`
-	Default Command: `["irb"]`

```dockerfile
# Sat, 15 Feb 2025 00:00:36 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1742169600'
# Sat, 15 Feb 2025 00:00:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 15 Feb 2025 00:00:36 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Sat, 15 Feb 2025 00:00:36 GMT
ENV LANG=C.UTF-8
# Sat, 15 Feb 2025 00:00:36 GMT
ENV RUBY_VERSION=3.4.2
# Sat, 15 Feb 2025 00:00:36 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.2.tar.xz
# Sat, 15 Feb 2025 00:00:36 GMT
ENV RUBY_DOWNLOAD_SHA256=ebf1c2eb58f5da17c23e965d658dd7e6202c5c50f5179154c5574452bef4b3e0
# Sat, 15 Feb 2025 00:00:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Sat, 15 Feb 2025 00:00:36 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 15 Feb 2025 00:00:36 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 15 Feb 2025 00:00:36 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 15 Feb 2025 00:00:36 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Sat, 15 Feb 2025 00:00:36 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:18c44d6735d044d9bace3fdbe647c9b8187637683376f05d85dcb1185876721f`  
		Last Modified: Mon, 17 Mar 2025 22:19:04 GMT  
		Size: 28.5 MB (28489456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b514658a4f48245596c09f7112cb0f6884c0b1fa96bda139a946ab70038e2fe0`  
		Last Modified: Mon, 17 Mar 2025 23:20:58 GMT  
		Size: 2.9 MB (2895399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4293bb3eaab8701eb6621595b0af4ed6d4d4003d08faf4c3a6c80ba4d816d1ab`  
		Last Modified: Tue, 18 Mar 2025 00:21:23 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52fc3942df7e1f5c90331a975935262ea5cc08bd733542696811feb2bda5caf0`  
		Last Modified: Tue, 18 Mar 2025 02:04:56 GMT  
		Size: 38.3 MB (38338605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66d321bc8cc9d4780ff9d3fe1ac5c9287a7a2081e74822fc07c6c74308289b74`  
		Last Modified: Tue, 18 Mar 2025 02:04:53 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim` - unknown; unknown

```console
$ docker pull ruby@sha256:d670b3940e64cb0caf6a60f93484359589bc72aac98653aa613e42309a3ff775
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 KB (23875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dc31994ea84e318002c4eb9e98d6f168dda81da094ede8e3b9660797db14049`

```dockerfile
```

-	Layers:
	-	`sha256:5aeac523c594b3eb18f002169d21172fe7823e7c12ea86550200818997fb6323`  
		Last Modified: Tue, 18 Mar 2025 02:04:52 GMT  
		Size: 23.9 KB (23875 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:slim` - linux; ppc64le

```console
$ docker pull ruby@sha256:280a96e0712b1257a5dee007b74f1086c417ac923fb3e567ebc479883436ab01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.5 MB (74545090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:526db629ba585619bf4a8d6b62d66e108855a7ff5acadb8e60f02a1e45082354`
-	Default Command: `["irb"]`

```dockerfile
# Sat, 15 Feb 2025 00:00:36 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1742169600'
# Sat, 15 Feb 2025 00:00:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 15 Feb 2025 00:00:36 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Sat, 15 Feb 2025 00:00:36 GMT
ENV LANG=C.UTF-8
# Sat, 15 Feb 2025 00:00:36 GMT
ENV RUBY_VERSION=3.4.2
# Sat, 15 Feb 2025 00:00:36 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.2.tar.xz
# Sat, 15 Feb 2025 00:00:36 GMT
ENV RUBY_DOWNLOAD_SHA256=ebf1c2eb58f5da17c23e965d658dd7e6202c5c50f5179154c5574452bef4b3e0
# Sat, 15 Feb 2025 00:00:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Sat, 15 Feb 2025 00:00:36 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 15 Feb 2025 00:00:36 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 15 Feb 2025 00:00:36 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 15 Feb 2025 00:00:36 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Sat, 15 Feb 2025 00:00:36 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:89104bade2bef9a11eda15952361b42943ba7a21a6bc452862cf92faeccc17cf`  
		Last Modified: Mon, 17 Mar 2025 22:20:32 GMT  
		Size: 32.0 MB (32047814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:297f17f6db06f7ccb8ce850d74e9476f76be07c3d767a47f85269129c1aa3413`  
		Last Modified: Tue, 18 Mar 2025 00:05:31 GMT  
		Size: 3.7 MB (3703023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02aecf7064d6a6758c0cf99fa625261158248215154a7aa546eb441f19911a81`  
		Last Modified: Tue, 18 Mar 2025 00:05:31 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d84e4541c8af9ba631fad48a772690b974fa90fc29ea83640d251d30b80b735a`  
		Last Modified: Tue, 18 Mar 2025 00:29:21 GMT  
		Size: 38.8 MB (38793920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32fae6013fa47c2d3a9597a1a4c5c7abdd88c9542f3d658196965cb3ef2061b0`  
		Last Modified: Tue, 18 Mar 2025 00:29:20 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim` - unknown; unknown

```console
$ docker pull ruby@sha256:bab324341a796f92fac7b1c0c86d0cb1c2683b73f788452c727e629040d5ce67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2512278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:804fba8d9e9ea2ff3c131a7ac4fd9c06a485be2e03805c953be744965c3e24fd`

```dockerfile
```

-	Layers:
	-	`sha256:6d09dfe0e1f96990034ab6459e3a15b8b7601afe6fa01343953611c23a5e0e08`  
		Last Modified: Tue, 18 Mar 2025 00:29:20 GMT  
		Size: 2.5 MB (2488225 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36b3f390c8d12f3ce6eda97d59981f618d30e5745922a95241b73755706b25a0`  
		Last Modified: Tue, 18 Mar 2025 00:29:20 GMT  
		Size: 24.1 KB (24053 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:slim` - linux; s390x

```console
$ docker pull ruby@sha256:94deb1763ee1a24f66e42bc7a2ed2825ba3ab9f9034cff76b92f0bfb31e2df32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.0 MB (67999490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb1d88200ce2a05d5cd18241d366faea744d4b0e5ab4b866aeddea7b74b1889c`
-	Default Command: `["irb"]`

```dockerfile
# Sat, 15 Feb 2025 00:00:36 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1742169600'
# Sat, 15 Feb 2025 00:00:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 15 Feb 2025 00:00:36 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Sat, 15 Feb 2025 00:00:36 GMT
ENV LANG=C.UTF-8
# Sat, 15 Feb 2025 00:00:36 GMT
ENV RUBY_VERSION=3.4.2
# Sat, 15 Feb 2025 00:00:36 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.2.tar.xz
# Sat, 15 Feb 2025 00:00:36 GMT
ENV RUBY_DOWNLOAD_SHA256=ebf1c2eb58f5da17c23e965d658dd7e6202c5c50f5179154c5574452bef4b3e0
# Sat, 15 Feb 2025 00:00:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Sat, 15 Feb 2025 00:00:36 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 15 Feb 2025 00:00:36 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 15 Feb 2025 00:00:36 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 15 Feb 2025 00:00:36 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Sat, 15 Feb 2025 00:00:36 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:c25b115468ab81aaa9017d4d794bc086cba904c84f73abda1eac28615cd44629`  
		Last Modified: Mon, 17 Mar 2025 22:27:10 GMT  
		Size: 26.9 MB (26861059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2ac3c278183a5f89567d212db7d1cf86cdf072aa72fbb0786fd4105c665de4a`  
		Last Modified: Mon, 17 Mar 2025 23:18:50 GMT  
		Size: 3.2 MB (3163408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c52827efbb6609678e743c0ee70daa5571a004537ecf1d6bae4388fc6572767`  
		Last Modified: Mon, 17 Mar 2025 23:18:49 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:601d797c46a7e9dfd2223b2d0104e2e797dbd5d5d87561f5d2fce3d8e7c4ef9b`  
		Last Modified: Mon, 17 Mar 2025 23:18:50 GMT  
		Size: 38.0 MB (37974691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9cc91bbeb18a46acfaa2ca410ca53c09291de4fc078d9f0a9b5419d261eee6c`  
		Last Modified: Mon, 17 Mar 2025 23:18:50 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim` - unknown; unknown

```console
$ docker pull ruby@sha256:fdfefb288b5a5ca0a95d075518207cfc735c49c7229f0ec6c33e47b23fd41c92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2507605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8aa672700439d8922463738049e4eaa5fff85249dc5a067358cbee29bd71d4b`

```dockerfile
```

-	Layers:
	-	`sha256:42ed65e1f038e3571269a403491f93574474af00a50285649769f483afb94ba9`  
		Last Modified: Mon, 17 Mar 2025 23:18:50 GMT  
		Size: 2.5 MB (2483627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:910506704fdcdb0059796910e66793e952f2a1c0c9584b8d3b339fc9101ea803`  
		Last Modified: Mon, 17 Mar 2025 23:18:49 GMT  
		Size: 24.0 KB (23978 bytes)  
		MIME: application/vnd.in-toto+json
