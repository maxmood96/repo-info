## `ruby:3-slim-bookworm`

```console
$ docker pull ruby@sha256:f5114779be5b8c771e02ae3564ba0410529526743027b14ea4e33738d8d16207
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
$ docker pull ruby@sha256:2cd4ea8138c8730fa87241672d37d85795a2095bf88fea69273be5b17b1b275e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73207085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5df56e92f2bef5279169cc773d67e4ffed0e0aa84bbc648ff872675981de56ee`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 01:11:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 01:11:46 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 11 Jun 2026 01:14:06 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 01:14:06 GMT
ENV RUBY_VERSION=3.4.9
# Thu, 11 Jun 2026 01:14:06 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Thu, 11 Jun 2026 01:14:06 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Thu, 11 Jun 2026 01:14:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 11 Jun 2026 01:14:06 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 11 Jun 2026 01:14:06 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 11 Jun 2026 01:14:06 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:14:06 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 11 Jun 2026 01:14:06 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:b9136609bef0128191aa157637b98dd7b98e52154ca60c18258d65957a01c6d0`  
		Last Modified: Wed, 10 Jun 2026 23:39:54 GMT  
		Size: 28.2 MB (28237624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33d49595e2fe1b7c4ac17618aae9b48619bc470838196d900f7464c2c0537106`  
		Last Modified: Thu, 11 Jun 2026 01:14:16 GMT  
		Size: 3.5 MB (3511577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ad0baa3d0549471ddbbd36e86577b3231bcb18e7832c04e32fbabd0e3fbb9d2`  
		Last Modified: Thu, 11 Jun 2026 01:14:16 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fc0c7153ad48d7e36a18e55c14f6c8394368c5f57a27dac9cc07a1a56d3c4e6`  
		Last Modified: Thu, 11 Jun 2026 01:14:17 GMT  
		Size: 41.5 MB (41457552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa6bd531f8d9b9f91bf1848411fcf817ee03d38260db1373357938cc00c833de`  
		Last Modified: Thu, 11 Jun 2026 01:14:16 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-slim-bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:b942b88319898f820d6d8fd3a1001790e9def65bdb125536dc8c48095282dd4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2624158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb5b474102e6244b717bb5aa09962185d319c4ed641017b79449a2646d13d0ac`

```dockerfile
```

-	Layers:
	-	`sha256:63ae6686e20e765c185de025bed2a867ba41fe5598d5b23f1301807ee0919e36`  
		Last Modified: Thu, 11 Jun 2026 01:14:16 GMT  
		Size: 2.6 MB (2601379 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21b3ed10e37cc37882ec0e5e5b26e76c99388485e20ae619eeaae951bc250721`  
		Last Modified: Thu, 11 Jun 2026 01:14:16 GMT  
		Size: 22.8 KB (22779 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-slim-bookworm` - linux; arm variant v5

```console
$ docker pull ruby@sha256:cdf00dcfca1d8412c8f255c0e2be481a77a309d37549ef15f0ae437fe4673f26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.1 MB (66062739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85671a01773f7b6a942a0ec14f685a8a5005b1540c0b4fad1bb1166a5dc45b6a`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 02:01:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 02:01:30 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 11 Jun 2026 02:07:20 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 02:07:20 GMT
ENV RUBY_VERSION=3.4.9
# Thu, 11 Jun 2026 02:07:20 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Thu, 11 Jun 2026 02:07:20 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Thu, 11 Jun 2026 02:07:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 11 Jun 2026 02:07:20 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 11 Jun 2026 02:07:20 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 11 Jun 2026 02:07:20 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 02:07:20 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 11 Jun 2026 02:07:20 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:99eb1512995af32b91c63bcd418e886af77e3c7ca088226161af558763425461`  
		Last Modified: Wed, 10 Jun 2026 23:38:28 GMT  
		Size: 25.8 MB (25773188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3abe6088a7d3a4cd829e06d86ff59f61bf265b6d7f03cabb29de31d0c2830bd8`  
		Last Modified: Thu, 11 Jun 2026 02:04:27 GMT  
		Size: 3.1 MB (3083712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b093f483e1346338159715e641f6f19a9d56cf46eb98664d39e3cf3c002c57b`  
		Last Modified: Thu, 11 Jun 2026 02:04:27 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb43d257e69294d02c56967da3e7c21d130e054b96970fdac525637daef511b8`  
		Last Modified: Thu, 11 Jun 2026 02:07:30 GMT  
		Size: 37.2 MB (37205508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6033558f4cf7e50e763401f8859b8a8d39089a5863d118f2832e766748c33f3d`  
		Last Modified: Thu, 11 Jun 2026 02:07:29 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-slim-bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:fcc28bf2e8ea91284b1dbb15a5b9e5d566221acd08c154f5f1b71360899d84a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2628066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:466fc1f09d994ffd4d9a1da88dc01b69e05ddd8dd90881cd39e3c4231afd204f`

```dockerfile
```

-	Layers:
	-	`sha256:cb0aea11f40c3fc5434458a249b7b64fad26b9c44ad23f74fb9d649ce9554af6`  
		Last Modified: Thu, 11 Jun 2026 02:07:29 GMT  
		Size: 2.6 MB (2605176 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb8477300b93118053f9d06595ea87b1f1f3e65a427f16b89a52b2db6e0ccb4c`  
		Last Modified: Thu, 11 Jun 2026 02:07:29 GMT  
		Size: 22.9 KB (22890 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-slim-bookworm` - linux; arm variant v7

```console
$ docker pull ruby@sha256:bc5ed119db308d5f61c2afa0497805bcdded316786c3293f48fce688891a785e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.9 MB (63889740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd57624947debfe31498727861cfdb143d358601e28452e1da0048d7367fa6c1`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 02:36:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 02:36:16 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 11 Jun 2026 02:38:46 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 02:38:46 GMT
ENV RUBY_VERSION=3.4.9
# Thu, 11 Jun 2026 02:38:46 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Thu, 11 Jun 2026 02:38:46 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Thu, 11 Jun 2026 02:38:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 11 Jun 2026 02:38:46 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 11 Jun 2026 02:38:46 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 11 Jun 2026 02:38:46 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 02:38:46 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 11 Jun 2026 02:38:46 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:8ae2378435d99f39097aa4fd0d6c58c08445becca3153d53205b2cc5054b09c2`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 23.9 MB (23944473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f0fd0a9e70bf08e20e01aab0a866eb6fa0a3eff2e135577d704da95f41528c3`  
		Last Modified: Thu, 11 Jun 2026 02:38:55 GMT  
		Size: 2.9 MB (2916000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cb34f6c7d42b25e687b1e4482b460f5e6430959c49f2f229f5dfdfe58abe9f5`  
		Last Modified: Thu, 11 Jun 2026 02:38:55 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf6f93940b4eb058b80d384b9b146eab4c30cfb399641b3cd4d5983399944a7d`  
		Last Modified: Thu, 11 Jun 2026 02:38:56 GMT  
		Size: 37.0 MB (37028935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa488898fb4820b90eddfbd339b6806958e7f5e390e31e0e185eeb334628ba46`  
		Last Modified: Thu, 11 Jun 2026 02:38:55 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-slim-bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:05a03a3507af2f9c81ed05d75ac5dd373f9051aa19f881d0ccd5f2c2c975b2d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2626485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5941a108e19b8039c285664014d40d7f8c21ba1011dd07e870397ba10e811df1`

```dockerfile
```

-	Layers:
	-	`sha256:41e8050cc01eade05f8bcf87e17a5ef7fd636886dc1e30d27aaf3ab6ea25f5d7`  
		Last Modified: Thu, 11 Jun 2026 02:38:55 GMT  
		Size: 2.6 MB (2603595 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c49d04d20b73551274649396d9adb8813a2b29a6e50eccc7eadde67724e21595`  
		Last Modified: Thu, 11 Jun 2026 02:38:55 GMT  
		Size: 22.9 KB (22890 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull ruby@sha256:4ab75e0c19f41dc9abc2379decf27f7c7da137defc06f093d887681e7e838015
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.8 MB (72814922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93fe4d24921c162e768c6f87db73b89bffe017ef7cc1a09f0b55ff0805611f69`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 01:16:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 01:16:18 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 11 Jun 2026 01:18:42 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 01:18:42 GMT
ENV RUBY_VERSION=3.4.9
# Thu, 11 Jun 2026 01:18:42 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Thu, 11 Jun 2026 01:18:42 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Thu, 11 Jun 2026 01:18:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 11 Jun 2026 01:18:42 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 11 Jun 2026 01:18:42 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 11 Jun 2026 01:18:42 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:18:42 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 11 Jun 2026 01:18:42 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:402614bd39aaec1e4bdcf25aa67f88588fc8d93997a2551c4e130e6ed2b06c7a`  
		Last Modified: Wed, 10 Jun 2026 23:39:57 GMT  
		Size: 28.1 MB (28122307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:062a6045ce8a5aa39e8bd272daf91859bdcdf0aa26b64c92ca2fe0f93dd5c45e`  
		Last Modified: Thu, 11 Jun 2026 01:18:51 GMT  
		Size: 3.3 MB (3345017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d5985cedded4ee0cc680e30faf4783a6a58f2b4958d193977ae25538457e97f`  
		Last Modified: Thu, 11 Jun 2026 01:18:51 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e2f26ddfa3b942b575593b0b0e0ec1f6fa2a67dddb30b82209895bb197f2f07`  
		Last Modified: Thu, 11 Jun 2026 01:18:53 GMT  
		Size: 41.3 MB (41347266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca3de76848de1eeb678fc4f1684bbb2354b2db06d2e6d317ce90c6d85a17ce04`  
		Last Modified: Thu, 11 Jun 2026 01:18:51 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-slim-bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:c15363e422158b087be839427fffe5dfaef982ff95eb44d65f2c1f9d4e90ad4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2624541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7367921d54dfce38d41732ef8516fcdb2cbc20f0f3931551134ea31f1bdb45bc`

```dockerfile
```

-	Layers:
	-	`sha256:7d69c2cd4df364b67434027b9eba56096fa90ce0db9ac332034b71645f255f39`  
		Last Modified: Thu, 11 Jun 2026 01:18:52 GMT  
		Size: 2.6 MB (2601625 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8917851b0ecf31b856d81e037bc0af1731fe43f7d625f3fc547110d2e767163e`  
		Last Modified: Thu, 11 Jun 2026 01:18:51 GMT  
		Size: 22.9 KB (22916 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-slim-bookworm` - linux; 386

```console
$ docker pull ruby@sha256:857a6e079f33a8582fb5a5fb7e5f0bf73e3c893dac23ff336e157b9aef882d94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.7 MB (69742951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fec36be90d22e240d034aa962b85e3f2377b8c982bafe1b7f0734f538054b16`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 01:12:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 01:12:03 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 11 Jun 2026 01:14:17 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 01:14:17 GMT
ENV RUBY_VERSION=3.4.9
# Thu, 11 Jun 2026 01:14:17 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Thu, 11 Jun 2026 01:14:17 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Thu, 11 Jun 2026 01:14:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 11 Jun 2026 01:14:17 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 11 Jun 2026 01:14:17 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 11 Jun 2026 01:14:17 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:14:17 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 11 Jun 2026 01:14:17 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:707460b758530d4476f3fefff30544db7cf8dbd98838ccc3533bc05e79016be4`  
		Last Modified: Wed, 10 Jun 2026 23:40:00 GMT  
		Size: 29.2 MB (29225762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e5e6abb96384506288727d8267de7a2ef639797917dfef344b486fcb6d8a232`  
		Last Modified: Thu, 11 Jun 2026 01:14:25 GMT  
		Size: 3.5 MB (3515697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b07abe2f7f82fdeafb0eb199787963e56459ecb331ab9778012bf0eeabe33d0`  
		Last Modified: Thu, 11 Jun 2026 01:14:25 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e019ba0fabea3d71fddd53dc0edc0190b8849553551c533bade5874e2221e7c9`  
		Last Modified: Thu, 11 Jun 2026 01:14:26 GMT  
		Size: 37.0 MB (37001161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17f386a7ab13d58307f169b212b0148777af006184e491ba44d0ab874ba33ad4`  
		Last Modified: Thu, 11 Jun 2026 01:14:25 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-slim-bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:3c442d5d8416e660b95c4f09558c4e45a9a9c2e049e9571352d9270cc7cfc842
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2621311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8291e341558cf318c2c46f2bedbe4542059fc5d4afbd0ca62fa5bb7fa91c9bb`

```dockerfile
```

-	Layers:
	-	`sha256:44816bb9e5167fd083f214dddf63fb33cb6f5da82cfae13b50792c5e42886a94`  
		Last Modified: Thu, 11 Jun 2026 01:14:25 GMT  
		Size: 2.6 MB (2598565 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80fe8fbdcd1d255a90e5ebde0715c115437c89842da8aa98bf908504e24c36c5`  
		Last Modified: Thu, 11 Jun 2026 01:14:25 GMT  
		Size: 22.7 KB (22746 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-slim-bookworm` - linux; mips64le

```console
$ docker pull ruby@sha256:f69ceb8584814defc6dfd181e842d52089eeab83fdb3f1f5ba9e11704c1c7fe8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.8 MB (69802745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27c288abd7a9a1ac96d0bd0bcd50115f146b0a4857a30c2b9f0650020e8aee8f`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 14:21:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 14:21:17 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 20 May 2026 14:53:17 GMT
ENV LANG=C.UTF-8
# Wed, 20 May 2026 14:53:17 GMT
ENV RUBY_VERSION=3.4.9
# Wed, 20 May 2026 14:53:17 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Wed, 20 May 2026 14:53:17 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Wed, 20 May 2026 14:53:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 20 May 2026 14:53:17 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 20 May 2026 14:53:17 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 20 May 2026 14:53:17 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 14:53:18 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 20 May 2026 14:53:18 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:83efaacc11aede9fdd3dcef1c025f5df70c81553b815dfb44caceaf1fa9eba75`  
		Last Modified: Tue, 19 May 2026 22:35:42 GMT  
		Size: 28.5 MB (28522504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db54ff127c571f0a7f84af643380bbfd3e487dc1f9ceed85b5edef1b9f464f25`  
		Last Modified: Wed, 20 May 2026 14:37:30 GMT  
		Size: 2.9 MB (2903336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30d1ded71d41c7ab52c35f8a4264ff441f39c4166204a85e0e909b3deeae4ad7`  
		Last Modified: Wed, 20 May 2026 14:37:30 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4acb5a1618436834b59f10917b74e551da6cd522cc97af842bb30f1da4378ba`  
		Last Modified: Wed, 20 May 2026 14:53:59 GMT  
		Size: 38.4 MB (38376571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67e13c9d6e69e8783f4adfbb51e3e4f44507b0a3cc96b3a30fdd98e12019756b`  
		Last Modified: Wed, 20 May 2026 14:53:54 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-slim-bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:be9a181d73e652ce64887455ed7d80a2610fb4da67593f11ec10e8e654c5ba3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.6 KB (22630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:475e49bd1144fe0e51f8280c8346c4a41c083f94da2ec5f608afb7c6ef63ea2a`

```dockerfile
```

-	Layers:
	-	`sha256:3c6b1c6b5774b2c590ec9942fb218bc77414e9cf1c8206a2b8984236500d7d81`  
		Last Modified: Wed, 20 May 2026 14:53:54 GMT  
		Size: 22.6 KB (22630 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-slim-bookworm` - linux; ppc64le

```console
$ docker pull ruby@sha256:25f8101713ac7f8fafbb892cacba772564d028d77692acefca58f0132d9c30a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74669114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db2a1499bb34af0a9715c540d164c3edd9a27ec6c524406b7baf7bbfa9d8bf96`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 08:56:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 08:56:58 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 11 Jun 2026 09:06:13 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 09:06:13 GMT
ENV RUBY_VERSION=3.4.9
# Thu, 11 Jun 2026 09:06:13 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Thu, 11 Jun 2026 09:06:13 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Thu, 11 Jun 2026 09:06:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 11 Jun 2026 09:06:13 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 11 Jun 2026 09:06:13 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 11 Jun 2026 09:06:13 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 09:06:14 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 11 Jun 2026 09:06:14 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:23f7cdee3ef2598b081c2b848fee95730a7ab2b1cc5b726c72dcb8c2fe3632f7`  
		Last Modified: Thu, 11 Jun 2026 00:21:33 GMT  
		Size: 32.1 MB (32081941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15466711d3753de1713178829f550ac2140e1eebc2849c5638785ac6448e3ef5`  
		Last Modified: Thu, 11 Jun 2026 09:01:23 GMT  
		Size: 3.7 MB (3714736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:697662ecaff146e4d7c4913b1a54b4a7c2167082ad193585dcc6687e428f394b`  
		Last Modified: Thu, 11 Jun 2026 09:01:23 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac3200d5498a986c6aea5343d1073e61fec76d69a180636fb6b7c96c383a6f8c`  
		Last Modified: Thu, 11 Jun 2026 09:06:32 GMT  
		Size: 38.9 MB (38872105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2da7610a71e639d86659deed14972e62d06510a9f5aa6e1192051fcb294b35d8`  
		Last Modified: Thu, 11 Jun 2026 09:06:31 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-slim-bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:d1bed44b20632a11dde31550844b02d0a1aab63caa493695b6861c7e4dd63f7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2628587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edc83fc20bda182493983e8c5ac3c7b4f4de56b6d26ddb5ca47e845b48e851a0`

```dockerfile
```

-	Layers:
	-	`sha256:b5ee3c0948b6a7e5f37b5f525586d36a4f8c98299801001083bebe1a4641aa6c`  
		Last Modified: Thu, 11 Jun 2026 09:06:31 GMT  
		Size: 2.6 MB (2605764 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:755c2171f9beaf309783f12e029679725b3dc79bbfbf7fd7fbad59e51a8d05c0`  
		Last Modified: Thu, 11 Jun 2026 09:06:30 GMT  
		Size: 22.8 KB (22823 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-slim-bookworm` - linux; s390x

```console
$ docker pull ruby@sha256:aab9f83be12b8610d542771a96bb060dea141b146344b8d858943885a21aa219
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.1 MB (68106707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a88229969a6f7bced1083f11e27852db6a1091f2dbbc4212add7ba204da7f63`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 02:57:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 02:57:11 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 11 Jun 2026 03:03:39 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 03:03:39 GMT
ENV RUBY_VERSION=3.4.9
# Thu, 11 Jun 2026 03:03:39 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Thu, 11 Jun 2026 03:03:39 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Thu, 11 Jun 2026 03:03:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 11 Jun 2026 03:03:39 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 11 Jun 2026 03:03:39 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 11 Jun 2026 03:03:39 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 03:03:39 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 11 Jun 2026 03:03:39 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:6483bebe0f30256cfdd9c6f96373508f6b33d18b4bc61668ee641c700aa3108a`  
		Last Modified: Wed, 10 Jun 2026 23:41:10 GMT  
		Size: 26.9 MB (26893508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af4255f2aa770b8c2c928556c08a259a57f10374e4bb062bdc630deb8da5e44f`  
		Last Modified: Thu, 11 Jun 2026 03:00:20 GMT  
		Size: 3.2 MB (3173504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c87660a4b35ed8010a9be224ff7cd6756d20af4b7c249896855a49bbe5620e1`  
		Last Modified: Thu, 11 Jun 2026 03:00:20 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9b830aef104641a581a831f4fe8fc4574541400e8981c7750447a250c416ee0`  
		Last Modified: Thu, 11 Jun 2026 03:03:54 GMT  
		Size: 38.0 MB (38039363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f918082772d7168a70d2d7870505b85e2156816a78559a38d02313e1fb7f86b2`  
		Last Modified: Thu, 11 Jun 2026 03:03:54 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-slim-bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:e4a1c2729c34bae229d26b45c2ff425b4b2a0e71f91edeac0fc7648dda167f85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2620989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8db576c28a728d16e3feeeaea6698618d3e829d1fde9b265129edb9be1a5f4e`

```dockerfile
```

-	Layers:
	-	`sha256:7578df63b7ba1ad464943efb303072d1ec5cbeac5282c457f7fc06801506ca4c`  
		Last Modified: Thu, 11 Jun 2026 03:03:54 GMT  
		Size: 2.6 MB (2598210 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62074dd6e9550eeb2e1f724e9cdcda03c2f78442ace92b395cdd54a583327dbc`  
		Last Modified: Thu, 11 Jun 2026 03:03:54 GMT  
		Size: 22.8 KB (22779 bytes)  
		MIME: application/vnd.in-toto+json
