## `ruby:3-slim`

```console
$ docker pull ruby@sha256:7f13f26e3f0e74b2e618df5afd9d3de44b3eb62c3dfc40d017a5d2c9d9e9c5e5
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

### `ruby:3-slim` - linux; amd64

```console
$ docker pull ruby@sha256:3714737e7c4e3b530e5a402170ed188397ed704f5c1fbfd3aa5d189650760dab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.1 MB (73079964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75642bdadad8870f5d662fd680dd703d58da7d68f317d3f089657d2814a27726`
-	Default Command: `["irb"]`

```dockerfile
# Sat, 15 Feb 2025 00:00:36 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
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
	-	`sha256:8a628cdd7ccc83e90e5a95888fcb0ec24b991141176c515ad101f12d6433eb96`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 28.2 MB (28227259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05222832ecff9b17b18042824fb5693fbcd0ce05535b3c9c62d6f8a36547bbd0`  
		Last Modified: Tue, 08 Apr 2025 01:37:18 GMT  
		Size: 3.5 MB (3499309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8193de40f42b12c2aca16181a7081feb9ab5e5187fcd6fd4b289239f90ab6a76`  
		Last Modified: Tue, 08 Apr 2025 01:37:18 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f89cbb172f59f5287da0b5f9ecf02695e4066dfe512f47409b2192249412532`  
		Last Modified: Tue, 08 Apr 2025 01:37:19 GMT  
		Size: 41.4 MB (41353064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c37eee0a8c5b5e067a014ed346844a19f9f949c93e1cfc95e7e3ac7a058bb7e4`  
		Last Modified: Tue, 08 Apr 2025 01:37:18 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-slim` - unknown; unknown

```console
$ docker pull ruby@sha256:b902811b68bdc573884407b8ddaa76d2e15bb09c161e781b74f66887cd53b4ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2509219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:903a514f8a0b15f6c225833813ae378781eea7fae659eb062f21a469c6a1d186`

```dockerfile
```

-	Layers:
	-	`sha256:d3a5ead01abce177d1ffc895a5a2c1364d71caadcd70c6e155edd0c22d53b0b2`  
		Last Modified: Tue, 08 Apr 2025 01:37:18 GMT  
		Size: 2.5 MB (2485240 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b88ab821865c06bd462ae2bea3db27b1b62cff8212e4d51a5f4db200b389cf3`  
		Last Modified: Tue, 08 Apr 2025 01:37:18 GMT  
		Size: 24.0 KB (23979 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-slim` - linux; arm variant v5

```console
$ docker pull ruby@sha256:b51e0d38219c9facd43b2416ebd9610ed47980436d591681d5459e9bfaf37f89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.9 MB (65943578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c72273f27a443a5f5413732c1e68a8316a0480922397d557ad55ab11bd8348f`
-	Default Command: `["irb"]`

```dockerfile
# Sat, 15 Feb 2025 00:00:36 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1743984000'
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
	-	`sha256:43827b58858937700512f4f85bd9e1e47cd08063566d6ac2cec794d4573c0948`  
		Last Modified: Tue, 08 Apr 2025 07:55:04 GMT  
		Size: 37.1 MB (37111966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:669a9b48d2d4e7927ee60786301f66c0d396350fd2fb5388e2e6c8b0644bea24`  
		Last Modified: Tue, 08 Apr 2025 07:55:02 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-slim` - unknown; unknown

```console
$ docker pull ruby@sha256:86a439dc3fc28b6bbe9bc79b60bfd87f153bb08dc1f319687fe230a3f2aea407
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2512895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98f152160b113b3842abdebd8c0d54176afd17e158ed776739e0f70f1537ddb5`

```dockerfile
```

-	Layers:
	-	`sha256:ab825ce7132e66098d747ddca2e8cedbb310c0339476e1cb86fb12003d9809ba`  
		Last Modified: Tue, 08 Apr 2025 07:55:02 GMT  
		Size: 2.5 MB (2488769 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03a11f8d99d9b65045afe09c7ec8e70cbba82b8d3ea768707e0a23d0cd9a2c21`  
		Last Modified: Tue, 08 Apr 2025 07:55:02 GMT  
		Size: 24.1 KB (24126 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-slim` - linux; arm variant v7

```console
$ docker pull ruby@sha256:7c8e955cd33e121a88bc35313de240bdd0ba490faa2a146bda1ccb058a605bd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.8 MB (63760864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cbe1e6981a577ef6182b6b2211895fc5e03340ce27169a41ab37b3fe331a2a6`
-	Default Command: `["irb"]`

```dockerfile
# Sat, 15 Feb 2025 00:00:36 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1742169600'
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
	-	`sha256:676cf117f557880ff2e894692781cbce1b2a04502aff2e34b58c230b14731b8f`  
		Last Modified: Mon, 17 Mar 2025 22:18:43 GMT  
		Size: 23.9 MB (23915088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90de84afec6d4f313e7bf277c66cdcd6136876e4c4965613cc67e1980d1444fb`  
		Last Modified: Mon, 17 Mar 2025 23:43:15 GMT  
		Size: 2.9 MB (2907809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a73b798bb0e7139852833719de73453b77fd4d1365a02d6a7edbe7a1316b7dad`  
		Last Modified: Mon, 17 Mar 2025 23:43:15 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:024e00a021d6106a1678a30e886a8bed4ad1adea1d1370f7a0dd8a9370319fcb`  
		Last Modified: Tue, 18 Mar 2025 00:13:03 GMT  
		Size: 36.9 MB (36937635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d19a47a79f46c29b9d9a3c7f555107f4088e601dad2840fa0dab63fdb0e26cd`  
		Last Modified: Tue, 18 Mar 2025 00:13:02 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-slim` - unknown; unknown

```console
$ docker pull ruby@sha256:c717ea9ae9d6eca07e12a2e4b14adf8cb72922391425d88a462e5191bf3774ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2510286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14ccef9571862ab405d017e368ea1088393863d01240957a23ea85b10a86e80d`

```dockerfile
```

-	Layers:
	-	`sha256:d705c546ebd01764aba0b3da949d9bb04337c2d1b52b22a2d0b38df2817d0419`  
		Last Modified: Tue, 18 Mar 2025 00:13:02 GMT  
		Size: 2.5 MB (2486160 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:158d5c6cb94d1a52b641f894482943bf2ca868b539092ee1286cb068eaf4537a`  
		Last Modified: Tue, 18 Mar 2025 00:13:02 GMT  
		Size: 24.1 KB (24126 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-slim` - linux; arm64 variant v8

```console
$ docker pull ruby@sha256:ac0c82d5d5acf7eace78a4410465f8cfef2531790a5c8307c7b88f7195fe60b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.6 MB (72612051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f3296329801b4e03bc4c1f0d3126c0cc108a3b1e50edd8f9a2c52072a75e679`
-	Default Command: `["irb"]`

```dockerfile
# Sat, 15 Feb 2025 00:00:36 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
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
	-	`sha256:d9b6365477446a79987b20560ae52637be6f54d6d2f801e16aaa0ca25dd0964b`  
		Last Modified: Mon, 17 Mar 2025 22:17:34 GMT  
		Size: 28.0 MB (28044037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3f1f5b37bd6494f4c979734eddbf38ec3c9d650a090b347a2d957a8954d0749`  
		Last Modified: Tue, 18 Mar 2025 00:23:40 GMT  
		Size: 3.3 MB (3322905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb042444c12b759079305dd1cac7c315803bfb9f000bdc2b4e985de08a8419d1`  
		Last Modified: Tue, 18 Mar 2025 00:23:40 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca25bd205cdde8dff7cd43e4c8b21aef6acf0443738c2dd74a12a436be2a3a28`  
		Last Modified: Tue, 18 Mar 2025 00:33:19 GMT  
		Size: 41.2 MB (41244776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef392ccca3800d9543390d5b8c4848b3d4d2506206ca5213970cf3336e93e0dc`  
		Last Modified: Tue, 18 Mar 2025 00:33:18 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-slim` - unknown; unknown

```console
$ docker pull ruby@sha256:b585ef964f6ff6db91876016bb2dbd7a34bf29d3da51ee544e70e4cfa269c2e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2508386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:351416726ac174599fba6632853d0293ebe517ab92630ae0ab23cd39e15507a5`

```dockerfile
```

-	Layers:
	-	`sha256:1a7af144e06ef40157445337cafaf94893625d977cbd62a2494c5f775ac18a3a`  
		Last Modified: Tue, 18 Mar 2025 00:33:18 GMT  
		Size: 2.5 MB (2484210 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3bbf08db4efc52408fdfab8c95ac20d5a1580dd8bf30187383aa78e45ef676d`  
		Last Modified: Tue, 18 Mar 2025 00:33:18 GMT  
		Size: 24.2 KB (24176 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-slim` - linux; 386

```console
$ docker pull ruby@sha256:ec87c3812d22339f3bd61e1b20c1eb7cfa825e5db7398a0725393c6091433332
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.7 MB (69655405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7bf7eb696ceb394e5efb60eea851b3175cd16a993711d723e503228b19a74c6`
-	Default Command: `["irb"]`

```dockerfile
# Sat, 15 Feb 2025 00:00:36 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1743984000'
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
	-	`sha256:e4fab02059329179b6416bda7cdc389d26699f1c93a02194f146c047031c4748`  
		Last Modified: Tue, 08 Apr 2025 00:23:49 GMT  
		Size: 29.2 MB (29210731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:722853981e8471b1e6817748f3a6158833e8ee114544f7af88e7a903b8dcd661`  
		Last Modified: Tue, 08 Apr 2025 01:31:04 GMT  
		Size: 3.5 MB (3503380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ca419a7d4222f17f91cf6091a2afe51defb0aa8a35e8a7cf291dbfcb95802da`  
		Last Modified: Tue, 08 Apr 2025 01:31:04 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cbbf0145b1ddc891316758202af00242524de2e5105ae01b09a36c65e5d745d`  
		Last Modified: Tue, 08 Apr 2025 01:31:05 GMT  
		Size: 36.9 MB (36940961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:471d3d725dd04402621039538f6e813387aff850d571f6407eb7b46f799ee3a9`  
		Last Modified: Tue, 08 Apr 2025 01:31:04 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-slim` - unknown; unknown

```console
$ docker pull ruby@sha256:1972a2391d1a5979061fc8f9d2f5a76832d2e40f080eb8ac9639cb3b4869896f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2506280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a6e2b8799356a6c7cdee01671b667b8ab717957782ac6f9f22b92cd0ce50136`

```dockerfile
```

-	Layers:
	-	`sha256:e77fa43adf300a2cec1d2d493b622148111ff167663aba01e3948846524af935`  
		Last Modified: Tue, 08 Apr 2025 01:31:04 GMT  
		Size: 2.5 MB (2482360 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7641b4aa1cd7974109c24df7f44313160e8981d2f18e8decf0392ea85c75d45f`  
		Last Modified: Tue, 08 Apr 2025 01:31:04 GMT  
		Size: 23.9 KB (23920 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-slim` - linux; mips64le

```console
$ docker pull ruby@sha256:193fa44e55f6fd24079bbb8d29db8fa0442e3c47a8a411d028568eb301e44243
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.7 MB (69723791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02c1f4ffc5168b22490fc8a1d1fd05becd5126b0497b01c33e00d2a38a49a822`
-	Default Command: `["irb"]`

```dockerfile
# Sat, 15 Feb 2025 00:00:36 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1742169600'
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
	-	`sha256:18c44d6735d044d9bace3fdbe647c9b8187637683376f05d85dcb1185876721f`  
		Last Modified: Mon, 17 Mar 2025 22:19:04 GMT  
		Size: 28.5 MB (28489456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b514658a4f48245596c09f7112cb0f6884c0b1fa96bda139a946ab70038e2fe0`  
		Last Modified: Mon, 17 Mar 2025 23:20:58 GMT  
		Size: 2.9 MB (2895399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4293bb3eaab8701eb6621595b0af4ed6d4d4003d08faf4c3a6c80ba4d816d1ab`  
		Last Modified: Tue, 18 Mar 2025 00:21:23 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52fc3942df7e1f5c90331a975935262ea5cc08bd733542696811feb2bda5caf0`  
		Last Modified: Tue, 18 Mar 2025 02:04:56 GMT  
		Size: 38.3 MB (38338605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66d321bc8cc9d4780ff9d3fe1ac5c9287a7a2081e74822fc07c6c74308289b74`  
		Last Modified: Tue, 18 Mar 2025 02:04:53 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-slim` - unknown; unknown

```console
$ docker pull ruby@sha256:d670b3940e64cb0caf6a60f93484359589bc72aac98653aa613e42309a3ff775
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 KB (23875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dc31994ea84e318002c4eb9e98d6f168dda81da094ede8e3b9660797db14049`

```dockerfile
```

-	Layers:
	-	`sha256:5aeac523c594b3eb18f002169d21172fe7823e7c12ea86550200818997fb6323`  
		Last Modified: Tue, 18 Mar 2025 02:04:52 GMT  
		Size: 23.9 KB (23875 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-slim` - linux; ppc64le

```console
$ docker pull ruby@sha256:9b709cf59ed1a2923c3ee9d53459ea4fd95b2b6be025ba9899121bd81905a928
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.6 MB (74565347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66e853a9cdf9672d435667b01390500d68c2f72f5599cc9424d9d9bd7bee96cf`
-	Default Command: `["irb"]`

```dockerfile
# Sat, 15 Feb 2025 00:00:36 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1743984000'
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
	-	`sha256:eda04574e09a8e08ba343dd01ac61bceb64282d2e992a997bd2102897b52d004`  
		Last Modified: Tue, 08 Apr 2025 00:23:44 GMT  
		Size: 32.1 MB (32068231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42468877a74e57c50c11233c777cffdbaa83d62017691c314be00ed02fbee779`  
		Last Modified: Tue, 08 Apr 2025 01:19:17 GMT  
		Size: 3.7 MB (3702920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f5065fa57efae8ad889eb0ec7942e994d0544c22f59c33ef5cda5fc47622545`  
		Last Modified: Tue, 08 Apr 2025 07:19:40 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99ec3180956030ee555195d49e63e5934fdea975a8e0e2f865fc8271728a34f2`  
		Last Modified: Tue, 08 Apr 2025 07:19:41 GMT  
		Size: 38.8 MB (38793864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d807289e3f1c993d54fd4373ebf02a853a0005a69a9210f98f022e5a5771f61d`  
		Last Modified: Tue, 08 Apr 2025 07:19:40 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-slim` - unknown; unknown

```console
$ docker pull ruby@sha256:423d2bfc28b008765510382de90005258f06e4ebc774eac803b9c0cdd53dd27f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2513614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c22ddc7416da75919c7c15efc50b99aae31a8b12ee10c3e8dd964770a0a3c2ee`

```dockerfile
```

-	Layers:
	-	`sha256:b4e45e34233f2ab3140de4fdef4eeaa794ce31e430957782e7947bf07c890a33`  
		Last Modified: Tue, 08 Apr 2025 07:19:40 GMT  
		Size: 2.5 MB (2489561 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:687411a156f56aeabdd6fefae88803ecf7b4ecc89127132b1b40448a7119a62d`  
		Last Modified: Tue, 08 Apr 2025 07:19:40 GMT  
		Size: 24.1 KB (24053 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-slim` - linux; s390x

```console
$ docker pull ruby@sha256:635ffec364b903ebe151348fcd5d2cdd873af50c4abbc383fc05c50d9228421d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.0 MB (68022560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d02758c3eba6514826b83f3656ad2bbe20b218d5a90fce968da5f7daeb8375da`
-	Default Command: `["irb"]`

```dockerfile
# Sat, 15 Feb 2025 00:00:36 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1743984000'
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
	-	`sha256:4d39bd57bcf7f4854587de5b4defd11e1b3b354bad1320b74c6994d07d7b3671`  
		Last Modified: Tue, 08 Apr 2025 00:24:14 GMT  
		Size: 26.9 MB (26884606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b5390cf33ec28c798a2df11ec64efd7f989ab7db3d4d33d56e88209a2178b13`  
		Last Modified: Tue, 08 Apr 2025 01:15:45 GMT  
		Size: 3.2 MB (3163368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee68bcbce1342748889cb05bd536d8c1873092b88e16957dce203a7d188202c6`  
		Last Modified: Tue, 08 Apr 2025 06:12:23 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca6d4cc1085091b47a1a879fe44c700c329a44137e68f5c58a7c1362b29800c4`  
		Last Modified: Tue, 08 Apr 2025 06:12:24 GMT  
		Size: 38.0 MB (37974254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef4e2d960924c8619958978c4f4bde3d9f22333e70b667b1dfbb7a1629900b36`  
		Last Modified: Tue, 08 Apr 2025 06:12:23 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-slim` - unknown; unknown

```console
$ docker pull ruby@sha256:a8ca91f53a8c2a3ff124e3799ea5bd39482e82ed379520b5c82075023d7d3fa3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2508941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b027b5a2486d808601a44e9aaf3a7b3ee04e197aedc74e9ff95f7898849298f`

```dockerfile
```

-	Layers:
	-	`sha256:012265ac26791cabf5826a3a01c1ea39ee07d226c0171b142d0145440da4f622`  
		Last Modified: Tue, 08 Apr 2025 06:12:23 GMT  
		Size: 2.5 MB (2484963 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05306e8f1bc305e56b2e3ff28bd0b85ab8931e6566537d98ec223d4b95f46578`  
		Last Modified: Tue, 08 Apr 2025 06:12:23 GMT  
		Size: 24.0 KB (23978 bytes)  
		MIME: application/vnd.in-toto+json
