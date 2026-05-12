## `ruby:slim-trixie`

```console
$ docker pull ruby@sha256:bf59457be37b4d045e06ccf332f4ace6b711623d1d9dadc30d55a246d2bf3477
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
$ docker pull ruby@sha256:b4533aab82b33def4feac424959414fcc2fb7740edf96dfa95d3d122b9a22e7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.7 MB (80696774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53667bb4c2ef81747e70c9badf6844c43a9bc83771ae22329807afbfa1050146`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Tue, 12 May 2026 00:19:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 12 May 2026 00:19:49 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 12 May 2026 00:22:14 GMT
ENV LANG=C.UTF-8
# Tue, 12 May 2026 00:22:14 GMT
ENV RUBY_VERSION=4.0.4
# Tue, 12 May 2026 00:22:14 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/4.0/ruby-4.0.4.tar.xz
# Tue, 12 May 2026 00:22:14 GMT
ENV RUBY_DOWNLOAD_SHA256=6ff9d2d6e75f5a6f997222ecc45f79209d663737eceb3689d1f42ab952673fb7
# Tue, 12 May 2026 00:22:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 		${rustArch:+--enable-zjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 12 May 2026 00:22:14 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 12 May 2026 00:22:14 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 12 May 2026 00:22:14 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 00:22:14 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 12 May 2026 00:22:14 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:57fb71246055257a374deb7564ceca10f43c2352572b501efc08add5d24ebb61`  
		Last Modified: Fri, 08 May 2026 18:24:13 GMT  
		Size: 29.8 MB (29780226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d9db46579a4e191db96f871c96575d5212b4f83e091154da102e10225f233be`  
		Last Modified: Tue, 12 May 2026 00:22:23 GMT  
		Size: 1.3 MB (1279828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dea6ca8f3753a26be49d586d066338e53fd9c2f313f8e666d2e02b078d611cf0`  
		Last Modified: Tue, 12 May 2026 00:22:23 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dab6e174a56c0819c1cb734202414f583e1458210091c3fbf36658eec01a8e62`  
		Last Modified: Tue, 12 May 2026 00:22:30 GMT  
		Size: 49.6 MB (49636385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7c3bf8ddaf3a89d08e8210c51dc07a1b2d884d1a6f9d439b5cc0b5c025635bf`  
		Last Modified: Tue, 12 May 2026 00:22:24 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim-trixie` - unknown; unknown

```console
$ docker pull ruby@sha256:221a6310fff8606a2115b5dc8133d84254c6f3bbfa16284b49e9ad1f498c3a41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2240362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc17c08b69867f87ed013aeb4ca4a34f54a1be917f28b2206f07c1e1efb63420`

```dockerfile
```

-	Layers:
	-	`sha256:eae50f791bd05ce5c7891c78e3d8fba6fcc4fa5510828973f9f795df9a24c997`  
		Last Modified: Tue, 12 May 2026 00:22:23 GMT  
		Size: 2.2 MB (2216043 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1f20244fed4809247676eb86f798a3e8e35258c64b30883c68a6b9e68cf1e9d`  
		Last Modified: Tue, 12 May 2026 00:22:23 GMT  
		Size: 24.3 KB (24319 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:slim-trixie` - linux; arm variant v5

```console
$ docker pull ruby@sha256:a675dfe49f2ba53cb526d518768476e6b0e1b9a2d1cfa7da3189b6bb32d6a4bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.9 MB (71858095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1679fe466950635bf7adef85c10c142b56bcf3be68d92dfbba68a120a5489b3`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1777939200'
# Tue, 12 May 2026 00:04:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 12 May 2026 00:04:25 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 12 May 2026 00:07:28 GMT
ENV LANG=C.UTF-8
# Tue, 12 May 2026 00:07:28 GMT
ENV RUBY_VERSION=4.0.4
# Tue, 12 May 2026 00:07:28 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/4.0/ruby-4.0.4.tar.xz
# Tue, 12 May 2026 00:07:28 GMT
ENV RUBY_DOWNLOAD_SHA256=6ff9d2d6e75f5a6f997222ecc45f79209d663737eceb3689d1f42ab952673fb7
# Tue, 12 May 2026 00:07:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 		${rustArch:+--enable-zjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 12 May 2026 00:07:28 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 12 May 2026 00:07:28 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 12 May 2026 00:07:28 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 00:07:28 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 12 May 2026 00:07:28 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:8f774e9b92b540806fc05167db7ce09a3e1b12abdb9d496f7b8c82138656065a`  
		Last Modified: Fri, 08 May 2026 18:33:49 GMT  
		Size: 27.9 MB (27948200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa9949348b0067d41c769dc21b5ebc0dc6cab43056f9107b05cc67e7afdec653`  
		Last Modified: Tue, 12 May 2026 00:07:37 GMT  
		Size: 1.3 MB (1263632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f5695633fe6b02a41e3e4c14cbcdc41cd784e7fb984cc46d858d4cc37c72d04`  
		Last Modified: Tue, 12 May 2026 00:07:37 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cf1ab054188fee2bab3a7ba5517498c5613a9a77e4528b30d77c7f8d402ea2d`  
		Last Modified: Tue, 12 May 2026 00:07:38 GMT  
		Size: 42.6 MB (42645929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a3ba388bfeb1d22594a4bc896daf8893e8c49b2cf8c42e1344217947eb704d0`  
		Last Modified: Tue, 12 May 2026 00:07:37 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim-trixie` - unknown; unknown

```console
$ docker pull ruby@sha256:97124a24277b877a672aac09e69eb792374d2cd634aea463cbdbcf8c5253bd28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2243509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13f908a6b3c53b4f94060fc14cfb442fbeb6444d5e263416bb5c23c920d74e9c`

```dockerfile
```

-	Layers:
	-	`sha256:62e9472f6ef4b2af8c164f4daa50acb899d1baebe082c80432ec9886f7d99fc4`  
		Last Modified: Tue, 12 May 2026 00:07:37 GMT  
		Size: 2.2 MB (2219038 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:415b30022e1537f31b6c27cfb0b2c33a6e40a494f53fa5e8c19586bed6e17602`  
		Last Modified: Tue, 12 May 2026 00:07:37 GMT  
		Size: 24.5 KB (24471 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:slim-trixie` - linux; arm variant v7

```console
$ docker pull ruby@sha256:c87e8ff609f49490a87db8d2b8bf3561f28890a7f7eeea0b4e7801b58fd801e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69945156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14ac9e29e184d9f9cb68ce27bfdea39b3d4110cc9d2cca1b901e64f0a6239d17`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1777939200'
# Tue, 12 May 2026 00:07:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 12 May 2026 00:07:06 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 12 May 2026 00:09:52 GMT
ENV LANG=C.UTF-8
# Tue, 12 May 2026 00:09:52 GMT
ENV RUBY_VERSION=4.0.4
# Tue, 12 May 2026 00:09:52 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/4.0/ruby-4.0.4.tar.xz
# Tue, 12 May 2026 00:09:52 GMT
ENV RUBY_DOWNLOAD_SHA256=6ff9d2d6e75f5a6f997222ecc45f79209d663737eceb3689d1f42ab952673fb7
# Tue, 12 May 2026 00:09:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 		${rustArch:+--enable-zjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 12 May 2026 00:09:52 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 12 May 2026 00:09:52 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 12 May 2026 00:09:52 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 00:09:52 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 12 May 2026 00:09:52 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:f1433620eadfdfe016c8054b954f619ae5bca159f35a9459c36a76d9ef4d39c3`  
		Last Modified: Fri, 08 May 2026 18:37:58 GMT  
		Size: 26.2 MB (26214912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:223c22dce9f8a56d7fd678aee98c2950f31fbe31be4bf10103f050f16a35ccf2`  
		Last Modified: Tue, 12 May 2026 00:10:02 GMT  
		Size: 1.2 MB (1237520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5016fb680695cfc950594d1ecad89c077410f5eb7695c6eea05ed5cd78ffe22`  
		Last Modified: Tue, 12 May 2026 00:09:46 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5661432ca8ccc05be30ec2e12a5657928fd83345f98044b822239d17def8de86`  
		Last Modified: Tue, 12 May 2026 00:10:03 GMT  
		Size: 42.5 MB (42492389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4292ea76771fc949afcc272543229d21e2799057929a6ae81221ca767f3e5c7d`  
		Last Modified: Tue, 12 May 2026 00:10:02 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim-trixie` - unknown; unknown

```console
$ docker pull ruby@sha256:e3bbccb9f0c1ebb20a600f12617f721412d52421ef7b983c0bfdd00b8d29392b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2241950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a7f0c76d918f3e5746f324b5e804544c70c88967c99554792d9183be2b291a4`

```dockerfile
```

-	Layers:
	-	`sha256:9112fefeecb8ccac57518fbe03f95f63bc1f529807f3942e21b534486d6ac707`  
		Last Modified: Tue, 12 May 2026 00:10:02 GMT  
		Size: 2.2 MB (2217479 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75a2dafa26b6af78baa9fe7f31e7ea681bfb03b79d7d95a6189e5ed8a9c922d8`  
		Last Modified: Tue, 12 May 2026 00:10:02 GMT  
		Size: 24.5 KB (24471 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:slim-trixie` - linux; arm64 variant v8

```console
$ docker pull ruby@sha256:5c82b005c2d6bfbc5c53ea297333869f43781f4ff872dc5afa10dd7ef6f61100
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.9 MB (80883470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a236c96a1a6be59aeb4b9716cba6b4287faf4c951f748a32a56c22e6df20c336`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Tue, 12 May 2026 00:18:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 12 May 2026 00:18:21 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 12 May 2026 00:20:51 GMT
ENV LANG=C.UTF-8
# Tue, 12 May 2026 00:20:51 GMT
ENV RUBY_VERSION=4.0.4
# Tue, 12 May 2026 00:20:51 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/4.0/ruby-4.0.4.tar.xz
# Tue, 12 May 2026 00:20:51 GMT
ENV RUBY_DOWNLOAD_SHA256=6ff9d2d6e75f5a6f997222ecc45f79209d663737eceb3689d1f42ab952673fb7
# Tue, 12 May 2026 00:20:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 		${rustArch:+--enable-zjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 12 May 2026 00:20:51 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 12 May 2026 00:20:51 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 12 May 2026 00:20:51 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 00:20:51 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 12 May 2026 00:20:51 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97a8372e98928fc5c0f1db09c8f38389e0522136c9e432a09d758c7482bbe69f`  
		Last Modified: Tue, 12 May 2026 00:21:01 GMT  
		Size: 1.3 MB (1261700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afe8afd1788f94f664b8d01df9a8080e2648e46fe005d9eda7b2db1f187c2f93`  
		Last Modified: Tue, 12 May 2026 00:20:58 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2524289164a549d44bd038dfe5a842186d0712398ac7a8e50c129232faf5812`  
		Last Modified: Tue, 12 May 2026 00:21:03 GMT  
		Size: 49.5 MB (49477793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35b50062f22ffa8f9ecd2cc06a7f7ead569231fffce8bd3948bfd078fee2eb2d`  
		Last Modified: Tue, 12 May 2026 00:21:01 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim-trixie` - unknown; unknown

```console
$ docker pull ruby@sha256:b7c78f01b7c3de51ee4ebb80f49924b1379104fbed20e99d59c789800ed23ade
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2240868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:787ce8d4cb2d40248b82718a71b3c552fd3783ee5b5177901083faf17f64ad2f`

```dockerfile
```

-	Layers:
	-	`sha256:f5eb357293909552a2d7fe01f842cf3b3eeb6e2239a243e62552525bca4bad5b`  
		Last Modified: Tue, 12 May 2026 00:21:01 GMT  
		Size: 2.2 MB (2216351 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b584145ef200a9bf8c152d0bdd184708570582be61fa733e8cbce8320cade8fe`  
		Last Modified: Tue, 12 May 2026 00:21:01 GMT  
		Size: 24.5 KB (24517 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:slim-trixie` - linux; 386

```console
$ docker pull ruby@sha256:0d0036c211068ec7f6ed3fc0d2c2b9701c062ae55f661bb77a770b7f5f7b5ef7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.0 MB (74987303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03473b147a15095b72ea7e217c9bb05f25bee548ce8e4f3503bb278b941a2c6d`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1777939200'
# Tue, 12 May 2026 00:05:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 12 May 2026 00:05:28 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 12 May 2026 00:08:04 GMT
ENV LANG=C.UTF-8
# Tue, 12 May 2026 00:08:04 GMT
ENV RUBY_VERSION=4.0.4
# Tue, 12 May 2026 00:08:04 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/4.0/ruby-4.0.4.tar.xz
# Tue, 12 May 2026 00:08:04 GMT
ENV RUBY_DOWNLOAD_SHA256=6ff9d2d6e75f5a6f997222ecc45f79209d663737eceb3689d1f42ab952673fb7
# Tue, 12 May 2026 00:08:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 		${rustArch:+--enable-zjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 12 May 2026 00:08:04 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 12 May 2026 00:08:04 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 12 May 2026 00:08:04 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 00:08:04 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 12 May 2026 00:08:04 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:43e2ffbaa23260ffb4e3de716920f2ed9e6af56e465ca1233a2d84c2cc1cf005`  
		Last Modified: Fri, 08 May 2026 18:32:48 GMT  
		Size: 31.3 MB (31296400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca51ea7e5275a84afc501f3f19fd27599ab3bcd94b1f3334c456162e70f4610e`  
		Last Modified: Tue, 12 May 2026 00:08:14 GMT  
		Size: 1.3 MB (1287489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16aeac6fe6cb29f54881a5600e71af863bcf23a9e7698f9e4fc9d049e1aa11e2`  
		Last Modified: Tue, 12 May 2026 00:08:13 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2d5bbdbe618f83297aa662257757e79be098b6156364550cf4e7bf3913f4671`  
		Last Modified: Tue, 12 May 2026 00:08:15 GMT  
		Size: 42.4 MB (42403078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e32a3816e81c2593f4fd19e9159ddd66ec24ce922f17e3a9b76343f8d6ba573f`  
		Last Modified: Tue, 12 May 2026 00:08:13 GMT  
		Size: 145.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim-trixie` - unknown; unknown

```console
$ docker pull ruby@sha256:c7f9881bf8422caf3e70298d6471ee67fda848cf1dae8da03a580615e8652828
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2237478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24c08e590ac6a5ce53e03783378cbf7416e89668993631766e521fd20acf98f6`

```dockerfile
```

-	Layers:
	-	`sha256:af6efeea3c703774402ee45e1bfdac24c656560f4cc35c51197937707debf678`  
		Last Modified: Tue, 12 May 2026 00:08:14 GMT  
		Size: 2.2 MB (2213216 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f6482f9f89077cc99d22f637773587cfebf995cccc30ca9d97591066aaeaa6e`  
		Last Modified: Tue, 12 May 2026 00:08:14 GMT  
		Size: 24.3 KB (24262 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:slim-trixie` - linux; ppc64le

```console
$ docker pull ruby@sha256:1167b7cffe25647b83f7924dd3b1bea42191890286cf997dbe152e6c37f582d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.4 MB (79376840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6564b63f83d27b8c36783a4e6fff28a6031b562a0a464cbc3a1b2fe7b5360cf2`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1777939200'
# Sat, 09 May 2026 01:58:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Sat, 09 May 2026 01:58:16 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 12 May 2026 00:58:34 GMT
ENV LANG=C.UTF-8
# Tue, 12 May 2026 00:58:34 GMT
ENV RUBY_VERSION=4.0.4
# Tue, 12 May 2026 00:58:34 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/4.0/ruby-4.0.4.tar.xz
# Tue, 12 May 2026 00:58:34 GMT
ENV RUBY_DOWNLOAD_SHA256=6ff9d2d6e75f5a6f997222ecc45f79209d663737eceb3689d1f42ab952673fb7
# Tue, 12 May 2026 00:58:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 		${rustArch:+--enable-zjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 12 May 2026 00:58:34 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 12 May 2026 00:58:34 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 12 May 2026 00:58:34 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 00:58:35 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 12 May 2026 00:58:35 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:b9baa45d89920bd180d7551ccc5bc535e0c5f55b863ddebddfdc06f9436dfe91`  
		Last Modified: Fri, 08 May 2026 19:46:53 GMT  
		Size: 33.6 MB (33598087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8497ccc5c4c38f9991098194461e4f7c8254daa698ba3731af28f2d577f70bae`  
		Last Modified: Sat, 09 May 2026 02:02:07 GMT  
		Size: 1.3 MB (1309850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8989f35676fce5c3e46abc422f90e102a86d79bee20f6e8bcd07edec926895ef`  
		Last Modified: Sat, 09 May 2026 02:02:07 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63f4b9296553baa38df5a2aa177fb73aa2c787c2231872ba442d534022342a48`  
		Last Modified: Tue, 12 May 2026 00:58:54 GMT  
		Size: 44.5 MB (44468569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bf51e922dbce15ef6e8ec7f13d5c96d98dd3d3fca2a12bec2e53e8b6f941260`  
		Last Modified: Tue, 12 May 2026 00:58:52 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim-trixie` - unknown; unknown

```console
$ docker pull ruby@sha256:80a8b8402c28356eaf23cd38c45ff193fd8a3fcf8a5db73f33eebce9b1dc07a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2243990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dfa32e9ed26a4142e80a0c3c862ba37228717957a1369e19a27076b0706651f`

```dockerfile
```

-	Layers:
	-	`sha256:bc45018ce18aa013ce08d2c8e015123dca19c512a66ba58355d12e2c33038b43`  
		Last Modified: Tue, 12 May 2026 00:58:53 GMT  
		Size: 2.2 MB (2219596 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f1989c6388d6fa66463a37f8bae198ebbfc3ea549312b0b13c8a694a84b191f`  
		Last Modified: Tue, 12 May 2026 00:58:52 GMT  
		Size: 24.4 KB (24394 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:slim-trixie` - linux; riscv64

```console
$ docker pull ruby@sha256:327d3983a3325278c80d23b9f0a77756e707d44ea2526f8fc94ad19ffb7cf6dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.7 MB (73662071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2688c47927454db1c64718e863a3c117ff88842b9f6ef258038b0652758c6b1`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1776729600'
# Fri, 24 Apr 2026 11:28:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Fri, 24 Apr 2026 11:28:07 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 24 Apr 2026 13:25:26 GMT
ENV LANG=C.UTF-8
# Fri, 24 Apr 2026 13:25:26 GMT
ENV RUBY_VERSION=4.0.3
# Fri, 24 Apr 2026 13:25:26 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/4.0/ruby-4.0.3.tar.xz
# Fri, 24 Apr 2026 13:25:26 GMT
ENV RUBY_DOWNLOAD_SHA256=22cf6005d25bbe496b5ebe9224d63a1aaabfbfe02591bb5d612517c5a7836f29
# Fri, 24 Apr 2026 13:25:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 		${rustArch:+--enable-zjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 24 Apr 2026 13:25:26 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 24 Apr 2026 13:25:26 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 24 Apr 2026 13:25:26 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 24 Apr 2026 13:25:27 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 24 Apr 2026 13:25:27 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:c59e3a1f334be9f0528643dd07d69319f75f877f83be33ec1eff872a489985a0`  
		Last Modified: Wed, 22 Apr 2026 02:30:51 GMT  
		Size: 28.3 MB (28280195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf68a0f8c00d3d42b30169c9302b31abfb27a89cbfeeb1d0058da4b95bc125db`  
		Last Modified: Fri, 24 Apr 2026 13:27:12 GMT  
		Size: 1.2 MB (1248916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26e83f8760e009cce9b352d4a88ac9d520f1c80a531ee6feaa03f81575547758`  
		Last Modified: Fri, 24 Apr 2026 13:27:11 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1836f795357453e88414f8b7c5e775f1333d88613dccf2af7a2e776abf7e85d`  
		Last Modified: Fri, 24 Apr 2026 13:27:19 GMT  
		Size: 44.1 MB (44132628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d97decf66cacf54cb0cc4b621839de6afbd593c38d5a75dde5b0eb79c10c8e42`  
		Last Modified: Fri, 24 Apr 2026 13:27:12 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim-trixie` - unknown; unknown

```console
$ docker pull ruby@sha256:d681dde9dced16aa8107208b5cc6a75a82642aad0fb8b85fe4af25e77b96970f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2234382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81a36eae9143bd9f88db368b6e0ad9c4302237e65b5d39354a967644a332cce9`

```dockerfile
```

-	Layers:
	-	`sha256:7ad9057642d4200c8e9efbcb18a67f4de4048f492d4e885a14d80d51aafa9254`  
		Last Modified: Fri, 24 Apr 2026 13:27:12 GMT  
		Size: 2.2 MB (2209988 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7cae890cb6f3c766358459e888d6820df3d004c81dc17fab150a282b3f8e982`  
		Last Modified: Fri, 24 Apr 2026 13:27:12 GMT  
		Size: 24.4 KB (24394 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:slim-trixie` - linux; s390x

```console
$ docker pull ruby@sha256:b876bff51b7e895744a8f0eb7b480a659bbbdb063724b986484234fe5008279e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75421905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:375ea1d0d919e2f53519240138c9233748c005767f1f0c5b9aa95c89d56b019b`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1777939200'
# Tue, 12 May 2026 00:06:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 12 May 2026 00:06:35 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 12 May 2026 00:09:32 GMT
ENV LANG=C.UTF-8
# Tue, 12 May 2026 00:09:32 GMT
ENV RUBY_VERSION=4.0.4
# Tue, 12 May 2026 00:09:32 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/4.0/ruby-4.0.4.tar.xz
# Tue, 12 May 2026 00:09:32 GMT
ENV RUBY_DOWNLOAD_SHA256=6ff9d2d6e75f5a6f997222ecc45f79209d663737eceb3689d1f42ab952673fb7
# Tue, 12 May 2026 00:09:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 		${rustArch:+--enable-zjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 12 May 2026 00:09:32 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 12 May 2026 00:09:32 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 12 May 2026 00:09:32 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 00:09:32 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 12 May 2026 00:09:32 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:2fbbc68c452b3ba3a496488f38159dac53afe693311bee1c04f555d854ff4a2e`  
		Last Modified: Fri, 08 May 2026 18:29:20 GMT  
		Size: 29.8 MB (29840347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8361bffdbabbacb368e63f52c0c760463aa0cdbffb88d4e32eca21deb72b51b0`  
		Last Modified: Tue, 12 May 2026 00:09:46 GMT  
		Size: 1.3 MB (1294710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4df63c9a85019755fb472f2b4596a26d16f481f7027f32c6545bcd0e001dafe2`  
		Last Modified: Tue, 12 May 2026 00:09:46 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:636665b5a6392436cfaa17e416fff85f5a4eae659a33e655b0f807681cdfb165`  
		Last Modified: Tue, 12 May 2026 00:09:48 GMT  
		Size: 44.3 MB (44286513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3bb774371246727c43d4de7bfc652566c7473a9af9482d25cbaf263aae8dea6`  
		Last Modified: Tue, 12 May 2026 00:09:46 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim-trixie` - unknown; unknown

```console
$ docker pull ruby@sha256:d7a76fd4bfdc900c6e71b55eba794492f00c98389288eb85608c25ac1fbd7626
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2241808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b75795199bb6af234c37769f6f0374298b166b680388348ccbf802419d1154e`

```dockerfile
```

-	Layers:
	-	`sha256:4d18a91ac8dbe13400d4ba08e1f9f43eabd8e586f3815fac1126c1b22461cc88`  
		Last Modified: Tue, 12 May 2026 00:09:47 GMT  
		Size: 2.2 MB (2217488 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:902ff7ef2f20bc5eb32a72329175371e90c2b48a1d65528e3947ba7ae733e332`  
		Last Modified: Tue, 12 May 2026 00:09:46 GMT  
		Size: 24.3 KB (24320 bytes)  
		MIME: application/vnd.in-toto+json
