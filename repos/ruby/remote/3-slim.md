## `ruby:3-slim`

```console
$ docker pull ruby@sha256:b0c5ea1354497817ed41091f6ee9cfe0cc1911286fa1a8077df1e5d61095e525
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

### `ruby:3-slim` - linux; amd64

```console
$ docker pull ruby@sha256:5cddead0b1e439fb53f6e35f50f5199ef62bf7e3d572a24b867ad6e609453264
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.2 MB (76174926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90bb4173194eebfe9fff7b147dff5a90abf16fd403a2d7851a5a627e93bb950f`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
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
	-	`sha256:8c7716127147648c1751940b9709b6325f2256290d3201662eca2701cadb2cdf`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 29.8 MB (29777766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24d8bdec960877d7ee206d2f15c47639759b95982311051584762eb2ce240574`  
		Last Modified: Wed, 08 Oct 2025 18:13:40 GMT  
		Size: 4.2 MB (4238635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1389fb9e5ae8d6da3d20eaf487829897c73321d17e1ab7e021648c8c10920373`  
		Last Modified: Wed, 08 Oct 2025 18:13:40 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:061fb72dc7059a4a75ce34cdebf796c32a399933add82b6c2d4e6c1c38504b39`  
		Last Modified: Wed, 08 Oct 2025 18:13:43 GMT  
		Size: 42.2 MB (42158193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df15fa3f48d05688e09699861cc15024f4e69279393ac93c3c64fccf042d7ada`  
		Last Modified: Wed, 08 Oct 2025 18:13:40 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-slim` - unknown; unknown

```console
$ docker pull ruby@sha256:d72ab4e6411fb93ad551381217925d46959cb091722d2a45de04a7979687f2b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2244181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9aaaec8dadb26a76db11463a0316826141be0fce44d3c4bf076fcd11d355de20`

```dockerfile
```

-	Layers:
	-	`sha256:03c008739f1d338904c04108346d6f68024613187bdce72bb2a8b2d4b6743e7c`  
		Last Modified: Wed, 08 Oct 2025 20:29:49 GMT  
		Size: 2.2 MB (2219931 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4bf71dcd842f8eeb05ba003fd5703ab137e2ad8cc254b85c6836c67033703ea`  
		Last Modified: Wed, 08 Oct 2025 20:29:50 GMT  
		Size: 24.2 KB (24250 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-slim` - linux; arm variant v5

```console
$ docker pull ruby@sha256:ff11b13d21e91d96aa78854b3f1783bd9ad39984144209353f4a12b4d0ea736a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.2 MB (67201669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c411e8c5577b7014d376f147e8ef34023ac08f9978a0c4a37da492685dce5586`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 07 Oct 2025 23:03:17 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1760918400'
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
	-	`sha256:389bac9f76fa529ccf801fd7c9cb260ecee27d208221c25004185ab22936c4d4`  
		Last Modified: Tue, 21 Oct 2025 00:20:45 GMT  
		Size: 27.9 MB (27946283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0dd4d3de6a90f8d0f5faef22f559002a749471358c16cf37594dc28fb467a91`  
		Last Modified: Tue, 21 Oct 2025 03:19:31 GMT  
		Size: 1.3 MB (1262887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:117ed1c5d0138a63fe137788b666a0178d9f4d5284aed97a3214cb9626c2980c`  
		Last Modified: Tue, 21 Oct 2025 03:19:31 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46bcf65780905045dcf3ed054acc5c607d0acf90eb8f66e81154d5753fe39803`  
		Last Modified: Tue, 21 Oct 2025 03:19:34 GMT  
		Size: 38.0 MB (37992168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4f3c22b548c2c045cc1122f62d8ab119ce62a999fa3057c0058e28574c519be`  
		Last Modified: Tue, 21 Oct 2025 03:19:31 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-slim` - unknown; unknown

```console
$ docker pull ruby@sha256:ba9ddb38590fe6a0514b27d0c1dbfb81417f8f8742fb4e196d6e31d2fbb1f412
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2247326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64fa2e96dbedb4bb7a5d70c4f17429dfa9d490de326982c8ed46be5f5f7dfb4d`

```dockerfile
```

-	Layers:
	-	`sha256:b03d718df8952e1596a1d767ebcac2f8b1e6a185fd74605f95404cb8f0273047`  
		Last Modified: Tue, 21 Oct 2025 05:57:34 GMT  
		Size: 2.2 MB (2222926 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5fcce16279f1477541857affc5bce31f1ed9a18acc543d32638c065019a93c43`  
		Last Modified: Tue, 21 Oct 2025 05:57:34 GMT  
		Size: 24.4 KB (24400 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-slim` - linux; arm variant v7

```console
$ docker pull ruby@sha256:500eaa8b9468fc11b27358ecc5437e13d263b5a4e33a903e917231d6d6077298
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.5 MB (67519071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c88ffb5ae3620ec07fa519f86b145b3e53dd11484e7c7dfa4090b87e808b611`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1759104000'
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
	-	`sha256:0289e98159900b326d4cedde367bf225e25835a3ad879647f17f922e43cfa884`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 26.2 MB (26212758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c5fbecbd8f232902b71916a7541260f3cde310a25622398e59750b43b8e2ecd`  
		Last Modified: Wed, 08 Oct 2025 18:12:37 GMT  
		Size: 3.4 MB (3441298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b769c3b83129100c7ebd332fbe227232d09b268fb20bf3d3a58afe3286f1d7`  
		Last Modified: Wed, 08 Oct 2025 18:12:37 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1700d41421ae5e2f474a9584e059b63c67c0c636fec7fe8f6fa54cf8dcee17f1`  
		Last Modified: Wed, 08 Oct 2025 18:12:40 GMT  
		Size: 37.9 MB (37864682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:293681702893ee9795b1b343e31d93a74ead52d58500c8ddb03d6d983a45c146`  
		Last Modified: Wed, 08 Oct 2025 18:12:37 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-slim` - unknown; unknown

```console
$ docker pull ruby@sha256:a5fead14b8ae5f86ce76fb4431e37ec760660ffc121e444a0ef52ce7ad8c2637
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2245768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45b7f6b2b472ca1349f906b3a7178c687a5bb731f49d8bf61cf447fa067f3bd6`

```dockerfile
```

-	Layers:
	-	`sha256:b80adc6795ba376374dd5ecbaa70f83add45bc1f87461da4bf72e051182d485a`  
		Last Modified: Wed, 08 Oct 2025 20:29:41 GMT  
		Size: 2.2 MB (2221367 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9adfbd3550003c849483d4f37d4884108c655e285c48581c0ce3da515dafeb03`  
		Last Modified: Wed, 08 Oct 2025 20:29:43 GMT  
		Size: 24.4 KB (24401 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-slim` - linux; arm64 variant v8

```console
$ docker pull ruby@sha256:509216f75b236f7fe08b5cf5abf69584fb96c113f01757be3be13ed5f13e9642
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.9 MB (76867510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d984ed8412f0393823cdaf35877edba871b1cbaf049e4b1fd7069cbc414ff0c`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1759104000'
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
	-	`sha256:e363695fcb930d5f18449254c0052117582c3de4263c91575b0a9040c986e412`  
		Last Modified: Mon, 29 Sep 2025 23:35:13 GMT  
		Size: 30.1 MB (30140842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26395651123655cda4d802c26b1f8140476e16d1a677f793c94e46e9a2c4e816`  
		Last Modified: Wed, 08 Oct 2025 18:15:06 GMT  
		Size: 4.6 MB (4580398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eebb7a9b5663ddefd8c81f14096634fc1f6335f6ceabab4ca5ef85ba31b1e8b`  
		Last Modified: Wed, 08 Oct 2025 18:15:04 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56190edec78a7b72ae72a5b588f64dabe3fbad052613aaaf6e5a3d593a585a96`  
		Last Modified: Wed, 08 Oct 2025 18:15:08 GMT  
		Size: 42.1 MB (42145937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:721e4c3729e66b852532b035ea342e7c27d33ec65788d08f5f0321083932146e`  
		Last Modified: Wed, 08 Oct 2025 18:15:04 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-slim` - unknown; unknown

```console
$ docker pull ruby@sha256:0e9b457022f5d3f0f4d31cbd778ab6bad44fda5e4132e8e7d1c76f1941f36ba6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2244686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08c927643f0b5bed0bd28ab204cb0b1265159df5c9bc776b1e29eead05af922d`

```dockerfile
```

-	Layers:
	-	`sha256:f4260e4c355a60051565a0a8f73ebd73f39ae947bb7c7cc3ab123d94a0f011f7`  
		Last Modified: Wed, 08 Oct 2025 20:29:46 GMT  
		Size: 2.2 MB (2220239 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:515d3b767ed8061dffe7353fdb20a9a5dd2416217141a4671149a88ce5485ec9`  
		Last Modified: Wed, 08 Oct 2025 20:29:47 GMT  
		Size: 24.4 KB (24447 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-slim` - linux; 386

```console
$ docker pull ruby@sha256:c4ea06fece8ff758199016536c0d2deaf7c782e765fa3aee30795cb63177666e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73211258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c51e678d2e8a6646728d8ed4c7878bead22dadec541137243d9577ee921dbfa7`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1759104000'
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
	-	`sha256:ab4c7760f4a4bda4b0797f3f0b56bd90b9778b76fc8351f2e1bd7c332b9dcc92`  
		Last Modified: Mon, 29 Sep 2025 23:35:33 GMT  
		Size: 31.3 MB (31294536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c38853ce4b0e208a9125060e0f456e14b3a9ab585922967532c7d59b6f77e5ab`  
		Last Modified: Wed, 08 Oct 2025 18:13:04 GMT  
		Size: 4.2 MB (4176773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f40a40417e96c0bf31059a28f05b62d7bbadffc1a9c5608fdab6cf1affc135bf`  
		Last Modified: Wed, 08 Oct 2025 18:13:04 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb6e211ff62ae87d57611cf475eab5282adc23aa930f995a3f33476752fde394`  
		Last Modified: Wed, 08 Oct 2025 18:13:07 GMT  
		Size: 37.7 MB (37739616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b52cb76b74cd5407c97bd9eaab20872f3dc3166eaf3d57a7139a921f390d2c67`  
		Last Modified: Wed, 08 Oct 2025 18:13:04 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-slim` - unknown; unknown

```console
$ docker pull ruby@sha256:760e075c117614ad34547fb6dc6cfad738a68e84771899510f7c61fa2eedfdad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2241296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e2b8d87902df94d25c40bada06345949208573acf3b3ab94a36793acf8075ef`

```dockerfile
```

-	Layers:
	-	`sha256:7ac77606eee9135802a206be8d22a36e9ad2d83680a8c393618ca0a51e4998d8`  
		Last Modified: Wed, 08 Oct 2025 20:29:40 GMT  
		Size: 2.2 MB (2217104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:257d969a8f4ed021d4264b81360b9c4128213e47bd4b99b7cb0de2fbf70fe9f5`  
		Last Modified: Wed, 08 Oct 2025 20:29:41 GMT  
		Size: 24.2 KB (24192 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-slim` - linux; ppc64le

```console
$ docker pull ruby@sha256:96d5d51fc4ff16f9e2054f14ab2f84a2d1116c6e13cb5a7ce7f16f7e53dc0ac3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.7 MB (77706291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4c34770d764830d8bc4fe57120fa3a4057884dfbe2abad44e5366581bd94d8a`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1759104000'
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
	-	`sha256:8bcecd3ced4047f6a4d35464fc2ee9b45e7fcc10b49690427794f4421b0552ab`  
		Last Modified: Mon, 29 Sep 2025 23:41:19 GMT  
		Size: 33.6 MB (33598454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:976752e1a563808e28225cd60d92e3bb6790e9808867767172b4309121eaa4de`  
		Last Modified: Wed, 08 Oct 2025 18:34:11 GMT  
		Size: 4.5 MB (4506224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4cea3fea55897793de99e882604e5227f8d308b3611254944e0978b42fd0a02`  
		Last Modified: Wed, 08 Oct 2025 18:34:09 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dddee654d8a14423bf04021346233f1ec931d1be3befe7b74e9ef5c007d3552`  
		Last Modified: Wed, 08 Oct 2025 18:34:20 GMT  
		Size: 39.6 MB (39601279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54d2a15cb239e606145ae050249a588d0a1de8632500feda3544978ed17e975e`  
		Last Modified: Wed, 08 Oct 2025 18:34:09 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-slim` - unknown; unknown

```console
$ docker pull ruby@sha256:91512fed5bfaac2a8cea7dfd9b163c0f84afcf38d713e1803f3e7cd8fe06ac0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2247807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:887fd16f1d3aae52feb676e044585568c0d5124e7b009c321bde428b558c8570`

```dockerfile
```

-	Layers:
	-	`sha256:c65aacdb188092403ccddcdfa8acb9423d94814593d11fd92c772daaa1e131d7`  
		Last Modified: Wed, 08 Oct 2025 20:29:46 GMT  
		Size: 2.2 MB (2223484 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7cb619ecb27fc050d07552db287371fe24089bea477cf877e0b3d055a647f194`  
		Last Modified: Wed, 08 Oct 2025 20:29:46 GMT  
		Size: 24.3 KB (24323 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-slim` - linux; riscv64

```console
$ docker pull ruby@sha256:9a088c697be47e41716b1c5fd20d2eb77b2587e9660a78f59affa900a0a31151
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.1 MB (70139106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:989c200bbfa67b50d46f4a337b692343f9c559f0328ad9880083fd0c83e4a9d9`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1759104000'
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
	-	`sha256:ecc6f9aec21fb94a493c2875c244e720a2f7c6c034063ce87b2f5b6b46962ec9`  
		Last Modified: Tue, 30 Sep 2025 01:05:14 GMT  
		Size: 28.3 MB (28275502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17cb807284daad75c5fa3695fef1d2d37861b8908199bc341ce4ea3d64611987`  
		Last Modified: Thu, 09 Oct 2025 00:41:45 GMT  
		Size: 3.9 MB (3861785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7712b4b26af05218185cf0ac46549fb825a44232f2916383d5dd7583ade75c66`  
		Last Modified: Thu, 09 Oct 2025 00:41:45 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af3bca0a2d50507123a93ca8c134e3c84d998f76a509095be909ddfbbe2c205a`  
		Last Modified: Thu, 09 Oct 2025 00:41:47 GMT  
		Size: 38.0 MB (38001485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ccf0232d6ce42f4796dbff677980604031cd8427b2c75a100c1593097164bfb`  
		Last Modified: Thu, 09 Oct 2025 00:41:45 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-slim` - unknown; unknown

```console
$ docker pull ruby@sha256:9ac8ab407a5f0ee4cf538973e7dbfecbacf67acfdb541b718e5ebec6fae194fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2238203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1057e00972d931b9b5659299d5d81bce9ebe5f3080f4c10047e9b361dcea1964`

```dockerfile
```

-	Layers:
	-	`sha256:fda2374817340cc527bb7dd1108801af2af3b1259e207931f656b6b73718b1b6`  
		Last Modified: Thu, 09 Oct 2025 02:57:38 GMT  
		Size: 2.2 MB (2213879 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab9da7cb266f8d81484ef04a06cc7c07032c6538c5c884f47c2c26d2dad8d947`  
		Last Modified: Thu, 09 Oct 2025 02:57:39 GMT  
		Size: 24.3 KB (24324 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-slim` - linux; s390x

```console
$ docker pull ruby@sha256:bfa436eb41ba16bbe47ea8bff027ad08579c56d62e551670b41af94738ec6038
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.5 MB (73496972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89dc841bbaee0958e24976a62a32ece94469c82c4daea64d8d2888db1d3a6860`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1759104000'
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
	-	`sha256:924b0740f35a15fc20142be5c392f6b033c8051daecf16d2db38c22d6d73eb53`  
		Last Modified: Mon, 29 Sep 2025 23:41:29 GMT  
		Size: 29.8 MB (29837230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13b94219bc2d3f6debe3a1214636652bb4296b7a0c6b41b51c442dbb55b247f6`  
		Last Modified: Tue, 30 Sep 2025 12:47:37 GMT  
		Size: 1.3 MB (1294331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:853d2a8514957d74c25bfc8f6b26ffb41866be42b94c7993401b21f8935aa8c4`  
		Last Modified: Tue, 30 Sep 2025 13:37:03 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f643f8d7858021a97f0967638ee5bcabf0d4351b2c38b20664203c2db9bf4681`  
		Last Modified: Wed, 08 Oct 2025 19:10:59 GMT  
		Size: 42.4 MB (42365078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dec945648ffcc1fed2409183ddc544cf232ac1c087af685ff7ee54c6060b972d`  
		Last Modified: Wed, 08 Oct 2025 18:23:24 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-slim` - unknown; unknown

```console
$ docker pull ruby@sha256:8e90461ea74acc26f083b592415bd2366255c09f14909f8136aa13ca0d07f9f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2245626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d8d9d94141ace8e9f401d5e8abc59244ec8c446ea2f378cc0e4a70712cc71d2`

```dockerfile
```

-	Layers:
	-	`sha256:a2e4f7c787166b75ca440854443b9a3ff264854b185610af67ca075755feee3a`  
		Last Modified: Wed, 08 Oct 2025 20:29:43 GMT  
		Size: 2.2 MB (2221376 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf81c67b183867fcdf50cb1d07e33c6892a4e4f6a841292d3e1276dd36726366`  
		Last Modified: Wed, 08 Oct 2025 20:29:44 GMT  
		Size: 24.2 KB (24250 bytes)  
		MIME: application/vnd.in-toto+json
