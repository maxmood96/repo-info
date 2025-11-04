## `ruby:slim`

```console
$ docker pull ruby@sha256:6ad3e90f473b88a0aa45c8cd00a99c896a7fab1c0814767d40c501028aafbeab
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
$ docker pull ruby@sha256:77748c7b096c6b80951ff1363667cf785bb2f4a8e3df13b705ee0dd546b96bc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73216274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8751674567e290883149e2611db67b53b8add9f8981de88b0ca15586a839262e`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 04:26:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 04:26:53 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 04 Nov 2025 04:29:19 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 04:29:19 GMT
ENV RUBY_VERSION=3.4.7
# Tue, 04 Nov 2025 04:29:19 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Tue, 04 Nov 2025 04:29:19 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Tue, 04 Nov 2025 04:29:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 04 Nov 2025 04:29:19 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 04 Nov 2025 04:29:19 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 04 Nov 2025 04:29:19 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 04:29:19 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 04 Nov 2025 04:29:19 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:d7ecded7702a5dbf6d0f79a71edc34b534d08f3051980e2c948fba72db3197fc`  
		Last Modified: Tue, 04 Nov 2025 00:13:18 GMT  
		Size: 29.8 MB (29778104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b16a280ca2b46af513537a7d977a24dd0779f3b6b7ac2a379e32564f36bb62f`  
		Last Modified: Tue, 04 Nov 2025 04:29:35 GMT  
		Size: 1.3 MB (1279642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f12677bb7810189f862e4324fd378db9bc131cf8446805bdcf9923ad09d03c85`  
		Last Modified: Tue, 04 Nov 2025 04:29:34 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0e12593a63e3781635232c1a24a87ca6d97150b8e568eaf8b52786ec55eeb71`  
		Last Modified: Tue, 04 Nov 2025 04:29:38 GMT  
		Size: 42.2 MB (42158201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e06499c8b4d3f65803507338e343bb0c0eb7ef53c593e6346ab9acb506fd6234`  
		Last Modified: Tue, 04 Nov 2025 04:29:34 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim` - unknown; unknown

```console
$ docker pull ruby@sha256:e6210bae78aa8ed0196104a628939cda8eb2fadc19a1656315eb5ded3359c647
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2244138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a66a6fca1e5c3b3e8a9a1253f640d22328f5463f0cbb2283b720d08cbc54c9a0`

```dockerfile
```

-	Layers:
	-	`sha256:b5107d557f85ed7e31556b0aa13c12f1152bd3faa908f08d2a0a464ba09c7ea4`  
		Last Modified: Tue, 04 Nov 2025 09:30:28 GMT  
		Size: 2.2 MB (2219931 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:668041cc7484c860289c5743e96e573c752e0fb7c1cf9f01c3e59bb1cbc53646`  
		Last Modified: Tue, 04 Nov 2025 09:30:28 GMT  
		Size: 24.2 KB (24207 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:slim` - linux; arm variant v5

```console
$ docker pull ruby@sha256:fc1a242baa3a5d158318cad64633163ddd1670467dfc62702e286b296ec6399e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.2 MB (67203817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a710f2ce8c5db4bb4277e206aae522a42ffd1894a835799fcf09a5d809179219`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 02:03:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 02:03:02 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 04 Nov 2025 02:06:06 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 02:06:06 GMT
ENV RUBY_VERSION=3.4.7
# Tue, 04 Nov 2025 02:06:06 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Tue, 04 Nov 2025 02:06:06 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Tue, 04 Nov 2025 02:06:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 04 Nov 2025 02:06:06 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 04 Nov 2025 02:06:06 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 04 Nov 2025 02:06:06 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 02:06:06 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 04 Nov 2025 02:06:06 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:453afc2258d7bc5729fed5672fb95bafa092e30a933b4377a12034be940a671b`  
		Last Modified: Tue, 04 Nov 2025 00:13:12 GMT  
		Size: 27.9 MB (27946438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3d0265096dbb284e99f417d031751021c9ae33f3f78009b02af999be9e103e7`  
		Last Modified: Tue, 04 Nov 2025 02:06:26 GMT  
		Size: 1.3 MB (1263101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c42e7d8c22f9871e899c99d0145179d61bb16cb0f11b7df59c608bb94a3a078`  
		Last Modified: Tue, 04 Nov 2025 02:06:26 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:987310b96c69b7fafcffd3f0c2d88aa5284782f309dcc87f43d62249512214fc`  
		Last Modified: Tue, 04 Nov 2025 02:06:29 GMT  
		Size: 38.0 MB (37993947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:390710f8f96b1b345e49ef7872d2c458ecba1c9ddb776a51d10371ca2e6f2708`  
		Last Modified: Tue, 04 Nov 2025 02:06:26 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim` - unknown; unknown

```console
$ docker pull ruby@sha256:24905919c49808a5fa1cd20a775f56500a7b3a7baab541084146516170239b05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2247284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d86d772ede42d396325e0c1ace2a414724e8cdccd41b6a7317a3b7b6e3115999`

```dockerfile
```

-	Layers:
	-	`sha256:9f94a732927ef77e77ec757c93a584a98c3919a1e9afc163a881a4c54b9412eb`  
		Last Modified: Tue, 04 Nov 2025 06:59:36 GMT  
		Size: 2.2 MB (2222926 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3cafeeb962fa6d8dbd11403a4fe02a6d1aac12b9cb679462bc8258953ae56d02`  
		Last Modified: Tue, 04 Nov 2025 06:59:37 GMT  
		Size: 24.4 KB (24358 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:slim` - linux; arm variant v7

```console
$ docker pull ruby@sha256:2aa4e08a9704c88e94a17615498761c1626a719cef9e499ccd189bdc9f4ac56b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.3 MB (65315463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac29bcccc07a0799692b6868fef217753cf8a5029f2ec3514b7d7672fa4fe0ea`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 02:33:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 02:33:46 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 04 Nov 2025 02:39:26 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 02:39:26 GMT
ENV RUBY_VERSION=3.4.7
# Tue, 04 Nov 2025 02:39:26 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Tue, 04 Nov 2025 02:39:26 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Tue, 04 Nov 2025 02:39:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 04 Nov 2025 02:39:26 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 04 Nov 2025 02:39:26 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 04 Nov 2025 02:39:26 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 02:39:26 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 04 Nov 2025 02:39:26 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:8945aefb71bd942499dd072e2c7c869b6b74b7c4dd83bff59c209b7b95d52a9f`  
		Last Modified: Tue, 04 Nov 2025 00:13:33 GMT  
		Size: 26.2 MB (26213039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bff1cf61353f8dff587184978fed1cbb398dca8e140da33c564fefaec487d2e`  
		Last Modified: Tue, 04 Nov 2025 02:36:44 GMT  
		Size: 1.2 MB (1236604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ff3a12ca516b6f79cbac115ae27bcbb967dd1009cccff770d79a7cae383a3f`  
		Last Modified: Tue, 04 Nov 2025 02:36:43 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e6468f7034188523d195654f6c0fb84c8d7d944289ae9e8f031cb5f78c7a580`  
		Last Modified: Tue, 04 Nov 2025 02:39:45 GMT  
		Size: 37.9 MB (37865491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:950069925d30b01ded0a2ed186d917f1eff55fd5881f4be0b9d79cf4398aee27`  
		Last Modified: Tue, 04 Nov 2025 02:39:41 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim` - unknown; unknown

```console
$ docker pull ruby@sha256:17d2d0e13f399c40e16ae826e9455632b52cb8a08052a296d4f11da7a40d8f52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2245724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6113ab0c25ee5963cbab0d000eea01677b25bbb01cb889068b525b1f9db11463`

```dockerfile
```

-	Layers:
	-	`sha256:2eb7130c81d361e7126914f0bae0260b383226a5df0eb8d351dbb43e5624dedb`  
		Last Modified: Tue, 04 Nov 2025 09:57:54 GMT  
		Size: 2.2 MB (2221367 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6a0fa3860d1711fc9fc74ea78ff4d980c77f682401a6e205a7e23c4212c7775`  
		Last Modified: Tue, 04 Nov 2025 09:57:55 GMT  
		Size: 24.4 KB (24357 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:slim` - linux; arm64 variant v8

```console
$ docker pull ruby@sha256:217c10b06680fff66566e77f0cbff06ee3fc80439a8f9bb18c0dfb54a386bac4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.5 MB (73549487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb25a092c81a03e10ae41606c339c848e918f1c14fa5136c07380693e898907f`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:39:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 01:39:19 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 04 Nov 2025 01:41:55 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 01:41:55 GMT
ENV RUBY_VERSION=3.4.7
# Tue, 04 Nov 2025 01:41:55 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Tue, 04 Nov 2025 01:41:55 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Tue, 04 Nov 2025 01:41:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 04 Nov 2025 01:41:55 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 04 Nov 2025 01:41:55 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 04 Nov 2025 01:41:55 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 01:41:55 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 04 Nov 2025 01:41:55 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:51365f04b68881c6fd3d04aa38cdb689fdee6efba2aa6afcf2da5385022cf475`  
		Last Modified: Tue, 04 Nov 2025 00:13:42 GMT  
		Size: 30.1 MB (30142298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:318c83755afbe771e645a69fd11df0a60d6e7dd541fc57e5b0f1b0be4b2a0883`  
		Last Modified: Tue, 04 Nov 2025 01:42:11 GMT  
		Size: 1.3 MB (1261429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:547c48599929aa6c7fb7bed5f82a13c0154ffb885b6f1e85e9f644b0767b1f70`  
		Last Modified: Tue, 04 Nov 2025 01:42:11 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6e552b7b884adedf291e273039ac04ca2d02aac2bf91d0790d8ed1417002926`  
		Last Modified: Tue, 04 Nov 2025 01:42:15 GMT  
		Size: 42.1 MB (42145432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a35feb980ed30f707dcd311800ab0801ef0c69e411a8513d2d57f4e74def26a3`  
		Last Modified: Tue, 04 Nov 2025 01:42:11 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim` - unknown; unknown

```console
$ docker pull ruby@sha256:7516476d3016fd0df281b3c56cfc717bb6d46bf5cc161d63be1a9c4eb95e5df4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2244643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a01fd47e9373403a75acc4ddbf518cf91302b3eb683cf6ccb8a4c62bbca694e`

```dockerfile
```

-	Layers:
	-	`sha256:6fd4356c3122bbb2df3a38fbab3ddd7c78ceea54fc73fc475b6e7da909760468`  
		Last Modified: Tue, 04 Nov 2025 09:58:21 GMT  
		Size: 2.2 MB (2220239 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c6e23f912d368df62b1b604d04c4b90a2fe93ddd455ad6c3887b6d9e8b36b95`  
		Last Modified: Tue, 04 Nov 2025 09:58:22 GMT  
		Size: 24.4 KB (24404 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:slim` - linux; 386

```console
$ docker pull ruby@sha256:f55cbce6f7f36a9e26eb52aaaf4c82085ed07de699b8f62881369e131dbddad4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.3 MB (70322393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f348504d5cc7bfd10d78bf66194805157f84e4b20471c8b3dab50793c8fafad7`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:44:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 01:44:11 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 04 Nov 2025 01:46:36 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 01:46:36 GMT
ENV RUBY_VERSION=3.4.7
# Tue, 04 Nov 2025 01:46:36 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Tue, 04 Nov 2025 01:46:36 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Tue, 04 Nov 2025 01:46:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 04 Nov 2025 01:46:36 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 04 Nov 2025 01:46:36 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 04 Nov 2025 01:46:36 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 01:46:36 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 04 Nov 2025 01:46:36 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:7f24a3a0c200106d0d9ab7b6264e50c689910154fb57bf08185b9eaf995db758`  
		Last Modified: Tue, 04 Nov 2025 00:13:54 GMT  
		Size: 31.3 MB (31294783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:380acf751aaff0cfcd7c7756af40398b9e9251c60fe774d6d48963af3717bcc3`  
		Last Modified: Tue, 04 Nov 2025 01:46:50 GMT  
		Size: 1.3 MB (1287391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f55b67e2dc259fce5e8fa56c275eb0bd052dee0d93161ad5d6486b89b81f0a0`  
		Last Modified: Tue, 04 Nov 2025 01:46:50 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a82374b54f555ed1a6248dd56e3235a34a764acf07fc586aadc26e7f5fce03c9`  
		Last Modified: Tue, 04 Nov 2025 01:46:54 GMT  
		Size: 37.7 MB (37739889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a46e8572e02cd7c9e07973aa5140d4f031a8b3d33dd466bcea06b4a9f3977a41`  
		Last Modified: Tue, 04 Nov 2025 01:46:51 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim` - unknown; unknown

```console
$ docker pull ruby@sha256:09450b91672f839544dfdb6ab884f4bb5ac10ace90fd3e32456848b3741844c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2241252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c4a97b437aa3de3f1436d65721b57079b1fda7c838b7000e7fd69eb663663a7`

```dockerfile
```

-	Layers:
	-	`sha256:528353befb89caacd1d6e06e67a89863a3d7632dae453581dc15477996b40f11`  
		Last Modified: Tue, 04 Nov 2025 09:30:26 GMT  
		Size: 2.2 MB (2217104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3ab9f36842f2890b1a1f1dbbecf393b39cb25574a52092bdb9acf7f54271a92`  
		Last Modified: Tue, 04 Nov 2025 09:30:26 GMT  
		Size: 24.1 KB (24148 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:slim` - linux; ppc64le

```console
$ docker pull ruby@sha256:57ae83326892cd535ad09284316d32721326737bca12daed9a5b1c2cda64eeb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.5 MB (74510430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:620475e433391d35feb6c3cdc7b2d0acdda9c86e934c82431967cbb552f5c8f8`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 12:16:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 12:16:16 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 04 Nov 2025 12:30:02 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 12:30:02 GMT
ENV RUBY_VERSION=3.4.7
# Tue, 04 Nov 2025 12:30:02 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Tue, 04 Nov 2025 12:30:02 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Tue, 04 Nov 2025 12:30:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 04 Nov 2025 12:30:02 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 04 Nov 2025 12:30:02 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 04 Nov 2025 12:30:02 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 12:30:05 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 04 Nov 2025 12:30:05 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:eead2c4a2afd8217def9d0ca536e7e4108ac8a91745ca25e76eb059260c04aab`  
		Last Modified: Tue, 04 Nov 2025 00:20:53 GMT  
		Size: 33.6 MB (33598647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b7cafc9e521290ae17ae96071a62fa0ce9cc48a489bf957fdf15c09abb8a804`  
		Last Modified: Tue, 04 Nov 2025 12:20:45 GMT  
		Size: 1.3 MB (1310384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b74df3c614cf044979896d45fdbb3780600a0f2a6f1a699a70de10d0153e6928`  
		Last Modified: Tue, 04 Nov 2025 12:20:45 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4312abe5d4cfc4eeefc5f2b09f01e9ba77dc6e592a8edc74346d8a87f2e45f28`  
		Last Modified: Tue, 04 Nov 2025 12:31:03 GMT  
		Size: 39.6 MB (39601068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf418f7fe1d0352a8b07d3730b4a8393da06df977da19a9696aee08825025762`  
		Last Modified: Tue, 04 Nov 2025 12:31:00 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim` - unknown; unknown

```console
$ docker pull ruby@sha256:faa45f006e59e355754cdcfa34e42892ff56a927cfafdddb9e14dee7b3a0092d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2247764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8859b98156bbdafcc3c3f5fd79ae93a2e6eba1e5ac12fc82ee01b9f0407f806d`

```dockerfile
```

-	Layers:
	-	`sha256:9b5b4c830ebf1f1a28c0da9e887ae43c43867fbc77cdfa3c13a316469af1e8da`  
		Last Modified: Tue, 04 Nov 2025 15:57:47 GMT  
		Size: 2.2 MB (2223484 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7cf84e3f5a6a0b36281e376644d791da27dfb0fec27c0cff78e1ac682bccac7b`  
		Last Modified: Tue, 04 Nov 2025 15:57:48 GMT  
		Size: 24.3 KB (24280 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:slim` - linux; riscv64

```console
$ docker pull ruby@sha256:a1ca485d75920b875fa59dfce8fb7eaaa9bed93cac31d2258e536dabc955b2e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.5 MB (67516123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e1b3cc6d3aa406fa71feb9c0a06adfaaf90e16271ca14d0fa6eb06e070470e5`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 07 Oct 2025 23:03:17 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1760918400'
# Tue, 07 Oct 2025 23:03:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 07 Oct 2025 23:03:17 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 07 Oct 2025 23:03:17 GMT
ENV LANG=C.UTF-8
# Tue, 07 Oct 2025 23:03:17 GMT
ENV RUBY_VERSION=3.4.7
# Tue, 07 Oct 2025 23:03:17 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Tue, 07 Oct 2025 23:03:17 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Tue, 07 Oct 2025 23:03:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 07 Oct 2025 23:03:17 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 07 Oct 2025 23:03:17 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 07 Oct 2025 23:03:17 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Oct 2025 23:03:17 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 07 Oct 2025 23:03:17 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:6d1567708d42906165204f9177d357cb6a2fd51f758da447f1743b00813f892f`  
		Last Modified: Tue, 21 Oct 2025 00:37:37 GMT  
		Size: 28.3 MB (28275650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be0079cf54a2702e7ac3d63e57e80e047b561eba1572a468c5e9eaca622b2b0c`  
		Last Modified: Thu, 23 Oct 2025 17:20:49 GMT  
		Size: 1.2 MB (1248220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91be70239e4204f47cf1219800928796e88572d01a93fd66cf37029227209a3b`  
		Last Modified: Thu, 23 Oct 2025 17:20:50 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:804556a509ec963e34bacf1629f5f304702c17b137a5858a9c7d5f22c1a0eb7d`  
		Last Modified: Thu, 23 Oct 2025 19:37:25 GMT  
		Size: 38.0 MB (37991920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b299b7eba01a71f5967ffe2de173ed58ad61a85f48562e8e3967ff73694328cc`  
		Last Modified: Thu, 23 Oct 2025 19:37:21 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim` - unknown; unknown

```console
$ docker pull ruby@sha256:5aba1c3d3a946be28f2dc53e1debfa46a1e30649c2e6dd8d450ddea337b88aa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2238203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:640149a40c9c6d6fcc8bf1792d757dcce592e17de5a2e442446f5675ed77acb1`

```dockerfile
```

-	Layers:
	-	`sha256:e9fe1f3f62060e78e62c6a4a0a626245dcc47079c16bc26960800b200b4dd9f9`  
		Last Modified: Thu, 23 Oct 2025 20:57:44 GMT  
		Size: 2.2 MB (2213879 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf9f06ebf9eb07258d0b9304d03d6b4df326134df0484fa06d416a42c219c021`  
		Last Modified: Thu, 23 Oct 2025 20:57:45 GMT  
		Size: 24.3 KB (24324 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:slim` - linux; s390x

```console
$ docker pull ruby@sha256:e9ce8fa83d14963b728cfb794ed35ef457b78678dd2899aa09f3fc87bafbdba5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.4 MB (70419754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:356108064ef1e5834018b75fa1ff66274a475c0ac160e7a61e9ceaf1cd8cd1b6`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 12:39:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 12:39:14 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 04 Nov 2025 12:46:16 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 12:46:16 GMT
ENV RUBY_VERSION=3.4.7
# Tue, 04 Nov 2025 12:46:16 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Tue, 04 Nov 2025 12:46:16 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Tue, 04 Nov 2025 12:46:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 04 Nov 2025 12:46:16 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 04 Nov 2025 12:46:16 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 04 Nov 2025 12:46:16 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 12:46:17 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 04 Nov 2025 12:46:17 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:ad0bc025a1766baba34dfa4dbb5713703de6595994d855ebf4689c0b161314ee`  
		Last Modified: Tue, 04 Nov 2025 00:20:17 GMT  
		Size: 29.8 MB (29837392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffc87d0d125756f6f7207ff00dd475820f1f662c1490e4f973570b5313e17fb6`  
		Last Modified: Tue, 04 Nov 2025 12:42:57 GMT  
		Size: 1.3 MB (1294636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ef7ffedbe0c72a7402c4c7ffa7ad05e05878b479406400dca12509798aee65e`  
		Last Modified: Tue, 04 Nov 2025 12:42:57 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:235f9a0ba0eb1a5da7986fb92d450451bc333572015535b1b763a366214e8b6b`  
		Last Modified: Tue, 04 Nov 2025 12:47:04 GMT  
		Size: 39.3 MB (39287395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e46ca528085c3652d506f94d3950096f37aeec2bac6827ae4ff7383b0116b3a`  
		Last Modified: Tue, 04 Nov 2025 12:47:00 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim` - unknown; unknown

```console
$ docker pull ruby@sha256:a27cc8802251533a2ff48c1c3005db00253018015fe782b03330ef5405088045
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2245583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3821bff904f3241a389a0830ba518fef5b724b5b7ca8a8c7f4ea8ad1af80f528`

```dockerfile
```

-	Layers:
	-	`sha256:45ea3b4fe82d2efc77de29b3ca7d6d05251d53e5ec29fffe74cd996e9422ea36`  
		Last Modified: Tue, 04 Nov 2025 15:57:55 GMT  
		Size: 2.2 MB (2221376 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6318891e1ff32694caa87777a26a029623b13f65c3795163c9a0de7bd734961f`  
		Last Modified: Tue, 04 Nov 2025 15:57:56 GMT  
		Size: 24.2 KB (24207 bytes)  
		MIME: application/vnd.in-toto+json
