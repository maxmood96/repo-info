## `ruby:slim`

```console
$ docker pull ruby@sha256:bf1ae63808063b7c3ba614d7e2e290011812ebffb7fd773f5ac4081d0c88538a
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
$ docker pull ruby@sha256:938541bb347b35de713748fd608d3ef1430654833c96073e84a0c7ff2a1cba32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.1 MB (73081633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9958d5ade8ad46698818f74cda1f92aa721b543621a6ffaf39be05955c75869e`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 14 Apr 2025 17:03:18 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
# Mon, 14 Apr 2025 17:03:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 17:03:18 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Mon, 14 Apr 2025 17:03:18 GMT
ENV LANG=C.UTF-8
# Mon, 14 Apr 2025 17:03:18 GMT
ENV RUBY_VERSION=3.4.3
# Mon, 14 Apr 2025 17:03:18 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.3.tar.xz
# Mon, 14 Apr 2025 17:03:18 GMT
ENV RUBY_DOWNLOAD_SHA256=174dcd8c516694f833fd3c93ea227fa6c3321464577a3882a6fc7e4fe20237fd
# Mon, 14 Apr 2025 17:03:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Mon, 14 Apr 2025 17:03:18 GMT
ENV GEM_HOME=/usr/local/bundle
# Mon, 14 Apr 2025 17:03:18 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Mon, 14 Apr 2025 17:03:18 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Apr 2025 17:03:18 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Mon, 14 Apr 2025 17:03:18 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:254e724d77862dc53abbd3bf0e27f9d2f64293909cdd3d0aad6a8fe5a6680659`  
		Last Modified: Thu, 08 May 2025 17:04:38 GMT  
		Size: 28.2 MB (28227642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:500fab38b4fc9c5ad310cbe7cf60eaa8acd5059d067f48359c56bdb041215038`  
		Last Modified: Thu, 08 May 2025 17:04:50 GMT  
		Size: 3.5 MB (3499309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:956798033913b36e678f776731db94a64d1425011adef2eb2724361f4e3c2121`  
		Last Modified: Thu, 08 May 2025 17:04:48 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2fb3569a8b30e748c967d82769e74753f0784dcd7a8e232e64b1ad8b01df1a3`  
		Last Modified: Thu, 08 May 2025 17:04:55 GMT  
		Size: 41.4 MB (41354352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0fbf0c81f0cc84f490b75a243af01d371970efed13c68245152cb9c1f8d07a2`  
		Last Modified: Thu, 08 May 2025 17:04:48 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim` - unknown; unknown

```console
$ docker pull ruby@sha256:7ed518ce8195266e33acaa1f5589ec29f79a04b849dbf28431d4dd843e13b773
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2509219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d18ce629a63c23975f7508e834f8e1a47ca9d0f022a7ad470047c51cab61007`

```dockerfile
```

-	Layers:
	-	`sha256:364ede6f48fea97ac56883bac12308c8a14cfaaab63c7eeb5bfcb4acc0f74de3`  
		Last Modified: Mon, 28 Apr 2025 22:07:28 GMT  
		Size: 2.5 MB (2485240 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ac93d09f0ea85c393b746961d5ee3043d06adb3f08fc0687a2911aee437553a`  
		Last Modified: Mon, 28 Apr 2025 22:07:28 GMT  
		Size: 24.0 KB (23979 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:slim` - linux; arm variant v5

```console
$ docker pull ruby@sha256:c65a093ceea98634484053f8ab2f474f163792ab0fb3c77c06b230239ddfb6a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.0 MB (65954855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b04012bb1e502b9b1a08771157d7451f4e126aa62fb577bf45fb9beaa351ad7c`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 14 Apr 2025 17:03:18 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1745798400'
# Mon, 14 Apr 2025 17:03:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 17:03:18 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Mon, 14 Apr 2025 17:03:18 GMT
ENV LANG=C.UTF-8
# Mon, 14 Apr 2025 17:03:18 GMT
ENV RUBY_VERSION=3.4.3
# Mon, 14 Apr 2025 17:03:18 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.3.tar.xz
# Mon, 14 Apr 2025 17:03:18 GMT
ENV RUBY_DOWNLOAD_SHA256=174dcd8c516694f833fd3c93ea227fa6c3321464577a3882a6fc7e4fe20237fd
# Mon, 14 Apr 2025 17:03:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Mon, 14 Apr 2025 17:03:18 GMT
ENV GEM_HOME=/usr/local/bundle
# Mon, 14 Apr 2025 17:03:18 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Mon, 14 Apr 2025 17:03:18 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Apr 2025 17:03:18 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Mon, 14 Apr 2025 17:03:18 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:3bc532ff9d2a2a12c6cfc746359843257a240960865aea7ecb10c71e0b93ec78`  
		Last Modified: Thu, 08 May 2025 17:08:44 GMT  
		Size: 25.8 MB (25757836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a074837e7b03898d01313fb13c34e6984d063e49f1b87381dc0d6e3f132de8cb`  
		Last Modified: Mon, 28 Apr 2025 21:44:55 GMT  
		Size: 3.1 MB (3073452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bbd69a214f3fd84bb19fb5c4a901edfec4f4cf9ff4d65bd287d255155c063aa`  
		Last Modified: Fri, 09 May 2025 01:19:27 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39fd6de015fe67e8c279bed4f88c2dcfa29c16014e612fb033f4973ddd58e948`  
		Last Modified: Tue, 29 Apr 2025 03:15:35 GMT  
		Size: 37.1 MB (37123235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54ac0438fa7553e4c1580f1b3ee9a2e36b14f01f213d3c7b614fa6bf756a5e46`  
		Last Modified: Tue, 29 Apr 2025 03:15:33 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim` - unknown; unknown

```console
$ docker pull ruby@sha256:ae7463733c90a0e040a3bc99ab287b995fb1a21bb8e1c540396b2b0a84fe714a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2512895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c1e86a056ba0e346e7fe8d22aa749bec00389a23728c06b5cb6d7d7b21ad7cb`

```dockerfile
```

-	Layers:
	-	`sha256:9a907da001ed03958ab3134b33388ce7e6b669a280ea92b5f28550abcf57b236`  
		Last Modified: Tue, 29 Apr 2025 03:15:34 GMT  
		Size: 2.5 MB (2488769 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ab78def982392c62f4ceb15af0f87a0458a1c9f593d4532126439e2e8cbbe74`  
		Last Modified: Tue, 29 Apr 2025 03:15:33 GMT  
		Size: 24.1 KB (24126 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:slim` - linux; arm variant v7

```console
$ docker pull ruby@sha256:57b1c3618cef0acfaf45df5a6463d86a76b96359d265389558b21cf314eb5fd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.8 MB (63798320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb2c6a687bcbe1259cd55cd0705760e0d0d13729eb90578a7465d8d40950ed3d`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 14 Apr 2025 17:03:18 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1745798400'
# Mon, 14 Apr 2025 17:03:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 17:03:18 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Mon, 14 Apr 2025 17:03:18 GMT
ENV LANG=C.UTF-8
# Mon, 14 Apr 2025 17:03:18 GMT
ENV RUBY_VERSION=3.4.3
# Mon, 14 Apr 2025 17:03:18 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.3.tar.xz
# Mon, 14 Apr 2025 17:03:18 GMT
ENV RUBY_DOWNLOAD_SHA256=174dcd8c516694f833fd3c93ea227fa6c3321464577a3882a6fc7e4fe20237fd
# Mon, 14 Apr 2025 17:03:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Mon, 14 Apr 2025 17:03:18 GMT
ENV GEM_HOME=/usr/local/bundle
# Mon, 14 Apr 2025 17:03:18 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Mon, 14 Apr 2025 17:03:18 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Apr 2025 17:03:18 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Mon, 14 Apr 2025 17:03:18 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:a3677b10b3c2b17c251b045a96a5c5899810ee1ee2fa8982715ba998fd10e6ad`  
		Last Modified: Thu, 08 May 2025 17:05:07 GMT  
		Size: 23.9 MB (23938074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3ca064f7c0632bec8acecd8b2fe7cfec7ddc1f6739cc172bad82631759a0712`  
		Last Modified: Mon, 28 Apr 2025 21:47:05 GMT  
		Size: 2.9 MB (2907778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc1fffc0adfa58cdc3d151691d776cbcb61baada317e35196a3f17ebbf2a3bcb`  
		Last Modified: Fri, 09 May 2025 01:19:27 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b1f53c0c6c94e5caa1165e6eed2b05a48f205f08ccaaf61b1dd363cabb7a23a`  
		Last Modified: Fri, 09 May 2025 05:44:19 GMT  
		Size: 37.0 MB (36952136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c87702520b4d885f0cf1d773a1e853e83867a749ad550302728db1ea383167f`  
		Last Modified: Fri, 09 May 2025 05:44:15 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim` - unknown; unknown

```console
$ docker pull ruby@sha256:292366d901d4fddc65a89de1ecb000ffedb14ce4b1737b0d92788a454bf7a6f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2511622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65ece841c8c602107ae2ea086d6da7a8bf9121da5b66596da5b537dc19f525bf`

```dockerfile
```

-	Layers:
	-	`sha256:70fb22704d2ae71485fe30f02fbd897405e047a5ffa012332a926610ba49f32c`  
		Last Modified: Tue, 29 Apr 2025 12:26:46 GMT  
		Size: 2.5 MB (2487496 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e625b562be160602a4e3b335342546c7ae4677b44c83fc7571ddc086bd325ab6`  
		Last Modified: Tue, 29 Apr 2025 12:26:46 GMT  
		Size: 24.1 KB (24126 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:slim` - linux; arm64 variant v8

```console
$ docker pull ruby@sha256:7b1287368b78964e35fd714da3484284711cd0419c8d7a63f3bf7c208aa27793
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.7 MB (72658771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b54a23c4e8057d181b284b9e31a6abf2cf57e86e6de30e0fd201e4a03f98d13d`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 14 Apr 2025 17:03:18 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
# Mon, 14 Apr 2025 17:03:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 17:03:18 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Mon, 14 Apr 2025 17:03:18 GMT
ENV LANG=C.UTF-8
# Mon, 14 Apr 2025 17:03:18 GMT
ENV RUBY_VERSION=3.4.3
# Mon, 14 Apr 2025 17:03:18 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.3.tar.xz
# Mon, 14 Apr 2025 17:03:18 GMT
ENV RUBY_DOWNLOAD_SHA256=174dcd8c516694f833fd3c93ea227fa6c3321464577a3882a6fc7e4fe20237fd
# Mon, 14 Apr 2025 17:03:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Mon, 14 Apr 2025 17:03:18 GMT
ENV GEM_HOME=/usr/local/bundle
# Mon, 14 Apr 2025 17:03:18 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Mon, 14 Apr 2025 17:03:18 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Apr 2025 17:03:18 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Mon, 14 Apr 2025 17:03:18 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:943331d8a9a9863299c02e5de6cce58602a5bc3dc564315aa886fe706376f27f`  
		Last Modified: Thu, 08 May 2025 17:04:42 GMT  
		Size: 28.1 MB (28066622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:073578d117750f596aa7c996766062136858c6982a3366ccfda4b86863b9f6e4`  
		Last Modified: Thu, 08 May 2025 17:06:10 GMT  
		Size: 3.3 MB (3322929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a6a41801c108bbc051599c06248ae883c1dfda0b5e11ba381d880d24951703c`  
		Last Modified: Thu, 08 May 2025 17:06:09 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae18597c9cbc3d9ab9a28a66718f125bf8d796b73ee69e42e532accbad1c8547`  
		Last Modified: Thu, 08 May 2025 17:08:41 GMT  
		Size: 41.3 MB (41268886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40f48b38b9108fda2cf8a0ab879c1089d22e8d033f0e391711ec50057afc7ace`  
		Last Modified: Thu, 08 May 2025 17:08:39 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim` - unknown; unknown

```console
$ docker pull ruby@sha256:f822ff4e9b38f79ea6314ffcfcf5540b5e379dbf59c461961eff4360d2975f86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2509722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17256bc2126fb882e934b0b7894cbf72dfd81d0dd11d39cc6318280d05b42e6f`

```dockerfile
```

-	Layers:
	-	`sha256:85f3572794441d249e9a09f50f168ace69a9daa969fa42abe146015adce786ea`  
		Last Modified: Wed, 30 Apr 2025 00:16:09 GMT  
		Size: 2.5 MB (2485546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88f6a7682784d7e96b5bb11972a076cbd545f48a685817038a92f1d33ebc3940`  
		Last Modified: Wed, 30 Apr 2025 00:16:08 GMT  
		Size: 24.2 KB (24176 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:slim` - linux; 386

```console
$ docker pull ruby@sha256:f623b88e17d3e915858e12eaff3570485c574422951d4067d2068c4f945beaf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.7 MB (69670816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07b75f3b2a8fda8cfe9a367e38aa39a203b557c0432cf7f46c04738d9b353ab9`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 14 Apr 2025 17:03:18 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1745798400'
# Mon, 14 Apr 2025 17:03:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 17:03:18 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Mon, 14 Apr 2025 17:03:18 GMT
ENV LANG=C.UTF-8
# Mon, 14 Apr 2025 17:03:18 GMT
ENV RUBY_VERSION=3.4.3
# Mon, 14 Apr 2025 17:03:18 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.3.tar.xz
# Mon, 14 Apr 2025 17:03:18 GMT
ENV RUBY_DOWNLOAD_SHA256=174dcd8c516694f833fd3c93ea227fa6c3321464577a3882a6fc7e4fe20237fd
# Mon, 14 Apr 2025 17:03:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Mon, 14 Apr 2025 17:03:18 GMT
ENV GEM_HOME=/usr/local/bundle
# Mon, 14 Apr 2025 17:03:18 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Mon, 14 Apr 2025 17:03:18 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Apr 2025 17:03:18 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Mon, 14 Apr 2025 17:03:18 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:ad2e653a01d32a9a8676730797453c924f9d10fe1414178e7a26c35132c3691e`  
		Last Modified: Thu, 08 May 2025 17:08:57 GMT  
		Size: 29.2 MB (29210866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8ec91eedda97e22e606173988d5daf2bc5c67d291fc1347f91abb4a33a02aba`  
		Last Modified: Mon, 28 Apr 2025 22:00:55 GMT  
		Size: 3.5 MB (3503452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b53db947854425e09a8a8a5b150a9a6ddc4c750a2429879941de988972dd0289`  
		Last Modified: Mon, 28 Apr 2025 22:00:55 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b19c4438352b1642354933b0e87840e4f59ef859714c8b0b71c500099e14dbe6`  
		Last Modified: Mon, 28 Apr 2025 22:00:56 GMT  
		Size: 37.0 MB (36956165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f8d4104537a071d86b15b26a40689787ae50189dda645f2d861cecb97300858`  
		Last Modified: Mon, 28 Apr 2025 22:00:55 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim` - unknown; unknown

```console
$ docker pull ruby@sha256:e8efbea0c527ecb4c9a9ffe9b266c2e11f2c179a4f1aafd195856539b7b264aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2506281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:032ff6bc4df71255402b64cfe6ca0b0fe91d5c58bf81fe16c8b568d9e097d8bd`

```dockerfile
```

-	Layers:
	-	`sha256:002733363d03086f592a5c1d4cd193cd59fc489810020ce5bc5c9c04147b6db0`  
		Last Modified: Mon, 28 Apr 2025 22:00:55 GMT  
		Size: 2.5 MB (2482360 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:182bfc3dc3b69e48142b6b529eec5667207cc415461f77af1675e5f7347d1ca3`  
		Last Modified: Mon, 28 Apr 2025 22:00:55 GMT  
		Size: 23.9 KB (23921 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:slim` - linux; mips64le

```console
$ docker pull ruby@sha256:612bdd864a6ad9da84b2cc8c42b53c2390b70483bc34609fd6bc00295d463c90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.8 MB (69758322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15e0c6f5fc1397d2e63888771d6f7da849b2783c8b9c3acc2e6153c63ef5a3ca`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 14 Apr 2025 17:03:18 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1745798400'
# Mon, 14 Apr 2025 17:03:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 17:03:18 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Mon, 14 Apr 2025 17:03:18 GMT
ENV LANG=C.UTF-8
# Mon, 14 Apr 2025 17:03:18 GMT
ENV RUBY_VERSION=3.4.3
# Mon, 14 Apr 2025 17:03:18 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.3.tar.xz
# Mon, 14 Apr 2025 17:03:18 GMT
ENV RUBY_DOWNLOAD_SHA256=174dcd8c516694f833fd3c93ea227fa6c3321464577a3882a6fc7e4fe20237fd
# Mon, 14 Apr 2025 17:03:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Mon, 14 Apr 2025 17:03:18 GMT
ENV GEM_HOME=/usr/local/bundle
# Mon, 14 Apr 2025 17:03:18 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Mon, 14 Apr 2025 17:03:18 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Apr 2025 17:03:18 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Mon, 14 Apr 2025 17:03:18 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:901060d913f9d0bbb82847b3b60c3a263ed0dac4f75aa29161be6ed89b57082a`  
		Last Modified: Thu, 08 May 2025 17:09:00 GMT  
		Size: 28.5 MB (28514138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2e3738fdfb9b5496051b58acd79f288b004b1f351674ceee392730c95f7c3b6`  
		Last Modified: Mon, 28 Apr 2025 21:53:55 GMT  
		Size: 2.9 MB (2895397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c5fbfddeac5bac55c315c978ba37e7118f419f17dc4c97d077c9e354a1897ee`  
		Last Modified: Fri, 09 May 2025 01:19:29 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0c82b36c040b0444acd4dc17758ac35576a2df1c9365bce638cac1f88093f73`  
		Last Modified: Tue, 29 Apr 2025 18:16:36 GMT  
		Size: 38.3 MB (38348456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43f9c350c5292e2c9d14647e07d6d4c3711780fb3fdaf13615829b851bd6eca5`  
		Last Modified: Tue, 29 Apr 2025 18:16:32 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim` - unknown; unknown

```console
$ docker pull ruby@sha256:42f98a629b15d32c285ee2db88299c9c31b029add11afef762f6af57f80ec495
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 KB (23875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b9b40448bc16c9f515f88a07d9b09583948244a48e9700b311f7fb0ff0de9f1`

```dockerfile
```

-	Layers:
	-	`sha256:c15aa1a425f894d3bd0f21f655ed9dfb144142fe93e2105a7d5583e987be5e72`  
		Last Modified: Tue, 29 Apr 2025 18:16:32 GMT  
		Size: 23.9 KB (23875 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:slim` - linux; ppc64le

```console
$ docker pull ruby@sha256:a603e7fc612a125224e324b839082d90ae0a36c8587befd0aa33c25d757467eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.6 MB (74586635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b68b6e0429ceab955ea97bc249954a4105897eac89b2d568daab303ff0e8e43f`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 14 Apr 2025 17:03:18 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1745798400'
# Mon, 14 Apr 2025 17:03:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 17:03:18 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Mon, 14 Apr 2025 17:03:18 GMT
ENV LANG=C.UTF-8
# Mon, 14 Apr 2025 17:03:18 GMT
ENV RUBY_VERSION=3.4.3
# Mon, 14 Apr 2025 17:03:18 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.3.tar.xz
# Mon, 14 Apr 2025 17:03:18 GMT
ENV RUBY_DOWNLOAD_SHA256=174dcd8c516694f833fd3c93ea227fa6c3321464577a3882a6fc7e4fe20237fd
# Mon, 14 Apr 2025 17:03:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Mon, 14 Apr 2025 17:03:18 GMT
ENV GEM_HOME=/usr/local/bundle
# Mon, 14 Apr 2025 17:03:18 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Mon, 14 Apr 2025 17:03:18 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Apr 2025 17:03:18 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Mon, 14 Apr 2025 17:03:18 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:a53e75e229cd115b5249f6e60d40785f1bfff9e7ccc2df65672a6f67afd0e348`  
		Last Modified: Thu, 08 May 2025 17:09:00 GMT  
		Size: 32.1 MB (32068443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:467dd76f60873e36a2ef2d22238cf80226734882a65c6026751c657d5e01c4ff`  
		Last Modified: Mon, 28 Apr 2025 21:47:41 GMT  
		Size: 3.7 MB (3702919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:895a5d43e9710a6e7cc4fa2a97548175c06fb684ef5a6bf6bf104beb7d07f590`  
		Last Modified: Fri, 09 May 2025 01:19:30 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:713b24ddcfdffc530745b299c9f67efefd7f1a1100bdf09e6b0c717f25cf266f`  
		Last Modified: Tue, 29 Apr 2025 03:28:01 GMT  
		Size: 38.8 MB (38814940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7487785ff2c02224f71c75cf07488d2310d63da949e3d16a3860630c8b5e8c8`  
		Last Modified: Tue, 29 Apr 2025 03:27:59 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim` - unknown; unknown

```console
$ docker pull ruby@sha256:9319f6e70f55c1585f2cf9c31c2b37db1385f61d57fa42cd146eca10dfebc97d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2513614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e25eba80b8bccbffc68862a882ec065d2272367c4d8e42e90b09304a232451b9`

```dockerfile
```

-	Layers:
	-	`sha256:bdadefd44753ade5782f428580506778f235e2f81897697ada0808ad57d7f729`  
		Last Modified: Tue, 29 Apr 2025 03:27:59 GMT  
		Size: 2.5 MB (2489561 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59d6483871b40ce39239e0a492a34626a24f74bb4276eb99fd05528467c1af12`  
		Last Modified: Tue, 29 Apr 2025 03:27:59 GMT  
		Size: 24.1 KB (24053 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:slim` - linux; s390x

```console
$ docker pull ruby@sha256:c5e78f0e0debf3f07e3cae96072133f8cc97d871e077db5ec6b67d53087ffed7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.0 MB (68033317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:686dc9c957bf443ec0d255586f0923704f62a0b62d19819a379fc801177030c7`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 14 Apr 2025 17:03:18 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1745798400'
# Mon, 14 Apr 2025 17:03:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 17:03:18 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Mon, 14 Apr 2025 17:03:18 GMT
ENV LANG=C.UTF-8
# Mon, 14 Apr 2025 17:03:18 GMT
ENV RUBY_VERSION=3.4.3
# Mon, 14 Apr 2025 17:03:18 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.3.tar.xz
# Mon, 14 Apr 2025 17:03:18 GMT
ENV RUBY_DOWNLOAD_SHA256=174dcd8c516694f833fd3c93ea227fa6c3321464577a3882a6fc7e4fe20237fd
# Mon, 14 Apr 2025 17:03:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Mon, 14 Apr 2025 17:03:18 GMT
ENV GEM_HOME=/usr/local/bundle
# Mon, 14 Apr 2025 17:03:18 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Mon, 14 Apr 2025 17:03:18 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Apr 2025 17:03:18 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Mon, 14 Apr 2025 17:03:18 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:2fb020f3caf1bc1659faa36e1595ae5ea71b8a94867ff23421b5ce8ca15030f4`  
		Last Modified: Thu, 08 May 2025 17:09:11 GMT  
		Size: 26.9 MB (26884867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa0c23ce11bc586ccd35a7b59168f12424eaaae2ea1392071067aeede22ffc19`  
		Last Modified: Mon, 28 Apr 2025 21:45:26 GMT  
		Size: 3.2 MB (3163400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f515e38b8637e561c1ce51f4b0bbec9e8cfb12699d7508d7151a47016b7a541e`  
		Last Modified: Fri, 09 May 2025 01:19:30 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daca12e98d04ed6862fde516dbf1fb8a6e2f498bd9d1b2ce46e0886668d13b63`  
		Last Modified: Tue, 29 Apr 2025 02:27:30 GMT  
		Size: 38.0 MB (37984719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fa3c6bd2ec7b277fa7f92704bc7cb19c5a86104b9135756cd7e50c96bea9656`  
		Last Modified: Tue, 29 Apr 2025 02:27:29 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim` - unknown; unknown

```console
$ docker pull ruby@sha256:68b1ab5778591c1bdfbf1677f826db95e749878f242571aef46b8af45b3b7116
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2508942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11857fb10e98d528f08c07f682186fb7b344477cc3e1139699ccd00e6c13cf44`

```dockerfile
```

-	Layers:
	-	`sha256:9f5a08a82ed9ddf77eeb8dccb72fa7f16266eae0463cfc78813da0370e9cf774`  
		Last Modified: Tue, 29 Apr 2025 02:27:29 GMT  
		Size: 2.5 MB (2484963 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93f5931ceed30a1460583ecfe3625f54e50b79f65cfdb1aa388f48134a65bc49`  
		Last Modified: Tue, 29 Apr 2025 02:27:29 GMT  
		Size: 24.0 KB (23979 bytes)  
		MIME: application/vnd.in-toto+json
