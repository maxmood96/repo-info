## `ruby:slim-bullseye`

```console
$ docker pull ruby@sha256:618749087525b97ac295c09c41941818b5425e6e2d474e3b7a65a887c4c44b37
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

### `ruby:slim-bullseye` - linux; amd64

```console
$ docker pull ruby@sha256:968e723b9d223a3bc581a6f54fe919d0f31db5ee17a3536d8c6e7b7030dab554
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.7 MB (72656144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b98eaea67e8d07c7a5605e6b28f5a8ccc240189008ccf494db3bea243a9bc81`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 14 Apr 2025 17:03:18 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1745798400'
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
	-	`sha256:c8e1eb8ab3b017bd9e33ddec83ebdd8292c542bbd14a8d5a6cfa2edc3ad3b8eb`  
		Last Modified: Mon, 28 Apr 2025 21:08:07 GMT  
		Size: 30.3 MB (30254604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fee95a2eef07b6b5aad432e8259b4e3214bd501f9eb7223a37c031709b5c5fff`  
		Last Modified: Mon, 28 Apr 2025 22:07:14 GMT  
		Size: 1.1 MB (1066582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7770ec40ef7fa53703f9d8324d29b52cd17a8b1e73e5d757b6edbcabee4919d3`  
		Last Modified: Mon, 28 Apr 2025 22:07:14 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac98f1af5a256d6cd6819d0bd44f330a389ace7fe1fcccc8254c1570fb04dfab`  
		Last Modified: Mon, 28 Apr 2025 22:07:15 GMT  
		Size: 41.3 MB (41334625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e8b21c97dcb3835c5fa9ac46a590406ebe37c25093479367d2b340c506a163e`  
		Last Modified: Mon, 28 Apr 2025 22:07:14 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim-bullseye` - unknown; unknown

```console
$ docker pull ruby@sha256:b046c7949c72f990ed4a237f6a01c22fd76cad31a03bcfbb1263981a6b2c0d70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2802773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34c8958482046440a993595628335b1319a66bd1f37e441cbd002f36bcf657a6`

```dockerfile
```

-	Layers:
	-	`sha256:a59fb35d9a890aab19940e4e063293200fe90fbd53f0e0fe17b8af8d9f39b167`  
		Last Modified: Mon, 28 Apr 2025 22:07:14 GMT  
		Size: 2.8 MB (2779979 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e27fbfb9d104cb20b2088fd822696fb5e696146c053282cd20587a458a1e683`  
		Last Modified: Mon, 28 Apr 2025 22:07:14 GMT  
		Size: 22.8 KB (22794 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:slim-bullseye` - linux; arm variant v7

```console
$ docker pull ruby@sha256:e46e7f2cb97a1eb0cd390b4a2d7a736750275ba31b9226da6e4c0d60f32e38b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.2 MB (63163673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff3a188eee4ada63108957bac850d9947adcd47155a7d1d62585143e247bced6`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1743984000'
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
	-	`sha256:bfc445187b87c4f640fe8b85c4ee3c251ce5e7023a5ff0acd053bde1f01e6aaf`  
		Last Modified: Tue, 08 Apr 2025 00:23:52 GMT  
		Size: 25.5 MB (25539135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19eb320086801f77003f5a012170eb7dfeedf82aa206b17a64d9c6a10d077a8a`  
		Last Modified: Tue, 08 Apr 2025 01:23:32 GMT  
		Size: 1.0 MB (1031393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f68439690c6230f261b0e96966bf856ede9f30f4fcaa005a921ebab6d358a750`  
		Last Modified: Tue, 08 Apr 2025 16:27:34 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28060383244e40d6c6eceadf75e00dc2305710e0f476f4ef9394b2a8eb8f7b10`  
		Last Modified: Mon, 14 Apr 2025 23:28:55 GMT  
		Size: 36.6 MB (36592813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3d8118fe0f9354a7558ba00627275c50a17274bfbaba35ee3f5177411ca65cc`  
		Last Modified: Mon, 14 Apr 2025 23:28:53 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim-bullseye` - unknown; unknown

```console
$ docker pull ruby@sha256:db1f9afd59b82f3ff1f8b8f48b5cc9b19519b9f2afa41b18a097c377c31a4508
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2805059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0da852493687b91093c0896ed4af7f9dd7b29830005730a034082313cf430fb`

```dockerfile
```

-	Layers:
	-	`sha256:2b22127a22c39697691b0ff875845d30f4cc67f2536327b5c8b36678d9f2c49c`  
		Last Modified: Mon, 14 Apr 2025 23:28:54 GMT  
		Size: 2.8 MB (2782149 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d08d19050ee541ef472b3555c48e8009617a1af5e3c99d3e6752d748ff7e1e41`  
		Last Modified: Mon, 14 Apr 2025 23:28:53 GMT  
		Size: 22.9 KB (22910 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull ruby@sha256:72236e480dcee155bd0ced059b35e4a9e658fb6ae1be9096fab15c82dcdc9070
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (70980700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ed88f6e27c0fc2e80ec2b56ff156ac46e2db08de3f035939c9b8bfacd1430f6`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1743984000'
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
	-	`sha256:59627ca2e9712141a7d131bec6c9931f8ecea11eac34d96bd1213ccea68e18e5`  
		Last Modified: Tue, 08 Apr 2025 00:23:35 GMT  
		Size: 28.7 MB (28749498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ce208c4d7f7a27ad6491e1c1f0bae29090ec7dd62082bf7d2571f0b857ea64a`  
		Last Modified: Wed, 09 Apr 2025 23:36:50 GMT  
		Size: 1.1 MB (1053897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e23c1ca94102e0fa683508f39c989715f6fb246600d4f4ab90b0b6fd9334df7`  
		Last Modified: Wed, 09 Apr 2025 23:36:50 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:924b674823f58b92eef2ca4a6af5beff65427a9a78a1a7493dc75ef6609f5816`  
		Last Modified: Mon, 14 Apr 2025 23:33:31 GMT  
		Size: 41.2 MB (41176973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25f49b5c82f167156bdd4bb81dc6874652d3b34c25b2b38a7e78916194863f62`  
		Last Modified: Mon, 14 Apr 2025 23:33:30 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim-bullseye` - unknown; unknown

```console
$ docker pull ruby@sha256:f86fe13c8ac4d509163cc6711c05116a9c28fab1f1a0381a53b5c221e95f9110
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2803121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07d1ec5d4fb847572af08a670ba53a4cec875168055068d3d154942352382f03`

```dockerfile
```

-	Layers:
	-	`sha256:8c6d8af0cecb8269518135e887c473442b07d21bb7b5f9eb0a493f745b31b44a`  
		Last Modified: Mon, 14 Apr 2025 23:33:30 GMT  
		Size: 2.8 MB (2780177 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f85a72978a3f9db8a96800b935ec2ec7b751953841cdb64eef447694d7b755ec`  
		Last Modified: Mon, 14 Apr 2025 23:33:30 GMT  
		Size: 22.9 KB (22944 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:slim-bullseye` - linux; 386

```console
$ docker pull ruby@sha256:e37ed5cd8014072f7adee8e302da1f8aa84ad444ff9bd24d87db3a2ebf7d354c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.0 MB (68955880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:831178632fd7b23e57a06d2a5de53fdcaac1e88f51db1233db8969e053c4b540`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 14 Apr 2025 17:03:18 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1745798400'
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
	-	`sha256:73bb1b80ecf1f8784ad6f92a35120b6e2306657fc7e8cbaedca1f45900f3d746`  
		Last Modified: Mon, 28 Apr 2025 21:08:07 GMT  
		Size: 31.2 MB (31187893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75eb3f2f4b251e34ee930f01858f726c1dfb62aa0e6adf2d662c34db7d307b01`  
		Last Modified: Mon, 28 Apr 2025 22:01:20 GMT  
		Size: 1.1 MB (1079103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fe3e5c2e4366f3beec14b5c1322642a9e43f125e6889c0236b44772504cf293`  
		Last Modified: Mon, 28 Apr 2025 22:01:20 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44bfef31663903caa72ea0a5b1981d33addc503dfc1545c62a0a2808f1f42a70`  
		Last Modified: Mon, 28 Apr 2025 22:01:22 GMT  
		Size: 36.7 MB (36688553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78b10f308e9d48d443713b1389879d0c0c582d9e8cda5d52f5cafcc8eeed8917`  
		Last Modified: Mon, 28 Apr 2025 22:01:20 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim-bullseye` - unknown; unknown

```console
$ docker pull ruby@sha256:6b842e05de03c983e49503a0a35fb530d8f18fb90a7fbfbf4d3bb3f11581eac0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2799865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cdf8984dedf5f55b9f02a970e620f0c9a1e7f4d7363d4d063347d5ccba007b2`

```dockerfile
```

-	Layers:
	-	`sha256:d3896555f274b76bec0bf1d96d0107f224d39f5ed1cc02ab4fe1293ce18d9fe4`  
		Last Modified: Mon, 28 Apr 2025 22:01:20 GMT  
		Size: 2.8 MB (2777108 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8490892f7aadf64f41710fdce9706765d0a47208ad4fb4631b42c052ce10f77e`  
		Last Modified: Mon, 28 Apr 2025 22:01:19 GMT  
		Size: 22.8 KB (22757 bytes)  
		MIME: application/vnd.in-toto+json
