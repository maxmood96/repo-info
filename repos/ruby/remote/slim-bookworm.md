## `ruby:slim-bookworm`

```console
$ docker pull ruby@sha256:f8cfcefee3122aed6bfad25d5d6dbad8cd3478fb2eacb5bf7e3b1010c16060f0
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

### `ruby:slim-bookworm` - linux; amd64

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
		Last Modified: Mon, 28 Apr 2025 21:08:01 GMT  
		Size: 28.2 MB (28227642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:500fab38b4fc9c5ad310cbe7cf60eaa8acd5059d067f48359c56bdb041215038`  
		Last Modified: Mon, 28 Apr 2025 22:07:28 GMT  
		Size: 3.5 MB (3499309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:956798033913b36e678f776731db94a64d1425011adef2eb2724361f4e3c2121`  
		Last Modified: Mon, 28 Apr 2025 22:07:28 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2fb3569a8b30e748c967d82769e74753f0784dcd7a8e232e64b1ad8b01df1a3`  
		Last Modified: Mon, 28 Apr 2025 22:07:29 GMT  
		Size: 41.4 MB (41354352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0fbf0c81f0cc84f490b75a243af01d371970efed13c68245152cb9c1f8d07a2`  
		Last Modified: Mon, 28 Apr 2025 22:07:28 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim-bookworm` - unknown; unknown

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

### `ruby:slim-bookworm` - linux; arm variant v5

```console
$ docker pull ruby@sha256:2297de9c23679209334140340d06e9dc236fc75e1b61a7159f53938c4a9e43f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.2 MB (68220741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9730a36ce9056c9cb29504de70887bdaaf3fd0feb9fe9a00aac31b522f02de1f`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1743984000'
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
	-	`sha256:bee0b90cda85f033e5343bbd7872c95c9de54d2dbe2fe864e9cb4b10716bc994`  
		Last Modified: Tue, 08 Apr 2025 00:23:07 GMT  
		Size: 25.8 MB (25757818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76da0305b2b23f80b1908c2ce6cdaee30c7f0a90503be88e1a607ebd5d8c65f1`  
		Last Modified: Tue, 08 Apr 2025 01:15:14 GMT  
		Size: 3.1 MB (3073460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4e679718b4a0a268971ab010660cfd8581d60c05d2e1f1f4dc104ef75227825`  
		Last Modified: Tue, 08 Apr 2025 07:55:02 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e595712bcdd9f04d1553868b2942240743633b089cf66225056cf143560917a2`  
		Last Modified: Mon, 14 Apr 2025 23:08:41 GMT  
		Size: 39.4 MB (39389129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e36a7118867fd72566424e176cbff7091fcea2e642270155e7c7c722ba90880`  
		Last Modified: Mon, 14 Apr 2025 23:08:40 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim-bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:3a3dae800ae3f8db86ac114fe8de15ea50f63cdaa760fd9dadee430acbca7866
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2512895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:152c977fd8f4a542d97b05a6f500d5deff307256ac3e5d1625123482d68b1353`

```dockerfile
```

-	Layers:
	-	`sha256:1a8da0abf29dd0fbd00bbc38756f27a9f8bf786b275c00f4d8964c7729015182`  
		Last Modified: Mon, 14 Apr 2025 23:08:40 GMT  
		Size: 2.5 MB (2488769 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98f4662db052d98620a42167b9fca0261281837793b9c70eb7194ca42530b5ce`  
		Last Modified: Mon, 14 Apr 2025 23:08:40 GMT  
		Size: 24.1 KB (24126 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:slim-bookworm` - linux; arm variant v7

```console
$ docker pull ruby@sha256:2cd63bbfc5fb8bfce6a9455add9b23b5dbd3d0d2a150c82a8e8b18e423e2725f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.9 MB (65907841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:522cecc99270b9281175e6a5cc197ea496d3d6b86f8c5acd2910b2f9384a9b68`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1743984000'
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
	-	`sha256:addc1be20d0979aa781d79a726ebf749adbc030186e63a44319274194e89cfa3`  
		Last Modified: Tue, 08 Apr 2025 00:23:15 GMT  
		Size: 23.9 MB (23937867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:428b9af88c849258200dfe951d2ab46f39e95311b0593488e6b7736531419708`  
		Last Modified: Tue, 08 Apr 2025 01:16:30 GMT  
		Size: 2.9 MB (2907779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1edb05d5531be9965f495a717a0b763b159ea3dde1cf0369a8d4ddfe247767d`  
		Last Modified: Tue, 08 Apr 2025 16:23:55 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3641ad3a58babc71e057ae6c353a545b41bda3ffcdae84404f9ab56587b49873`  
		Last Modified: Mon, 14 Apr 2025 23:22:48 GMT  
		Size: 39.1 MB (39061863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebb261f9238ec577be4cf71ec1f6f9a97de9d00f8df2ba4814ba74e8f679e2f9`  
		Last Modified: Mon, 14 Apr 2025 23:22:47 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim-bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:5784c4db9dafdd75d1dfb8939b7c0c159f224daf30b073af1b229ad3bd37a570
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2511622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a53507933ee9077ce7f38ee8dbe4da4b088c77fc2be35135f106d53cb70d149`

```dockerfile
```

-	Layers:
	-	`sha256:20d50b2b9e29a03b78f2f5fdec5a638f29afddaf73b95a589fdbd8382dc401b9`  
		Last Modified: Mon, 14 Apr 2025 23:22:47 GMT  
		Size: 2.5 MB (2487496 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d577efbeaeeed71903155b61e1571e43e65e9b2eab24eeed8f5f062ef1f6e437`  
		Last Modified: Mon, 14 Apr 2025 23:22:46 GMT  
		Size: 24.1 KB (24126 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull ruby@sha256:afd1e5f9496c324dcdaef73d82fb2bc333128ff677032c911d460d246696eb52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.9 MB (74911517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89af4b11c4ac0558a4f0c72052e53c91e1c402b134f9fc0bec54b096feaa2d74`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
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
	-	`sha256:16c9c4a8e9eef856231273efbb42a473740e8d50d74d35e6aedd04ff69fe161f`  
		Last Modified: Tue, 08 Apr 2025 00:23:04 GMT  
		Size: 28.1 MB (28066320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:770b59d5f4b7501214717c14396e0cb49ef7ca0c34466b78ae609a0d63339a56`  
		Last Modified: Wed, 09 Apr 2025 23:31:40 GMT  
		Size: 3.3 MB (3322881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:645dfe694d900e5d3be425b8114731e476433aa96dc43f5fb29f4abfe0653b30`  
		Last Modified: Wed, 09 Apr 2025 23:31:40 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7010733b9410cfe1be9a9ab045cd6c89448c583fd9b9a1c1312dd950f855490`  
		Last Modified: Mon, 14 Apr 2025 23:27:53 GMT  
		Size: 43.5 MB (43521982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:186527dcd9880aeefb352751824e6ec1a79c9a8dd5409c0fedab0a9181ae2470`  
		Last Modified: Mon, 14 Apr 2025 23:27:51 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim-bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:f657425e4c07f38418dc1b78c5cf082e732f1e291f8567860aab51703bea1a4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2509722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ac96749c4038a57ba2a373cab92fb612cc8aed1de79685627bbfd5b8250ecda`

```dockerfile
```

-	Layers:
	-	`sha256:6904a199f798f2177a922913523ef9cf99d5650eacdbb72d25df2ee71d448cd3`  
		Last Modified: Mon, 14 Apr 2025 23:27:52 GMT  
		Size: 2.5 MB (2485546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2eb10404cae92da2398f844c8fe46fe1257d9d16a85a2e197ee4b78ef583b4e3`  
		Last Modified: Mon, 14 Apr 2025 23:27:51 GMT  
		Size: 24.2 KB (24176 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:slim-bookworm` - linux; 386

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
		Last Modified: Mon, 28 Apr 2025 21:08:11 GMT  
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

### `ruby:slim-bookworm` - unknown; unknown

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

### `ruby:slim-bookworm` - linux; mips64le

```console
$ docker pull ruby@sha256:8d2599aa9efb39f6c0b9f904ca0a78ce513a92f0179cda210123873b66f668a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.0 MB (72036012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dd461039265eeb3f4b3d539ed16de8046a1017ba6a4fe96edd2cb0e23d3ba79`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1743984000'
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
	-	`sha256:c5170849255c666bce01dd02c1afbe442b1ecb682c342680d91dcd7cd477b57d`  
		Last Modified: Tue, 08 Apr 2025 00:23:28 GMT  
		Size: 28.5 MB (28513953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6949d2412d1813d925526134f33bbbd4b60e21f566ca57a9d89acc7ac2b8b0d6`  
		Last Modified: Tue, 08 Apr 2025 01:29:32 GMT  
		Size: 2.9 MB (2895366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8e1761691375b029d49a69b23d69d6c4ccd0af9a409bed5003b05a2f9386b2f`  
		Last Modified: Tue, 15 Apr 2025 00:11:05 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69394a46cbedefc017f1b9e5714e5d52f274bd01cebef2560c69fdc6029ce64f`  
		Last Modified: Tue, 15 Apr 2025 00:11:09 GMT  
		Size: 40.6 MB (40626359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:860a0972b052c6fa3d50938fdc1046c917ae29e79b837d9d1c2e5e2e6c04ae56`  
		Last Modified: Tue, 15 Apr 2025 00:11:05 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim-bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:ddee6319b0f0efe809e9f399492293fcd8b4a3786eda9f00ade576deb2ff447e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 KB (23874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8267673ddd3ea4fbc1f5a4ab17626780f777f007800119cc4a54b4f2392ae583`

```dockerfile
```

-	Layers:
	-	`sha256:d2abe2780a7ccaf548364355c50011fb332950a2218394ffba9e2dbb7d85329b`  
		Last Modified: Tue, 15 Apr 2025 00:11:05 GMT  
		Size: 23.9 KB (23874 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:slim-bookworm` - linux; ppc64le

```console
$ docker pull ruby@sha256:4efc412d556f136fc5b0aa4ab0a9953d3787b22a6afc6036cb475f36a9e8ed38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.1 MB (77060092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:828250aca6e32462beeaa6dca5683deb7cc0100a7f9b8bf4e44a1f7912f10cf8`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1743984000'
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
	-	`sha256:eda04574e09a8e08ba343dd01ac61bceb64282d2e992a997bd2102897b52d004`  
		Last Modified: Tue, 08 Apr 2025 00:23:44 GMT  
		Size: 32.1 MB (32068231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c6d12ecbe65638512a1c6d62e733b6280e655439e06aa1632c31da30928df79`  
		Last Modified: Wed, 09 Apr 2025 20:02:05 GMT  
		Size: 3.7 MB (3702900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31799ee43564a6794e70342c80c681ff206fcd610d1bff64cdb6c07f579a1b2c`  
		Last Modified: Wed, 09 Apr 2025 20:02:04 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ffaac4eba44e603e635f082d286e5fad888c03a67b1585dd287e980b496c024`  
		Last Modified: Mon, 14 Apr 2025 23:29:11 GMT  
		Size: 41.3 MB (41288627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d7b1ce41b940d2b9a9f4b64b17c7c13701735bd4f042407db3cda09a3a6edcf`  
		Last Modified: Mon, 14 Apr 2025 23:29:06 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim-bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:e7f1c38329d633c395b23e6cd27186c9fc43c29e86b2538ad414926619807ecf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2513613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d17d495bdcce8ce0a9748e483005c8542b5879619da3914e415e63b88267e453`

```dockerfile
```

-	Layers:
	-	`sha256:4560988bf9ba934fa3bdd0c8cb4f26b5bae38dc665b062c8d66f1fdf69b565be`  
		Last Modified: Mon, 14 Apr 2025 23:29:06 GMT  
		Size: 2.5 MB (2489561 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fcd572426241d66ff60839412ce23324702e4f64abb35a7bf3073426d027d60e`  
		Last Modified: Mon, 14 Apr 2025 23:29:06 GMT  
		Size: 24.1 KB (24052 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:slim-bookworm` - linux; s390x

```console
$ docker pull ruby@sha256:ec02a765a463aa139adf26ca9eedc7e4c6c8f563ebfb4ae911183ba3e4fce84d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.3 MB (70322223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ded386805c76f277146b96d9880d272fb6e1c5e36fa5b3ea7b077e21f9117375`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1743984000'
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
	-	`sha256:4d39bd57bcf7f4854587de5b4defd11e1b3b354bad1320b74c6994d07d7b3671`  
		Last Modified: Tue, 08 Apr 2025 00:24:14 GMT  
		Size: 26.9 MB (26884606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4eab93e0d63305db3d497c95992dbd3d14b93d5e0c2cbd97f4a8edfbb428aeb`  
		Last Modified: Wed, 09 Apr 2025 19:50:58 GMT  
		Size: 3.2 MB (3163370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88d6d57c9308909d37fe4ca9370b1a6830908cbc892f4a346e2bc4293cafcbc0`  
		Last Modified: Wed, 09 Apr 2025 19:50:58 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4e10083e50c1923ba56fdf01ae7725c4a3bfaad36f20353368cbf702ae2d327`  
		Last Modified: Mon, 14 Apr 2025 23:36:44 GMT  
		Size: 40.3 MB (40273913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b42c5357bd2ab0ff3ec924c9bfd8346426fb9c7baaa868a80fdad8096607c097`  
		Last Modified: Mon, 14 Apr 2025 23:36:44 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim-bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:9b2030240f217041279952173628d54a2d974cb452cccc114837c15778ad97f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2508942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf5fdef94cc283daad1b4a391058b87d01505710777c805c3ae72c9815d84240`

```dockerfile
```

-	Layers:
	-	`sha256:49f70bc085c2510799683f3864f3e04cabf15eab36b682cc0c8c83a739f4aaa2`  
		Last Modified: Mon, 14 Apr 2025 23:36:44 GMT  
		Size: 2.5 MB (2484963 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:616905a7722c78196cad9686a88ee2dcce09de3db8877e0a6cdb45af2aae22ef`  
		Last Modified: Mon, 14 Apr 2025 23:36:44 GMT  
		Size: 24.0 KB (23979 bytes)  
		MIME: application/vnd.in-toto+json
