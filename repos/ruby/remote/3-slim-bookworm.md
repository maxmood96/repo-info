## `ruby:3-slim-bookworm`

```console
$ docker pull ruby@sha256:7bb0e1e46378217ce0775845f6d64b039c56d2890bc715536e6687ab13fe2930
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
$ docker pull ruby@sha256:581fc2162515aac9be327b4b7c8220d2187adfaf4455d76cf10e0d6b7163b166
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.8 MB (80836245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08cc647ea305334ee804ade0779864b47849ae817557b91e666766d8406d23f9`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 09 Jul 2024 05:04:38 GMT
ADD file:3d9897cfe027ecc7cbdb16e74a676ed143725ea2d08dbb0dde23309e041de0f3 in / 
# Tue, 09 Jul 2024 05:04:38 GMT
CMD ["bash"]
# Tue, 09 Jul 2024 05:04:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jul 2024 05:04:38 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Tue, 09 Jul 2024 05:04:38 GMT
ENV LANG=C.UTF-8
# Tue, 09 Jul 2024 05:04:38 GMT
ENV RUBY_VERSION=3.3.4
# Tue, 09 Jul 2024 05:04:38 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.4.tar.xz
# Tue, 09 Jul 2024 05:04:38 GMT
ENV RUBY_DOWNLOAD_SHA256=1caaee9a5a6befef54bab67da68ace8d985e4fb59cd17ce23c28d9ab04f4ddad
# Tue, 09 Jul 2024 05:04:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 09 Jul 2024 05:04:38 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 09 Jul 2024 05:04:38 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 09 Jul 2024 05:04:38 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jul 2024 05:04:38 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 09 Jul 2024 05:04:38 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:e4fff0779e6ddd22366469f08626c3ab1884b5cbe1719b26da238c95f247b305`  
		Last Modified: Tue, 13 Aug 2024 00:23:48 GMT  
		Size: 29.1 MB (29126232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df69ca400a9eeda43226007e9c269895d0b4e52c9e967ba1a3cb140830a28115`  
		Last Modified: Tue, 13 Aug 2024 01:17:01 GMT  
		Size: 13.9 MB (13862388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2c3f7fa3919a4cae785cbf336e4653cfd1a538d643453aad4dbd10ce861e648`  
		Last Modified: Tue, 13 Aug 2024 01:16:59 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43aa6b364ee1363d03031e2fdaec208f3e46f99676d608b7e516b771aaa2823b`  
		Last Modified: Tue, 13 Aug 2024 01:17:01 GMT  
		Size: 37.8 MB (37847286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db442b7bb2380d28cf0d42a561ac01ad1326f5883f58f74284515c5e264e60ca`  
		Last Modified: Tue, 13 Aug 2024 01:16:59 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-slim-bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:f664c7465ced6130d7b83acab0347b5488296ae5250719ba3d065e8ebed1bdf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3923281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31800818f9e782844ea422331260f28cd6b073fede7f5a2d769e3400c9ba7729`

```dockerfile
```

-	Layers:
	-	`sha256:74e4dff922b95ccbd7708c05882e624e73e2cd08c91be55050ae5eb48cf0691a`  
		Last Modified: Tue, 13 Aug 2024 01:17:00 GMT  
		Size: 3.9 MB (3898453 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9830d7eaff19e252369e2efd8dcf07d650d77e5b2e7fee7d433d2578dd641f4`  
		Last Modified: Tue, 13 Aug 2024 01:16:59 GMT  
		Size: 24.8 KB (24828 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-slim-bookworm` - linux; arm variant v5

```console
$ docker pull ruby@sha256:e9346cc2dd2be75b2dfb569db6d373d5777f9946f7ec2d610e1938f744ba6c20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.7 MB (72687162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4109a7c893c45062063d432b38c615679063023aab2b2f70f56507ffe465d6ec`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 09 Jul 2024 05:04:38 GMT
ADD file:0a38a76ef88f0bc858f9663f2ec636121970b50fcd7a62192be7a7eba71bd6b4 in / 
# Tue, 09 Jul 2024 05:04:38 GMT
CMD ["bash"]
# Tue, 09 Jul 2024 05:04:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jul 2024 05:04:38 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Tue, 09 Jul 2024 05:04:38 GMT
ENV LANG=C.UTF-8
# Tue, 09 Jul 2024 05:04:38 GMT
ENV RUBY_VERSION=3.3.4
# Tue, 09 Jul 2024 05:04:38 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.4.tar.xz
# Tue, 09 Jul 2024 05:04:38 GMT
ENV RUBY_DOWNLOAD_SHA256=1caaee9a5a6befef54bab67da68ace8d985e4fb59cd17ce23c28d9ab04f4ddad
# Tue, 09 Jul 2024 05:04:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 09 Jul 2024 05:04:38 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 09 Jul 2024 05:04:38 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 09 Jul 2024 05:04:38 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jul 2024 05:04:38 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 09 Jul 2024 05:04:38 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:1bc90b37f777aded897944b0ce596c103432c1b84f7b626b9fd4a53356f006da`  
		Last Modified: Tue, 13 Aug 2024 00:58:27 GMT  
		Size: 26.9 MB (26887303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b960e7fcbdf0fe6a8f21767c9ff06d14602e6fb7ef0c1b9ebafc337877422d4`  
		Last Modified: Tue, 13 Aug 2024 22:26:01 GMT  
		Size: 11.6 MB (11616583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa5ccd2a6f24fcfec3b462bf2c1a1bc99d30be0fbfc225e5d0541564cf3141e5`  
		Last Modified: Tue, 13 Aug 2024 22:26:00 GMT  
		Size: 199.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:333ff8a2b4085bec52207a1992453ae3a9cecd0733179c3c9f57b341ead489c8`  
		Last Modified: Tue, 13 Aug 2024 22:39:46 GMT  
		Size: 34.2 MB (34182934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:622ab4ef3f5808d1679014999a2c56e8cd4c68ccf6eacd4cc5758cb92f9eb84e`  
		Last Modified: Tue, 13 Aug 2024 22:39:45 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-slim-bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:786e185e7cb44bcfd1c18db56b7248398ad14646eb3a2b543e034362a1a71d2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3893862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9177a9671e38f464ece690f3a91d5eb0060033d388163795eb6a71fdd0c70f1`

```dockerfile
```

-	Layers:
	-	`sha256:1152bc25c68da9138c915774721a4e07dca09c77f7a619dcca382f06c20844c0`  
		Last Modified: Tue, 13 Aug 2024 22:39:45 GMT  
		Size: 3.9 MB (3868894 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92a6c2bd84b9ff2270b90004915bcf2ef5e69a581e05172dd7e83416ecb2113b`  
		Last Modified: Tue, 13 Aug 2024 22:39:45 GMT  
		Size: 25.0 KB (24968 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-slim-bookworm` - linux; arm variant v7

```console
$ docker pull ruby@sha256:d6cf144e6279c35e3dc23f8928f554b1c63f9b729cc7bccd221ce9870ae07d52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.7 MB (69721808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8841828c099689eb2ff80f35044305f359ba87cbe798394ebc23a7a1dd0d35a7`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 09 Jul 2024 05:04:38 GMT
ADD file:452463dee9ffb3b2caafcf6c3f48a08dc239b49a5caf21d3da0d28de4df4fd38 in / 
# Tue, 09 Jul 2024 05:04:38 GMT
CMD ["bash"]
# Tue, 09 Jul 2024 05:04:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jul 2024 05:04:38 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Tue, 09 Jul 2024 05:04:38 GMT
ENV LANG=C.UTF-8
# Tue, 09 Jul 2024 05:04:38 GMT
ENV RUBY_VERSION=3.3.4
# Tue, 09 Jul 2024 05:04:38 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.4.tar.xz
# Tue, 09 Jul 2024 05:04:38 GMT
ENV RUBY_DOWNLOAD_SHA256=1caaee9a5a6befef54bab67da68ace8d985e4fb59cd17ce23c28d9ab04f4ddad
# Tue, 09 Jul 2024 05:04:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 09 Jul 2024 05:04:38 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 09 Jul 2024 05:04:38 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 09 Jul 2024 05:04:38 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jul 2024 05:04:38 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 09 Jul 2024 05:04:38 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:cf43e4280314547b69ae6040ab5c16458259478e27c46528b9d7898d69f26d84`  
		Last Modified: Tue, 13 Aug 2024 01:00:55 GMT  
		Size: 24.7 MB (24718142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cd3673264628d68026a5c0114f0622395677b4901726ce493fc623dd29bacbf`  
		Last Modified: Tue, 13 Aug 2024 23:30:15 GMT  
		Size: 11.0 MB (10952449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53686910b94bce05337ffb25a090902de9667a3388330d35300a208c6d8c5477`  
		Last Modified: Tue, 13 Aug 2024 23:30:14 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36c6f8c17f3243aa728f6b046baba6eb7104f9ceaeb13f87484189d3c3436237`  
		Last Modified: Tue, 13 Aug 2024 23:43:34 GMT  
		Size: 34.1 MB (34050879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d69c1b86928191ccda5e9091d78ccf1d072a224c05020812888a8da6a60d477a`  
		Last Modified: Tue, 13 Aug 2024 23:43:32 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-slim-bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:e80a0cff8c28c5733443ea685dd3125b23f7165a9b72289379bfc539301af259
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3893516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a64642496da0b7b5079bb9ee59726e2a88661eaed9611e2b724dc48d3e0b6d94`

```dockerfile
```

-	Layers:
	-	`sha256:ce13d5b003aa70a454435e2a7bc152b400c2a20d94bec2c10d4e09e88c11fa14`  
		Last Modified: Tue, 13 Aug 2024 23:43:33 GMT  
		Size: 3.9 MB (3868547 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6784382e6b5a829deff679100e833c386fd3140f8c56e700122215c306a8eece`  
		Last Modified: Tue, 13 Aug 2024 23:43:32 GMT  
		Size: 25.0 KB (24969 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull ruby@sha256:8616e98f47dd7cb0b59b4654fbea4df4f1ec115cc466b375bcfb73f9c7077c3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.8 MB (79769111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c726cd3104b757ba333f714ce9a972027de990c2ac38ca44a1b920f5d128fff9`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 09 Jul 2024 05:04:38 GMT
ADD file:4aa9ddc52f046592777767c91a04b9490d98811bedb8980fca794d55bbad1a0f in / 
# Tue, 09 Jul 2024 05:04:38 GMT
CMD ["bash"]
# Tue, 09 Jul 2024 05:04:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jul 2024 05:04:38 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Tue, 09 Jul 2024 05:04:38 GMT
ENV LANG=C.UTF-8
# Tue, 09 Jul 2024 05:04:38 GMT
ENV RUBY_VERSION=3.3.4
# Tue, 09 Jul 2024 05:04:38 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.4.tar.xz
# Tue, 09 Jul 2024 05:04:38 GMT
ENV RUBY_DOWNLOAD_SHA256=1caaee9a5a6befef54bab67da68ace8d985e4fb59cd17ce23c28d9ab04f4ddad
# Tue, 09 Jul 2024 05:04:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 09 Jul 2024 05:04:38 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 09 Jul 2024 05:04:38 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 09 Jul 2024 05:04:38 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jul 2024 05:04:38 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 09 Jul 2024 05:04:38 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:aa6fbc30c84e14e64571d3d7b547ea801dfca8a7bd74bd930b5ea5de3eb2f442`  
		Last Modified: Tue, 13 Aug 2024 00:42:45 GMT  
		Size: 29.2 MB (29156528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e2545e0e32f4ff221945e9e6016407464688d54d7e466553b1a8a96c0872f0e`  
		Last Modified: Tue, 13 Aug 2024 11:25:49 GMT  
		Size: 12.7 MB (12701605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e32849646863d2b4e41b0e9ea3632fb5615f5caa9b19265dcf26f1f2962f98d`  
		Last Modified: Tue, 13 Aug 2024 11:25:48 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0df3ce4786f0bf9f244700258417545dc26aca521e4c101308eda867b252a57d`  
		Last Modified: Tue, 13 Aug 2024 11:32:17 GMT  
		Size: 37.9 MB (37910639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da92cd6d38d6cc2cfdb873d6e8e23952d30fd2080c907054a41480355be554e0`  
		Last Modified: Tue, 13 Aug 2024 11:32:15 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-slim-bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:e7eb66c7f2be43a59f5248ddb35d20c361e61c62d912eb7fa6539fb3d61a8f22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3894903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7439a40094683633a6d172af60e0e5d2c8a743abea5c078843850d6349679813`

```dockerfile
```

-	Layers:
	-	`sha256:233f253b5dec3a38e70c4894b5919d812b7bbe0739a28ddf5869615f5deca5f5`  
		Last Modified: Tue, 13 Aug 2024 11:32:16 GMT  
		Size: 3.9 MB (3869719 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7bf2a89643a5c1b1df57027b444f650ca8ea514856aac6496ca4f0e668d41ab`  
		Last Modified: Tue, 13 Aug 2024 11:32:15 GMT  
		Size: 25.2 KB (25184 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-slim-bookworm` - linux; 386

```console
$ docker pull ruby@sha256:435d78fd29bc2256e5dd5fb0e54e44d11d27eb9cff94f986611a4b3fe85b5bb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.5 MB (77522235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da09fcfcafe4613c6daa5e2b5fe5c9f32c30606f14d28d1f8ef8e49c766934dc`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 09 Jul 2024 05:04:38 GMT
ADD file:6c928b979f82a9dc0b3801b97a516aaa3d17fe57cb9eecc077d202afda56d2fb in / 
# Tue, 09 Jul 2024 05:04:38 GMT
CMD ["bash"]
# Tue, 09 Jul 2024 05:04:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jul 2024 05:04:38 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Tue, 09 Jul 2024 05:04:38 GMT
ENV LANG=C.UTF-8
# Tue, 09 Jul 2024 05:04:38 GMT
ENV RUBY_VERSION=3.3.4
# Tue, 09 Jul 2024 05:04:38 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.4.tar.xz
# Tue, 09 Jul 2024 05:04:38 GMT
ENV RUBY_DOWNLOAD_SHA256=1caaee9a5a6befef54bab67da68ace8d985e4fb59cd17ce23c28d9ab04f4ddad
# Tue, 09 Jul 2024 05:04:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 09 Jul 2024 05:04:38 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 09 Jul 2024 05:04:38 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 09 Jul 2024 05:04:38 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jul 2024 05:04:38 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 09 Jul 2024 05:04:38 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:82c8eed510ac33a6df3a546a738b1f3806df7958ea977484d0f77eabe177108d`  
		Last Modified: Tue, 13 Aug 2024 00:42:35 GMT  
		Size: 30.1 MB (30144281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2572d535f7b2573470fdda666760f0f06b4c3bed4e12de9c3d24d0e946b11901`  
		Last Modified: Tue, 13 Aug 2024 01:17:25 GMT  
		Size: 13.4 MB (13410234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20f0b01b9c3ce549cc281eb4b3a639d45ea81f1098a7f832d80cd43505bd4ebe`  
		Last Modified: Tue, 13 Aug 2024 01:17:24 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c7cc50f922f7c8b37c8b2e939c7efc3e568c80d6d59c3da9efb088c027d21c7`  
		Last Modified: Tue, 13 Aug 2024 01:17:26 GMT  
		Size: 34.0 MB (33967378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f4e834f5431550733ac32bbe7b08e9cf38dde416c88e5fb2771c453e5684ffd`  
		Last Modified: Tue, 13 Aug 2024 01:17:25 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-slim-bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:c83ca57adc43b7af36e2b0102b78214c19fc0001649920386a879aac27e3b65e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3917064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67ecb9fbc2ee2848f90648c32505a7fc7819d746de648cd4d0145b7f3eda69c5`

```dockerfile
```

-	Layers:
	-	`sha256:a7f991334e0ff51cb5eb51984f0c72d0851f81482bcfcb92045e68b4004d8194`  
		Last Modified: Tue, 13 Aug 2024 01:17:25 GMT  
		Size: 3.9 MB (3892291 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1b76dc60a357c5b8fc4151aa2f92d474eec2b49b0546a4b88747e41ff1f5415`  
		Last Modified: Tue, 13 Aug 2024 01:17:24 GMT  
		Size: 24.8 KB (24773 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-slim-bookworm` - linux; mips64le

```console
$ docker pull ruby@sha256:52799b65bd28893eed600e5d79c7e152681cbdfb0fdfe3fdab8a2aa5439fd8f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.3 MB (77347776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e3467a0d66184557dcc868964cdf613811c18f1722c3052e5c5da197f6179f8`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 09 Jul 2024 05:04:38 GMT
ADD file:2fad80cfc89f7b624d81eb445f9c64e4cd3f190b85d89f40c33eb7e4bc562c6d in / 
# Tue, 09 Jul 2024 05:04:38 GMT
CMD ["bash"]
# Tue, 09 Jul 2024 05:04:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jul 2024 05:04:38 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Tue, 09 Jul 2024 05:04:38 GMT
ENV LANG=C.UTF-8
# Tue, 09 Jul 2024 05:04:38 GMT
ENV RUBY_VERSION=3.3.4
# Tue, 09 Jul 2024 05:04:38 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.4.tar.xz
# Tue, 09 Jul 2024 05:04:38 GMT
ENV RUBY_DOWNLOAD_SHA256=1caaee9a5a6befef54bab67da68ace8d985e4fb59cd17ce23c28d9ab04f4ddad
# Tue, 09 Jul 2024 05:04:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 09 Jul 2024 05:04:38 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 09 Jul 2024 05:04:38 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 09 Jul 2024 05:04:38 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jul 2024 05:04:38 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 09 Jul 2024 05:04:38 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:e8ebfef8c6b7f6250b54eec0d5d1ae5d66f60f418704f4094cb9291dc214be0f`  
		Last Modified: Tue, 13 Aug 2024 00:22:29 GMT  
		Size: 29.1 MB (29124941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a29f82a4f2bd0516b307bf6bd851118bce8d79c93b70d071579584e54643c03f`  
		Last Modified: Wed, 14 Aug 2024 18:40:43 GMT  
		Size: 12.9 MB (12877318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:847dd58447ca517adac4c901b301759bb9a3f4ca479627ab43194ec15f54411a`  
		Last Modified: Wed, 14 Aug 2024 18:40:41 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90ec0495addff2b22388dbfadf8fa0ce0952ba3f87f77fd8089265e7adcc2c0c`  
		Last Modified: Wed, 14 Aug 2024 19:12:16 GMT  
		Size: 35.3 MB (35345176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9a999149ccc19e75cd3f7009acc18746eea30a9befe951e37ab5ef4b27cabee`  
		Last Modified: Wed, 14 Aug 2024 19:12:13 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-slim-bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:2b449395b9921523fdc6724e9cb706f1dd0ba865b37e837092581f0c46de7a9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.7 KB (24711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c3bb21d91390f148dbcb912634aaaedc1a1676e6501e25a122c5925b2b52247`

```dockerfile
```

-	Layers:
	-	`sha256:75449d5fae62ff876ca54e7b7638370847f4c6b251e2070267cd04d797fcedcb`  
		Last Modified: Wed, 14 Aug 2024 19:12:13 GMT  
		Size: 24.7 KB (24711 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-slim-bookworm` - linux; ppc64le

```console
$ docker pull ruby@sha256:dbe22c02689ddab0823ea85d513e90f315b869460a5d8ef414e2f93147ae26fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.4 MB (83401078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce4a101129343059e268c182175dc44d9b0c164daad4c85c7fc089d934e6d9ca`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 09 Jul 2024 05:04:38 GMT
ADD file:2fb9d7e332d1c4cadd8151a8485091fce600b230987f3b306d19efc82ed0ac9c in / 
# Tue, 09 Jul 2024 05:04:38 GMT
CMD ["bash"]
# Tue, 09 Jul 2024 05:04:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jul 2024 05:04:38 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Tue, 09 Jul 2024 05:04:38 GMT
ENV LANG=C.UTF-8
# Tue, 09 Jul 2024 05:04:38 GMT
ENV RUBY_VERSION=3.3.4
# Tue, 09 Jul 2024 05:04:38 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.4.tar.xz
# Tue, 09 Jul 2024 05:04:38 GMT
ENV RUBY_DOWNLOAD_SHA256=1caaee9a5a6befef54bab67da68ace8d985e4fb59cd17ce23c28d9ab04f4ddad
# Tue, 09 Jul 2024 05:04:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 09 Jul 2024 05:04:38 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 09 Jul 2024 05:04:38 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 09 Jul 2024 05:04:38 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jul 2024 05:04:38 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 09 Jul 2024 05:04:38 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:36f5dfff311b1880d6202ab548fb824c9591bd1c9a04f7ab677235edddf9ab23`  
		Last Modified: Tue, 13 Aug 2024 00:26:22 GMT  
		Size: 33.1 MB (33122300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f0cf796cae99504f3068978ff5f161517cac64ae09622b15dbdef26d42273f8`  
		Last Modified: Tue, 13 Aug 2024 12:17:59 GMT  
		Size: 14.6 MB (14582474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3859d6b3a3306dfc2a51fa9405190ce888bab8e837387c18768ad5b7928e4efd`  
		Last Modified: Tue, 13 Aug 2024 12:17:59 GMT  
		Size: 199.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f7727f857563f9af95710dc5e84c0713159a7b2682f732554787aa1883f2824`  
		Last Modified: Tue, 13 Aug 2024 12:25:43 GMT  
		Size: 35.7 MB (35695962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89ed405155adf6dd1ac38ff04785989c4721daf4119b3f716747c13e67e804c7`  
		Last Modified: Tue, 13 Aug 2024 12:25:41 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-slim-bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:cb38a7d3777cd678220043a24fe02b5a019fff9e02603f80fcf1113b9de3a355
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3909173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18649711ad91330ad68a1f0b46175568eec6ee6ba8583ef0ef3cd985bb250188`

```dockerfile
```

-	Layers:
	-	`sha256:2b4c64a7f3626b6b0b156bea30feebd5738071466c0589cc0bec5aff3808f59b`  
		Last Modified: Tue, 13 Aug 2024 12:25:42 GMT  
		Size: 3.9 MB (3884277 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a9d9669e626f89471f8ec0db3a04d372f813b0f60933373199cf9da1c6e61d9`  
		Last Modified: Tue, 13 Aug 2024 12:25:41 GMT  
		Size: 24.9 KB (24896 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-slim-bookworm` - linux; s390x

```console
$ docker pull ruby@sha256:2d1f258c5bac2783a8c2345baa553238bf43ad91ab1be8f06db020510c9f9baa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.5 MB (74487933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da9223df512426c2ac4956424e9b62ebbbd72a77256f0842e4fcea3705e73758`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 09 Jul 2024 05:04:38 GMT
ADD file:2e68e80c30908adf6b4b6a8ea2cb0711c5b296a8ba63e2cff3b70422a4daaf97 in / 
# Tue, 09 Jul 2024 05:04:38 GMT
CMD ["bash"]
# Tue, 09 Jul 2024 05:04:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jul 2024 05:04:38 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Tue, 09 Jul 2024 05:04:38 GMT
ENV LANG=C.UTF-8
# Tue, 09 Jul 2024 05:04:38 GMT
ENV RUBY_VERSION=3.3.4
# Tue, 09 Jul 2024 05:04:38 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.4.tar.xz
# Tue, 09 Jul 2024 05:04:38 GMT
ENV RUBY_DOWNLOAD_SHA256=1caaee9a5a6befef54bab67da68ace8d985e4fb59cd17ce23c28d9ab04f4ddad
# Tue, 09 Jul 2024 05:04:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 09 Jul 2024 05:04:38 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 09 Jul 2024 05:04:38 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 09 Jul 2024 05:04:38 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jul 2024 05:04:38 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 09 Jul 2024 05:04:38 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:218a263fc97fdfaefe7df9b0e23e00c5a0b71a094fd212f91621d5683c6e3514`  
		Last Modified: Tue, 13 Aug 2024 00:47:29 GMT  
		Size: 27.5 MB (27490097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3604e9ef7f51f68332fa82d020496b963b0e75b2cccc7b7109048943c8d1ca38`  
		Last Modified: Tue, 13 Aug 2024 09:47:42 GMT  
		Size: 12.0 MB (12032579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a21a2ff28c736149bed107e05a8870ffb0b6d1dcdfc14ad38f1b9f6ef0f66cc0`  
		Last Modified: Tue, 13 Aug 2024 09:47:41 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21f8f94c08afd8c61c1b8e3c5f68e3a7fe1b237003d3d476fe27f576ab0c4e33`  
		Last Modified: Tue, 13 Aug 2024 09:53:57 GMT  
		Size: 35.0 MB (34964917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a6d47d631a1a609199f78aae9a9fb0d3eca9d09e4bf9099f1fee6261da788c7`  
		Last Modified: Tue, 13 Aug 2024 09:53:56 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-slim-bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:9dda12b43406d37bb0fd1e89f77a07bcee9934ca44db12845fca129c60a6d85c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3911532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a84a415d73369091b2c28a8389695f32d3fec9a08e668b3e8bb78e347d093c6e`

```dockerfile
```

-	Layers:
	-	`sha256:eb1b7d35123deff3d44654337beb8c6407cfdc41488a8a98f329631340ce2983`  
		Last Modified: Tue, 13 Aug 2024 09:53:56 GMT  
		Size: 3.9 MB (3886704 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13c668aac3d9413092bb485cf77ae4cbc155fa551707f2355736b9fb7897f48c`  
		Last Modified: Tue, 13 Aug 2024 09:53:56 GMT  
		Size: 24.8 KB (24828 bytes)  
		MIME: application/vnd.in-toto+json
