## `ruby:slim-bullseye`

```console
$ docker pull ruby@sha256:4b3052bf45af5b5e00a900174a1885ee910065706b19c8280800168d9de8ea89
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
$ docker pull ruby@sha256:5e486751ba06bfbee2b1e0c8af41877bd5edc8358c00ad685f2f3eadab68e0dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.6 MB (72638734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1a354692ef7a22968dc1ae3dbbaf4fdbdbfb65232b7adf9897bfd877d42c7cc`
-	Default Command: `["irb"]`

```dockerfile
# Sat, 15 Feb 2025 00:00:36 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1743984000'
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
	-	`sha256:b983e127c643116d446fa1b64216f464e1d06a8bfaeeb8a895c361c1bc3f5652`  
		Last Modified: Tue, 08 Apr 2025 00:23:09 GMT  
		Size: 30.3 MB (30257419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f85214207197e84d04a143b8b21352a7ba827aa85e75627f9533211ce4ec7764`  
		Last Modified: Tue, 08 Apr 2025 01:36:59 GMT  
		Size: 1.1 MB (1066587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75eaae8168cb4025bca8a3fe25b5bf22029074d3d5ec3378d92aaa3d0d6855dc`  
		Last Modified: Tue, 08 Apr 2025 01:36:59 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a657fac1808da5bcea208d0d865c07e4590205836cd70c94b452dcb4fb78383`  
		Last Modified: Tue, 08 Apr 2025 01:37:00 GMT  
		Size: 41.3 MB (41314394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57f629130ce49a86d79e19a0e53512c8129650fddc1dad02e9b6d5f308ae76c5`  
		Last Modified: Tue, 08 Apr 2025 01:36:58 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim-bullseye` - unknown; unknown

```console
$ docker pull ruby@sha256:bc6736ff0574c375ef6b3083198a5d8e6c8a4cddc1c1758b44bad2c34258d7f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2802720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da8544b601dc04a8ad3e98a98e39a5fa18fdc9756d969fbbe849c226c9f7bd8f`

```dockerfile
```

-	Layers:
	-	`sha256:9e03da947bff5faa9ec1cddf8a0324c47b36b6b9c00681422f0ade465f89466b`  
		Last Modified: Tue, 08 Apr 2025 01:36:59 GMT  
		Size: 2.8 MB (2779925 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:712775498d54902abfcf7c7102e76846b6e49c6e88caf275c26900ce4e1fc51c`  
		Last Modified: Tue, 08 Apr 2025 01:36:59 GMT  
		Size: 22.8 KB (22795 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:slim-bullseye` - linux; arm variant v7

```console
$ docker pull ruby@sha256:892dda5539445acd2163c511e77ef91e6abc01108f105b21d184438ba50dbed3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.0 MB (62952746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:564d621c939a2d9b7f28e573139ebfb259652db6aa7c4ff06a6181f2842381b6`
-	Default Command: `["irb"]`

```dockerfile
# Sat, 15 Feb 2025 00:00:36 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1742169600'
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
	-	`sha256:3687c9079028ac9bf763326f4be55b4e440b37b5baf0c4529715d811c7ec1718`  
		Last Modified: Mon, 17 Mar 2025 22:19:22 GMT  
		Size: 25.5 MB (25535344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e1b84a4c6dfa975f9b9a00a9191986c8286ac1a1e809c62e462bcfa09dd7eb6`  
		Last Modified: Mon, 17 Mar 2025 23:38:12 GMT  
		Size: 826.3 KB (826309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:958c5f48658fefceb9301ce9c5cd7bab4ff309fdcfea18c532a37363d1dc9149`  
		Last Modified: Mon, 17 Mar 2025 23:38:11 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ac2f3a333c1ecaebb56d8b35b47b0fe5606e5a54d42628b33dc84e800c81047`  
		Last Modified: Tue, 18 Mar 2025 00:09:31 GMT  
		Size: 36.6 MB (36590761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9d3d50f9bcbc8eb9249023360982178cebd46d71becd690613947fe5f59e77c`  
		Last Modified: Tue, 18 Mar 2025 00:09:30 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim-bullseye` - unknown; unknown

```console
$ docker pull ruby@sha256:1fbc8ef4b24ae457f69d19a71b3ec883c5c2e11e036404563013695ee71d9570
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2803141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:534f71d9bb9b36243609dc03762e2c4ca6dca08fc0d92eaf6d28919b8fca4fe2`

```dockerfile
```

-	Layers:
	-	`sha256:db3eda5a6530f947bb607381ab2ee31d6157e0ab3b90f0cec4f04cb3ed282cc6`  
		Last Modified: Tue, 18 Mar 2025 00:09:31 GMT  
		Size: 2.8 MB (2780235 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af375cdc38ce16d5b2ada045220c0ef0a4127d5d2c38462c00cac41d10c4dd25`  
		Last Modified: Tue, 18 Mar 2025 00:09:30 GMT  
		Size: 22.9 KB (22906 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull ruby@sha256:74e16e960e04111f43f9c0f659770ddcf220b04cc2581258f54a6d035a8a9bec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.8 MB (70770248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae94242eec96d895252549c8b75073ef3dde44e1d9245409ed3075d91a65e150`
-	Default Command: `["irb"]`

```dockerfile
# Sat, 15 Feb 2025 00:00:36 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1742169600'
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
	-	`sha256:6eba8885c82049d690776150810f32585aca6c3eba49f692753434bdaee447ec`  
		Last Modified: Mon, 17 Mar 2025 22:18:52 GMT  
		Size: 28.7 MB (28745923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72bb39a688b2bde325907e5dacca2c6c104a084a7debae48fbe9bf1e59c07447`  
		Last Modified: Mon, 17 Mar 2025 23:39:08 GMT  
		Size: 849.8 KB (849775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26372531c18262dcecd69fedbe678c1eaed735323de2afbaba4e39187a765b25`  
		Last Modified: Mon, 17 Mar 2025 23:39:07 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca8a1d2666ebcd2f3d09e867e3fec422b7338c055510f90904aa393b4b8f0dd`  
		Last Modified: Tue, 18 Mar 2025 00:27:13 GMT  
		Size: 41.2 MB (41174217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfe2fb1e65af90acbc24ca386dde65e94e6a626c79d135d9106146d0389ca7ed`  
		Last Modified: Tue, 18 Mar 2025 00:27:12 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim-bullseye` - unknown; unknown

```console
$ docker pull ruby@sha256:7ec9f7de82ef99cf5c2adeef30c78d72b8247b9c3868d06b7ed71a584dda9221
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2801202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5d08fb65b932c5469e173e38f41c179fd65e06bce83a754aac95c68b4dfaa0d`

```dockerfile
```

-	Layers:
	-	`sha256:79821b23fc26e24039c6dfb50eb59ec0ab37f9d2b28b03944d84f0d5f295e149`  
		Last Modified: Tue, 18 Mar 2025 00:27:12 GMT  
		Size: 2.8 MB (2778263 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7beb9aad0b98d6d8acbe2c45505ee38230310a016b5826b01a453da7d7b899d6`  
		Last Modified: Tue, 18 Mar 2025 00:27:12 GMT  
		Size: 22.9 KB (22939 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:slim-bullseye` - linux; 386

```console
$ docker pull ruby@sha256:45e6389d1cb80a5fc98c3af33181343ad6baef5a8359644e7ec56192e27599d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.9 MB (68949421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:844a36a993fd18c30c26dc7a01bbeed90dbd403bc98149c563ffd0d874cb61e5`
-	Default Command: `["irb"]`

```dockerfile
# Sat, 15 Feb 2025 00:00:36 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1743984000'
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
	-	`sha256:c7f226a3ed9e3a783e859dc8479e50da2694130147ffb4885645e02664eedbec`  
		Last Modified: Tue, 08 Apr 2025 00:23:04 GMT  
		Size: 31.2 MB (31184573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9f0729a2b8fb28ad4a4bf0abf3a0ba5b448763cab55579de5f1a494b8e1b246`  
		Last Modified: Tue, 08 Apr 2025 01:30:49 GMT  
		Size: 1.1 MB (1079103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:526e48375840e6a9e2acb30b5927493c8abfc22402805b60970065296ea7f3dd`  
		Last Modified: Tue, 08 Apr 2025 01:30:49 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cbcc4b152c5298e6e4d550666dfe95ffbbb09753626fb984748bcc9ab7b3368`  
		Last Modified: Tue, 08 Apr 2025 01:30:50 GMT  
		Size: 36.7 MB (36685413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6db7923ec4b4582a4e60e59b48e393de5c53716a8aab33edf5c18976341bdea`  
		Last Modified: Tue, 08 Apr 2025 01:30:49 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim-bullseye` - unknown; unknown

```console
$ docker pull ruby@sha256:462a28f01631b83759bb329a86cdbaecfe50da3ed3cf31962a34a8682e671ae6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2799811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cba6a1c55206fdede65e839bc2c213a6274711fd8f2562ad8c68950bdcbd262c`

```dockerfile
```

-	Layers:
	-	`sha256:0642afe46e70203e4d5cb32771d23bb934452b6ecb5a5cd8db6e6a0194c71ed4`  
		Last Modified: Tue, 08 Apr 2025 01:30:49 GMT  
		Size: 2.8 MB (2777054 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c793ea26293e81e28e296cb0a7a61aa4661c8617fcf32338654f6a3a4956d5b3`  
		Last Modified: Tue, 08 Apr 2025 01:30:49 GMT  
		Size: 22.8 KB (22757 bytes)  
		MIME: application/vnd.in-toto+json
