## `ruby:3-slim-bullseye`

```console
$ docker pull ruby@sha256:9a4e66bda4365c0770148bbff7bbbdc9b8728ee00906a05b651cf2e3ea54c4cf
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
$ docker pull ruby@sha256:cab676e2ffa969ecd33e07abbb1bcf7a420be1c859ff4273aad8e0fff809bc75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.4 MB (72428871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4acecf98855521c66e28bb3c7722913bfd9cf845d2b7175dd103f9c2ae84d1c7`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1738540800'
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
	-	`sha256:cf799a8da63a7bb7f377162d10ed737dd26b0e1174c8ac5d89a5da6c15dc7c04`  
		Last Modified: Tue, 04 Feb 2025 04:26:31 GMT  
		Size: 30.3 MB (30252588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7b465ba4d6c63fed26f6a7af69aa1a43636f05aa236937f29d87612a9a783cb`  
		Last Modified: Sat, 15 Feb 2025 04:03:41 GMT  
		Size: 862.6 KB (862578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df912ec5e2008b6a67713ab7c7be8a39971eb9d15babb7c6660aee1b5a460fa9`  
		Last Modified: Sat, 15 Feb 2025 04:03:41 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:671ec90692c49af822f5f458f2c7e5bee03b5f51fcd9b71aca3cb0d84d93b974`  
		Last Modified: Sat, 15 Feb 2025 04:03:43 GMT  
		Size: 41.3 MB (41313373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:825fc63f20e98b5d0e09f2614e56003b2b1bfb11c28fdee7ad33c0ccafd17c3d`  
		Last Modified: Sat, 15 Feb 2025 04:03:40 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-slim-bullseye` - unknown; unknown

```console
$ docker pull ruby@sha256:812b94e6ff53df61b09c8d3220dd43f7ce4c42b58a964f117a9dcf89a70fbc5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2800801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed18ad414e52cdbdd778f3687355348dade19ac954f68a44112c4c86031403b9`

```dockerfile
```

-	Layers:
	-	`sha256:98675da70a04f444a6c183ef65970dca02d78f1a5d0b7d5a0566f111f8d24533`  
		Last Modified: Sat, 15 Feb 2025 03:58:16 GMT  
		Size: 2.8 MB (2778011 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:087dd9c3ee3facce9acbc2f772fecd3f9e623a54bf93a848ac500b6c374beb6c`  
		Last Modified: Sat, 15 Feb 2025 03:58:16 GMT  
		Size: 22.8 KB (22790 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-slim-bullseye` - linux; arm variant v7

```console
$ docker pull ruby@sha256:922a2de3f9a3ec2a533e83139c2f1a952ecfe686de1d9a7ff6588a1caec3e579
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.0 MB (69990116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a777272234009eeb72664d6bf367f699369c07e0b724adc85784827cdc2e39da`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 14 Jan 2025 19:28:22 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1738540800'
# Tue, 14 Jan 2025 19:28:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Jan 2025 19:28:22 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 14 Jan 2025 19:28:22 GMT
ENV LANG=C.UTF-8
# Tue, 14 Jan 2025 19:28:22 GMT
ENV RUBY_VERSION=3.4.1
# Tue, 14 Jan 2025 19:28:22 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.1.tar.xz
# Tue, 14 Jan 2025 19:28:22 GMT
ENV RUBY_DOWNLOAD_SHA256=018d59ffb52be3c0a6d847e22d3fd7a2c52d0ddfee249d3517a0c8c6dbfa70af
# Tue, 14 Jan 2025 19:28:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		savedAptMark="$savedAptMark 		bzip2 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	"; 	apt-get install -y --no-install-recommends $savedAptMark; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 14 Jan 2025 19:28:22 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 14 Jan 2025 19:28:22 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 14 Jan 2025 19:28:22 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Jan 2025 19:28:22 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 14 Jan 2025 19:28:22 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:be8e62ac4d3904082a64376be6dbebabc925200adb880f791173ab7f6800b156`  
		Last Modified: Tue, 04 Feb 2025 08:24:31 GMT  
		Size: 25.5 MB (25533883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aaeef3d863118c130ac8b9b156f985010f81dee8ba7a7dbcd2616611f4028bb`  
		Last Modified: Sat, 15 Feb 2025 12:06:05 GMT  
		Size: 826.3 KB (826300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:707726ebf86dcfd850194d2cd12f9e18aa645c0755faac38fe4ccf14fbc74b05`  
		Last Modified: Wed, 05 Feb 2025 06:11:22 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0ce499412eda4102db93d5fe0cfec340313e4798499ff91d4dbfda57d3441ce`  
		Last Modified: Wed, 05 Feb 2025 11:37:09 GMT  
		Size: 43.6 MB (43629602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8d5be95c121ef2b7dd36bc0ea451e4eb6396fc69b4e1d3460d3f8b6152d4630`  
		Last Modified: Sun, 09 Feb 2025 03:03:58 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-slim-bullseye` - unknown; unknown

```console
$ docker pull ruby@sha256:4d455348c4bd104f676a03f838dafec328cb1f4365deebd87b773bc8a76f8c6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4113663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9038a046ba2de1121f660ae201450df7a39df9aa6d392558a9d6a470444b60bd`

```dockerfile
```

-	Layers:
	-	`sha256:9e1e993820e1c64d5bb443b9b6b75dadbb52048d0f8d4f994a020c5318521c02`  
		Last Modified: Sat, 15 Feb 2025 03:58:18 GMT  
		Size: 4.1 MB (4088628 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3626918b54e48ea0b99e9bc28348cd085c6e44a51b9e8cdcd37087d70795c9b6`  
		Last Modified: Sat, 15 Feb 2025 03:58:19 GMT  
		Size: 25.0 KB (25035 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull ruby@sha256:314b789bd83970e516dc566b7f48cd79fa31e4ec981c4744e4aa8b9b2b913b03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.9 MB (78891064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d09a5e4fe2dcea827cb8241f7714ffff745b7f09f9805441303c861243223522`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 14 Jan 2025 19:28:22 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1738540800'
# Tue, 14 Jan 2025 19:28:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Jan 2025 19:28:22 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 14 Jan 2025 19:28:22 GMT
ENV LANG=C.UTF-8
# Tue, 14 Jan 2025 19:28:22 GMT
ENV RUBY_VERSION=3.4.1
# Tue, 14 Jan 2025 19:28:22 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.1.tar.xz
# Tue, 14 Jan 2025 19:28:22 GMT
ENV RUBY_DOWNLOAD_SHA256=018d59ffb52be3c0a6d847e22d3fd7a2c52d0ddfee249d3517a0c8c6dbfa70af
# Tue, 14 Jan 2025 19:28:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		savedAptMark="$savedAptMark 		bzip2 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	"; 	apt-get install -y --no-install-recommends $savedAptMark; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 14 Jan 2025 19:28:22 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 14 Jan 2025 19:28:22 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 14 Jan 2025 19:28:22 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Jan 2025 19:28:22 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 14 Jan 2025 19:28:22 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:9225a2a808e874449ee822a282882a3c331aad2f5093c1062e16494d8bce3e9a`  
		Last Modified: Tue, 04 Feb 2025 04:27:50 GMT  
		Size: 28.7 MB (28744810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9731c9794180a21319e214a92e522e62bfb1829dc59da0b654b5adac15baa456`  
		Last Modified: Tue, 04 Feb 2025 20:09:15 GMT  
		Size: 849.8 KB (849764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:076cd9ef2c775d51ab99d3e83622aba0e05cd781cb9df5118a530b42875e7a1a`  
		Last Modified: Tue, 04 Feb 2025 20:13:33 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4f605051af1545f4ff68505dcb51121779662cf5f0959dcc204bc52eb92caa3`  
		Last Modified: Wed, 05 Feb 2025 00:39:37 GMT  
		Size: 49.3 MB (49296160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5cf1657b4ebc09ab6a7c70ce6ec4bbc682fb9a88882f784ad478b6c18d68571`  
		Last Modified: Tue, 04 Feb 2025 16:02:11 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-slim-bullseye` - unknown; unknown

```console
$ docker pull ruby@sha256:c5c839f72aa722620fccb4b92a9450b192ba050e780777330d48f0251b72e9b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4114085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30d40a71325215039202cf311a00712e6be2bfa37c137fcc14cafe96bc9095d2`

```dockerfile
```

-	Layers:
	-	`sha256:baa8917adce0464e41d1191649907248ddf4240a6b753e840357d20e194512b6`  
		Last Modified: Sat, 15 Feb 2025 03:58:21 GMT  
		Size: 4.1 MB (4089016 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd989b846042d2b4b998a524d8a23df1091f5b7b01523b66f9e05becf8ae4af2`  
		Last Modified: Sat, 15 Feb 2025 03:58:21 GMT  
		Size: 25.1 KB (25069 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-slim-bullseye` - linux; 386

```console
$ docker pull ruby@sha256:742f6a43452d8f1872dc339753b33c2eaf22cdbbf342d41697526f9f185aa2e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.7 MB (68739000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faec861a7e2a956b2ade3906530febcefc1c266a0d5d285da971b94e3e67d031`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1738540800'
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
	-	`sha256:af24a588b358e10d8284ac042756542ed964075987788d3d4a5fdbb6809e4de5`  
		Last Modified: Tue, 04 Feb 2025 05:05:20 GMT  
		Size: 31.2 MB (31178875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a6b959cbd039df4c3fe9c012420e9f0e78678cdcee1c3963a08cb6c93b518de`  
		Last Modified: Sat, 15 Feb 2025 02:33:11 GMT  
		Size: 874.7 KB (874717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74705cad82e98dd9a154898198775d3478250e349526efe5f0ce268f0c7e4d91`  
		Last Modified: Sat, 15 Feb 2025 02:33:11 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b022dacfd87c4b77a2ca27c37339a1a7cad411347780ad10b8588da8437d1258`  
		Last Modified: Sat, 15 Feb 2025 02:33:12 GMT  
		Size: 36.7 MB (36685076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bf7656eb835626236d80918f71664bfa81ee226e9698968dc12e65a98121acb`  
		Last Modified: Sat, 15 Feb 2025 03:09:33 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-slim-bullseye` - unknown; unknown

```console
$ docker pull ruby@sha256:ae8c5c52e43de0db6e673520c2f9810edec6dd69ef41144678ae08810f262160
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2797893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4370bbf1746deaff8b9faa18908fa3f92089c3bdf4ed43405d022ea802d81b83`

```dockerfile
```

-	Layers:
	-	`sha256:04a3e7e8cac3c4a98b6808f2396cb6eba5867f290bb792d1a9d0cb74ccd7a386`  
		Last Modified: Sat, 15 Feb 2025 03:58:24 GMT  
		Size: 2.8 MB (2775140 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4c92b8b67bdb5bc679aae50e77a08e705414c8ae9a7de1203a3d9037d5a212d`  
		Last Modified: Sat, 15 Feb 2025 03:58:24 GMT  
		Size: 22.8 KB (22753 bytes)  
		MIME: application/vnd.in-toto+json
