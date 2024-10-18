## `ruby:3-slim-bullseye`

```console
$ docker pull ruby@sha256:db9dccec75933094c39b8934bef5f16a51a77e9287b4f1cabc82e69ac67cf71c
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
$ docker pull ruby@sha256:dcedfa97f2eb1089747a6d85d9d8270585d5813e43445889112436063b7b3a6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.2 MB (79160058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2384bc2c38d54e95d4d1848840e3f8799ef522c1899872f6d76f203886735f4`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 03 Sep 2024 11:03:18 GMT
ADD file:0f6f1b93a8fddd20b36a99cc6cfbe4a03bc7be2adb427f7f8e74a2029c54c8bb in / 
# Tue, 03 Sep 2024 11:03:18 GMT
CMD ["bash"]
# Tue, 03 Sep 2024 11:03:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Sep 2024 11:03:18 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Tue, 03 Sep 2024 11:03:18 GMT
ENV LANG=C.UTF-8
# Tue, 03 Sep 2024 11:03:18 GMT
ENV RUBY_VERSION=3.3.5
# Tue, 03 Sep 2024 11:03:18 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.5.tar.xz
# Tue, 03 Sep 2024 11:03:18 GMT
ENV RUBY_DOWNLOAD_SHA256=51aec7ea89b46125a2c9adc6f36766b65023d47952b916b1aed300ddcc042359
# Tue, 03 Sep 2024 11:03:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 03 Sep 2024 11:03:18 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 03 Sep 2024 11:03:18 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 03 Sep 2024 11:03:18 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Sep 2024 11:03:18 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 03 Sep 2024 11:03:18 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:6dce3b49cfe6dc4b4e0198412bb0578215c86dae41303c47438639853bcba562`  
		Last Modified: Thu, 17 Oct 2024 00:24:36 GMT  
		Size: 31.4 MB (31428800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:882f9c6a50bdedcdb8617a019e94b4ed6e685ed591bb8b3d4536b9a9a4c6917f`  
		Last Modified: Thu, 17 Oct 2024 01:19:31 GMT  
		Size: 10.0 MB (10019176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:675d5e15ade859572009648937e8709022f6153485830c1d22858de4a68230f0`  
		Last Modified: Thu, 17 Oct 2024 01:19:31 GMT  
		Size: 199.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faa2fef12d248bdb11520645c86296baf3632f24c6ab62c9f0d97600230861e2`  
		Last Modified: Thu, 17 Oct 2024 01:19:32 GMT  
		Size: 37.7 MB (37711740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b844a0e386965f1a80a460daba200f03610a52507124a351971eb050b8c30229`  
		Last Modified: Thu, 17 Oct 2024 01:19:31 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-slim-bullseye` - unknown; unknown

```console
$ docker pull ruby@sha256:f601027bed9eda4d765e071f85facd28a940d58beaafd6e1d8d58ebc5520ba9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4118433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c3fad3b3c4a7ed7ffe81e9b79acafc18cdd020d531cf9cee8ed70fac3fce735`

```dockerfile
```

-	Layers:
	-	`sha256:65bcd2689c8a9471ec2155b23c91de70464e79d86c0350056ba9fe56586a538e`  
		Last Modified: Thu, 17 Oct 2024 01:19:31 GMT  
		Size: 4.1 MB (4094755 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f21c46d0a3434dba258aaa33c22b1255d45d90b5d723de8b1ce452554361fba`  
		Last Modified: Thu, 17 Oct 2024 01:19:31 GMT  
		Size: 23.7 KB (23678 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-slim-bullseye` - linux; arm variant v7

```console
$ docker pull ruby@sha256:4da06a3dca63112841e51a46b65fec908294e24122c2f0fc61f5b54f011c6a80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.3 MB (68315689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62a7ae34e3a521ac10e7200efbb20eaf1fd64da5badfa1479f9f5f3a29c200d7`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 03 Sep 2024 11:03:18 GMT
ADD file:9017833b3f74675db45d0ac4f67e9ea2e05e58da02c851ea580aa49f0b310c64 in / 
# Tue, 03 Sep 2024 11:03:18 GMT
CMD ["bash"]
# Tue, 03 Sep 2024 11:03:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Sep 2024 11:03:18 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Tue, 03 Sep 2024 11:03:18 GMT
ENV LANG=C.UTF-8
# Tue, 03 Sep 2024 11:03:18 GMT
ENV RUBY_VERSION=3.3.5
# Tue, 03 Sep 2024 11:03:18 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.5.tar.xz
# Tue, 03 Sep 2024 11:03:18 GMT
ENV RUBY_DOWNLOAD_SHA256=51aec7ea89b46125a2c9adc6f36766b65023d47952b916b1aed300ddcc042359
# Tue, 03 Sep 2024 11:03:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 03 Sep 2024 11:03:18 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 03 Sep 2024 11:03:18 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 03 Sep 2024 11:03:18 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Sep 2024 11:03:18 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 03 Sep 2024 11:03:18 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:ea6a6c5151e68b5b8e6387d29b1e945e29ac292dcf4f3458fa71a33db9e1aa51`  
		Last Modified: Fri, 27 Sep 2024 05:17:51 GMT  
		Size: 26.6 MB (26589312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46196c8de38d62eb2d87f52076af2e99f017004c736a21ea90d08c4421c78c4b`  
		Last Modified: Fri, 27 Sep 2024 18:21:05 GMT  
		Size: 8.1 MB (8140541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1553907295e3a6b1781b8763a6bfcc11c619e93b57b671ef7cfbec60e34f4221`  
		Last Modified: Fri, 27 Sep 2024 18:21:04 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5dd8b3c56180d8b4995ec281014e031056eee015129229112c4024e1b9f2eda`  
		Last Modified: Fri, 27 Sep 2024 18:26:50 GMT  
		Size: 33.6 MB (33585497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2871e443c7189b7791b79b0433074bbf969a94326de434191a069f8a5feb4d3`  
		Last Modified: Fri, 27 Sep 2024 18:26:49 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-slim-bullseye` - unknown; unknown

```console
$ docker pull ruby@sha256:368069554eb61b7cbb4394d0974238badcbacdd8f8a24e751af5b4812349dcd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4092402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3ce07a37ea5009edb247bd732365b0110e225903bd56e188625790b6d15b984`

```dockerfile
```

-	Layers:
	-	`sha256:1390fab70855748e2555d17098fd54af693c516447f808ab9141eb0e259d48f4`  
		Last Modified: Fri, 27 Sep 2024 18:26:49 GMT  
		Size: 4.1 MB (4068657 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad1d5fea64788d11f90613dc9da029865841b06a2892e08612442abc7700fd5a`  
		Last Modified: Fri, 27 Sep 2024 18:26:49 GMT  
		Size: 23.7 KB (23745 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull ruby@sha256:05f382d0bf81479b37aa67da3ac37b587b457765e9a1a5edbca1c9865cc59822
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.9 MB (76949705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39793e3ae83b723550f9817d05be834145208e52084740eb81c0e91e4844d730`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 03 Sep 2024 11:03:18 GMT
ADD file:f3f9a52e18a8da911b50ebddcc922d4b5a7aa8caa6eb15fb5c26c696b8fe9610 in / 
# Tue, 03 Sep 2024 11:03:18 GMT
CMD ["bash"]
# Tue, 03 Sep 2024 11:03:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Sep 2024 11:03:18 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Tue, 03 Sep 2024 11:03:18 GMT
ENV LANG=C.UTF-8
# Tue, 03 Sep 2024 11:03:18 GMT
ENV RUBY_VERSION=3.3.5
# Tue, 03 Sep 2024 11:03:18 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.5.tar.xz
# Tue, 03 Sep 2024 11:03:18 GMT
ENV RUBY_DOWNLOAD_SHA256=51aec7ea89b46125a2c9adc6f36766b65023d47952b916b1aed300ddcc042359
# Tue, 03 Sep 2024 11:03:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 03 Sep 2024 11:03:18 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 03 Sep 2024 11:03:18 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 03 Sep 2024 11:03:18 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Sep 2024 11:03:18 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 03 Sep 2024 11:03:18 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:b3c56a24ca3234ee90349473402ac1b368a2fb3c9620242fa70a85d7396d7799`  
		Last Modified: Thu, 17 Oct 2024 01:15:14 GMT  
		Size: 30.1 MB (30075757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a4d9356bc90752894941fc9a6237e5d953a1f23ea8b5e6c1f92c8b2fdbf0b5d`  
		Last Modified: Thu, 17 Oct 2024 20:22:47 GMT  
		Size: 9.2 MB (9239940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3fe5fdf7905a553d7367a3f240b6a1a83f7457859cfcd68de46fb7d17c92fe3`  
		Last Modified: Thu, 17 Oct 2024 20:22:47 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b06b61aa7c33c5cae5a70a7561e11cc077c9a0ead3f6e37bacfb3995b417a6d7`  
		Last Modified: Thu, 17 Oct 2024 20:34:36 GMT  
		Size: 37.6 MB (37633668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24142f1b2d58f432ed14fae0b58a6c15a5094600bb5aa320f9fb863d136af8f6`  
		Last Modified: Thu, 17 Oct 2024 20:34:34 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-slim-bullseye` - unknown; unknown

```console
$ docker pull ruby@sha256:e9337e95a8f437982ba4224b34b7a5ad3c69654b641bba34960bdb7343e2c39d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4092956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0968ecf5fc0a2cb6c8ea559d8d2efb42a04bfaab5239d0444c20bd382055700`

```dockerfile
```

-	Layers:
	-	`sha256:4f4d381ed12add2350a18a377b312bcacca3f3d076d99aa120ea200c0999a1ac`  
		Last Modified: Thu, 17 Oct 2024 20:34:35 GMT  
		Size: 4.1 MB (4069139 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22fcd481fa482bc2e277271090cd09ed5185a5714afdfd1d35887c85c2fdff09`  
		Last Modified: Thu, 17 Oct 2024 20:34:34 GMT  
		Size: 23.8 KB (23817 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-slim-bullseye` - linux; 386

```console
$ docker pull ruby@sha256:12ac490a447562b2d335659693b800e7ffcf226356a687fb8d7731091ab6fdc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.1 MB (78052260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e261b3519403a753726f71b4ea749d742b15faa9d0e79c08cf0f6087275c8fc6`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 03 Sep 2024 11:03:18 GMT
ADD file:05098c6b0b4cfde8b4ffadc861fc7668bbf1779983d50b6be61989e6378fc17b in / 
# Tue, 03 Sep 2024 11:03:18 GMT
CMD ["bash"]
# Tue, 03 Sep 2024 11:03:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Sep 2024 11:03:18 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Tue, 03 Sep 2024 11:03:18 GMT
ENV LANG=C.UTF-8
# Tue, 03 Sep 2024 11:03:18 GMT
ENV RUBY_VERSION=3.3.5
# Tue, 03 Sep 2024 11:03:18 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.5.tar.xz
# Tue, 03 Sep 2024 11:03:18 GMT
ENV RUBY_DOWNLOAD_SHA256=51aec7ea89b46125a2c9adc6f36766b65023d47952b916b1aed300ddcc042359
# Tue, 03 Sep 2024 11:03:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 03 Sep 2024 11:03:18 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 03 Sep 2024 11:03:18 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 03 Sep 2024 11:03:18 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Sep 2024 11:03:18 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 03 Sep 2024 11:03:18 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:0aff79075c186716daeb376e46e89131aa14f0dc2bd8f794bd04d72494cb4693`  
		Last Modified: Thu, 17 Oct 2024 00:43:15 GMT  
		Size: 32.4 MB (32413830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bfa19dc5601162c7186293bca217c9f33ef34552f2785d5646e1069d3e12e6c`  
		Last Modified: Thu, 17 Oct 2024 01:30:15 GMT  
		Size: 12.0 MB (11994685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:020c08698c1def837e4e34b6ba7d99c42d295de69176e161ec4d7704d3de853f`  
		Last Modified: Thu, 17 Oct 2024 01:30:14 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23402c2850fcc49c9009a8c206e60e3e567afd0e08b7c25092cd138216b6618b`  
		Last Modified: Thu, 17 Oct 2024 01:30:15 GMT  
		Size: 33.6 MB (33643404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:814d9967694cdfb823324a8bf1cc61a83347cb9fe54cbe2b176548e221ea1bfe`  
		Last Modified: Thu, 17 Oct 2024 01:30:14 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-slim-bullseye` - unknown; unknown

```console
$ docker pull ruby@sha256:0a39abdabd63b07711ec67891fa280c5067cebd2a3ba2e8a474556c1c3ace27c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4122600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b72de0b2271fca7398f741e8450ab3692d4203ee2ed2a183676543e969dd269`

```dockerfile
```

-	Layers:
	-	`sha256:7103e722760c06a0aa63a65ffcd3fff6bdf3595d15506b54dcaa844966c85ef5`  
		Last Modified: Thu, 17 Oct 2024 01:30:14 GMT  
		Size: 4.1 MB (4098957 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dcf47fcb5d84f073ef461753e2415f246dc68f1ab6611ae5883a3456a2a87d49`  
		Last Modified: Thu, 17 Oct 2024 01:30:14 GMT  
		Size: 23.6 KB (23643 bytes)  
		MIME: application/vnd.in-toto+json
