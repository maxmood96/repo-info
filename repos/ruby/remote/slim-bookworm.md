## `ruby:slim-bookworm`

```console
$ docker pull ruby@sha256:d0ea0f5670ea624467618dd0e86a4ff274cefe46029b5086fb1c1058698dd9c2
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
$ docker pull ruby@sha256:5e7ef6d431fde561e27157d92103761bac8ecefb75db1c298d5eb524b84a6d85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.7 MB (80736055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52127ba92cfb05336028bff317046ca48eaf9119e31dca540a2053d663b46568`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 01:10:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 01:10:51 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 11 Jun 2026 01:13:12 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 01:13:12 GMT
ENV RUBY_VERSION=4.0.5
# Thu, 11 Jun 2026 01:13:12 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/4.0/ruby-4.0.5.tar.xz
# Thu, 11 Jun 2026 01:13:12 GMT
ENV RUBY_DOWNLOAD_SHA256=5dc5521ea54c726e6cc10b1b5a0f4004b27b482e61c04c99aed79315e30895e5
# Thu, 11 Jun 2026 01:13:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 		${rustArch:+--enable-zjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 11 Jun 2026 01:13:12 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 11 Jun 2026 01:13:12 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 11 Jun 2026 01:13:12 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:13:12 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 11 Jun 2026 01:13:12 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:b9136609bef0128191aa157637b98dd7b98e52154ca60c18258d65957a01c6d0`  
		Last Modified: Wed, 10 Jun 2026 23:39:54 GMT  
		Size: 28.2 MB (28237624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64e280d5a1dbd74ef72dd4bae186810e701acd33eb6779c04a5f9b33e4c508d7`  
		Last Modified: Thu, 11 Jun 2026 01:13:22 GMT  
		Size: 3.5 MB (3511609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da976689ca41e7ae38e57a6bb9fe8c168e37371fd2baf97a47d8ce65428f5253`  
		Last Modified: Thu, 11 Jun 2026 01:13:22 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c560666f2915053ba125692f098b5412e8f26ff745d87136b629a17cf2216c8`  
		Last Modified: Thu, 11 Jun 2026 01:13:24 GMT  
		Size: 49.0 MB (48986492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89287d1aece348447fd01e687e6e9826594df81c83650dbfa63d5deafc599b66`  
		Last Modified: Thu, 11 Jun 2026 01:13:22 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim-bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:f9836689473f0f8f958770ae258b3bfe37c517a9b2c6b3ff68657a86403beaa8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2620911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a97bb325dcbb650ddbf129d6c2c2cc6ad14cf207d236d848a8aee787122ca38`

```dockerfile
```

-	Layers:
	-	`sha256:765b4a33fb084d006a835b5ed2855dcc4bf6b089a1744d940b9418ab9a69d76e`  
		Last Modified: Thu, 11 Jun 2026 01:13:22 GMT  
		Size: 2.6 MB (2597707 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:199c73d1389a2c74d9559cfa79c6cfdc26eb06de891d264e9156e0bd21ecbd35`  
		Last Modified: Thu, 11 Jun 2026 01:13:22 GMT  
		Size: 23.2 KB (23204 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:slim-bookworm` - linux; arm variant v5

```console
$ docker pull ruby@sha256:1b37f29df2220125d6a9d83b4349503b795c47871115243f09b3592fef75b982
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.8 MB (70824261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1416a979db4fa1ecc5cf2b10a2c23834a54d09a92c43d969c0205b05b48f0fad`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 02:01:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 02:01:30 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 11 Jun 2026 02:04:17 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 02:04:17 GMT
ENV RUBY_VERSION=4.0.5
# Thu, 11 Jun 2026 02:04:17 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/4.0/ruby-4.0.5.tar.xz
# Thu, 11 Jun 2026 02:04:17 GMT
ENV RUBY_DOWNLOAD_SHA256=5dc5521ea54c726e6cc10b1b5a0f4004b27b482e61c04c99aed79315e30895e5
# Thu, 11 Jun 2026 02:04:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 		${rustArch:+--enable-zjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 11 Jun 2026 02:04:17 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 11 Jun 2026 02:04:17 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 11 Jun 2026 02:04:17 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 02:04:17 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 11 Jun 2026 02:04:17 GMT
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
	-	`sha256:fbe3d08e1e0f09d8c45b5cec6e988274bc02ce099e96d4f1f1b6149fa10d0cc4`  
		Last Modified: Thu, 11 Jun 2026 02:04:28 GMT  
		Size: 42.0 MB (41967029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9ed1c2aa8d7d2c5917fcca8cf553de22c65e41ac909385775220efbf09320a7`  
		Last Modified: Thu, 11 Jun 2026 02:04:26 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim-bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:9a97f1e596d081a35a224a436641ef98cfa33c8abd77dd95dc50c3a467405b8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2624835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea9e29c4daeea317a52db34619103a1dddab1915d12888b3b11f07a66188c18f`

```dockerfile
```

-	Layers:
	-	`sha256:3ad84d078b3b2f227d6dca879757663059724a42dab41937164932f1f7c58754`  
		Last Modified: Thu, 11 Jun 2026 02:04:27 GMT  
		Size: 2.6 MB (2601512 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de9af05f88c7ae2d71f55444228503de48fe1e10cffed3f92026890c75ffc62d`  
		Last Modified: Thu, 11 Jun 2026 02:04:27 GMT  
		Size: 23.3 KB (23323 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:slim-bookworm` - linux; arm variant v7

```console
$ docker pull ruby@sha256:ba83729babf941092d9d449034d7139ab8c0633e7d3774a5a95bc3414abd4dea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.6 MB (68639257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8b2dc7296e92778bec7f4dd8cd59c182f68b34addc1f91ae7ee3762d3c38efd`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 02:35:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 02:35:21 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 11 Jun 2026 02:37:55 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 02:37:55 GMT
ENV RUBY_VERSION=4.0.5
# Thu, 11 Jun 2026 02:37:55 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/4.0/ruby-4.0.5.tar.xz
# Thu, 11 Jun 2026 02:37:55 GMT
ENV RUBY_DOWNLOAD_SHA256=5dc5521ea54c726e6cc10b1b5a0f4004b27b482e61c04c99aed79315e30895e5
# Thu, 11 Jun 2026 02:37:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 		${rustArch:+--enable-zjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 11 Jun 2026 02:37:55 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 11 Jun 2026 02:37:55 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 11 Jun 2026 02:37:55 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 02:37:55 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 11 Jun 2026 02:37:55 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:8ae2378435d99f39097aa4fd0d6c58c08445becca3153d53205b2cc5054b09c2`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 23.9 MB (23944473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea34490219b93ddbe046ad072699df1458f6b49c650afe79a1f667a551e88442`  
		Last Modified: Thu, 11 Jun 2026 02:38:04 GMT  
		Size: 2.9 MB (2916020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47373302505fa6e445be7b669b880a700864da7667663df31dd6b5acb2ba6010`  
		Last Modified: Thu, 11 Jun 2026 02:38:04 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd5052270374da4f0f35ad60aed41bab5d3425509b5cd3409f732b6a126b5068`  
		Last Modified: Thu, 11 Jun 2026 02:38:06 GMT  
		Size: 41.8 MB (41778431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4903cfc2e890186e0da78d06b0989a558f521ca4023d89b2b4a3c4f2946ac618`  
		Last Modified: Thu, 11 Jun 2026 02:38:04 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim-bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:03895e2ccc43ec215ce00caa68af040709c32150aa70b4239bd3485dcbd64d2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2623254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f765e63b2d5309f174d606d10ecc11d30cb176c7454966886c5d2245b9d23141`

```dockerfile
```

-	Layers:
	-	`sha256:58c84143d6a3864ad546d47ae3ce8e59f7e55f2de9fc27a8ee788b58b482a09a`  
		Last Modified: Thu, 11 Jun 2026 02:38:05 GMT  
		Size: 2.6 MB (2599931 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:687351b6706d290301ab30d3a21bf0544e284aaa2a25d3e838b1f4a2ce2ccecd`  
		Last Modified: Thu, 11 Jun 2026 02:38:04 GMT  
		Size: 23.3 KB (23323 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull ruby@sha256:58592c575ccf1e9a7b70128608729969195543c368da8dc20d0a0fac2d97b5b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.2 MB (80187650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bb4c26391f832c9879237914a1384a61a92182e0d7d60584f9db88a13552c68`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 01:15:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 01:15:55 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 11 Jun 2026 01:18:20 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 01:18:20 GMT
ENV RUBY_VERSION=4.0.5
# Thu, 11 Jun 2026 01:18:20 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/4.0/ruby-4.0.5.tar.xz
# Thu, 11 Jun 2026 01:18:20 GMT
ENV RUBY_DOWNLOAD_SHA256=5dc5521ea54c726e6cc10b1b5a0f4004b27b482e61c04c99aed79315e30895e5
# Thu, 11 Jun 2026 01:18:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 		${rustArch:+--enable-zjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 11 Jun 2026 01:18:20 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 11 Jun 2026 01:18:20 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 11 Jun 2026 01:18:20 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:18:20 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 11 Jun 2026 01:18:20 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:402614bd39aaec1e4bdcf25aa67f88588fc8d93997a2551c4e130e6ed2b06c7a`  
		Last Modified: Wed, 10 Jun 2026 23:39:57 GMT  
		Size: 28.1 MB (28122307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7ff2176cec03b6d701e80876b28a362310e626e832457e10268b15f8683f30b`  
		Last Modified: Thu, 11 Jun 2026 01:18:31 GMT  
		Size: 3.3 MB (3344980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d10181aceef9e4719b6873ecdba41005a68473ec4aa27f8c5eaeb4ce78bebd0a`  
		Last Modified: Thu, 11 Jun 2026 01:18:30 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3a76ad1cc4ab72d9eb8c3eb6127f2a72783679fe3a10a9da94370f197936730`  
		Last Modified: Thu, 11 Jun 2026 01:18:32 GMT  
		Size: 48.7 MB (48720031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bba69b7a5df5f4140edcbedeaadd78aefcd9bcd4b0388a828d791219f698d2aa`  
		Last Modified: Thu, 11 Jun 2026 01:18:30 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim-bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:d2bd682781ecf1ca81e9c1722ae80f6d5cd548e24ccf8800e885895d71a24ec4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2621316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c1e3b0cf5e33d02143075e54125ec65f9857a084482da5fefbc53484ac84279`

```dockerfile
```

-	Layers:
	-	`sha256:98320e7f06395b869c2d5d881b326012f8c6ec087a32675e5991bf5a10001756`  
		Last Modified: Thu, 11 Jun 2026 01:18:30 GMT  
		Size: 2.6 MB (2597965 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d680436bb195ca4dd11e3668ed4c92f9570d1929fd9d6a752e70c5944a32ae9d`  
		Last Modified: Thu, 11 Jun 2026 01:18:30 GMT  
		Size: 23.4 KB (23351 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:slim-bookworm` - linux; 386

```console
$ docker pull ruby@sha256:e0b043ba8b1edd55f9e8c726bbafb0c6a07ee008773558fc89a5f831feff5d68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.5 MB (74503938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70ecd55f8c160f7e265ccafacbc29e8fc9a760ecf4c212568fc364598949ccff`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 01:10:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 01:10:47 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 11 Jun 2026 01:13:15 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 01:13:15 GMT
ENV RUBY_VERSION=4.0.5
# Thu, 11 Jun 2026 01:13:15 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/4.0/ruby-4.0.5.tar.xz
# Thu, 11 Jun 2026 01:13:15 GMT
ENV RUBY_DOWNLOAD_SHA256=5dc5521ea54c726e6cc10b1b5a0f4004b27b482e61c04c99aed79315e30895e5
# Thu, 11 Jun 2026 01:13:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 		${rustArch:+--enable-zjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 11 Jun 2026 01:13:15 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 11 Jun 2026 01:13:15 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 11 Jun 2026 01:13:15 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:13:15 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 11 Jun 2026 01:13:15 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:707460b758530d4476f3fefff30544db7cf8dbd98838ccc3533bc05e79016be4`  
		Last Modified: Wed, 10 Jun 2026 23:40:00 GMT  
		Size: 29.2 MB (29225762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:863671187a85176596b1ad7a0790edcbf73abf7a5557021c9018f58daef598dc`  
		Last Modified: Thu, 11 Jun 2026 01:13:24 GMT  
		Size: 3.5 MB (3515673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:256b8b6dfc2e61a7add166d8a22aed241e8538e014fcd4fb4fa3eab2fbab534b`  
		Last Modified: Thu, 11 Jun 2026 01:13:23 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22eb6ca24cefef6999d3d85495608f8ec5f291ffa4754f44b28f675c9cb8fb3f`  
		Last Modified: Thu, 11 Jun 2026 01:13:25 GMT  
		Size: 41.8 MB (41762169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:895d1001bb21aee79a298f6bc8285826589a4ffdb40e5dce5f93a90e27260aba`  
		Last Modified: Thu, 11 Jun 2026 01:13:24 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim-bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:f4df3d056e8e4383002e9613c861d9d0498fb40c8bc359318c8c89b912c191bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2618053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35bf85e39201817c17fc407b2c400b95b57dafffed59b9f18c07ae5bcf1bc96f`

```dockerfile
```

-	Layers:
	-	`sha256:77efd58a74e16803026775c0b3199d0eda8dcf6d569db41c39c848fa139b252e`  
		Last Modified: Thu, 11 Jun 2026 01:13:24 GMT  
		Size: 2.6 MB (2594888 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2155505aa07fa863778f25092a75f1dce8e967824ad208d6adfbe7f5335261c4`  
		Last Modified: Thu, 11 Jun 2026 01:13:23 GMT  
		Size: 23.2 KB (23165 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:slim-bookworm` - linux; mips64le

```console
$ docker pull ruby@sha256:3294687697d2c8bfd833315bda8243bef4e8b7e2404999b604a7bf482df41192
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.8 MB (74765011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:908999d2f648c9034dfd350b1810561333a42aa6f03788a8e3d15e8d17b2bef2`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 14:21:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 14:21:17 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 20 May 2026 23:08:46 GMT
ENV LANG=C.UTF-8
# Wed, 20 May 2026 23:08:46 GMT
ENV RUBY_VERSION=4.0.5
# Wed, 20 May 2026 23:08:46 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/4.0/ruby-4.0.5.tar.xz
# Wed, 20 May 2026 23:08:46 GMT
ENV RUBY_DOWNLOAD_SHA256=5dc5521ea54c726e6cc10b1b5a0f4004b27b482e61c04c99aed79315e30895e5
# Wed, 20 May 2026 23:08:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 		${rustArch:+--enable-zjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 20 May 2026 23:08:46 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 20 May 2026 23:08:46 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 20 May 2026 23:08:46 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 23:08:47 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 20 May 2026 23:08:47 GMT
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
	-	`sha256:858d96d6b0544128431ab91014439c2d429ecc3994907271eb2c75d78d24a62c`  
		Last Modified: Wed, 20 May 2026 23:09:31 GMT  
		Size: 43.3 MB (43338837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e9d24c17c41c11f3e06f1c50f57a1ec3c31153d9e812c6e3c4b8b967fe5a089`  
		Last Modified: Wed, 20 May 2026 23:09:26 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim-bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:41b758dcb8724ea337cbdd2a8c27d59ba379092c615244821224f45e43bec542
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 KB (23063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75c3ad1c26b0c48d48fa5758cf519aa0785771a41c619e04ff4d38ce9f17e951`

```dockerfile
```

-	Layers:
	-	`sha256:5aef128056e946e8f4a8bd74ebb6127953f2a79bd6dac4787a105d50154a8aa7`  
		Last Modified: Wed, 20 May 2026 23:09:26 GMT  
		Size: 23.1 KB (23063 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:slim-bookworm` - linux; ppc64le

```console
$ docker pull ruby@sha256:0a4fd765a45706dd74e5240446c700e0ffcd62e6db65e2ab8494222bf81a912d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.7 MB (79651783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a278dddcfb5d878e6017b855610b30ad3bf81ab73f526809bcc5692b8eabedbd`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 05:24:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 05:24:12 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 20 May 2026 18:18:50 GMT
ENV LANG=C.UTF-8
# Wed, 20 May 2026 18:18:50 GMT
ENV RUBY_VERSION=4.0.5
# Wed, 20 May 2026 18:18:50 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/4.0/ruby-4.0.5.tar.xz
# Wed, 20 May 2026 18:18:50 GMT
ENV RUBY_DOWNLOAD_SHA256=5dc5521ea54c726e6cc10b1b5a0f4004b27b482e61c04c99aed79315e30895e5
# Wed, 20 May 2026 18:18:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 		${rustArch:+--enable-zjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 20 May 2026 18:18:50 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 20 May 2026 18:18:50 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 20 May 2026 18:18:50 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 18:18:51 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 20 May 2026 18:18:51 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:562cecbb5aa529d280e58ef1f95f14cdcd37a90c5ea9181798a78377e934e6e7`  
		Last Modified: Tue, 19 May 2026 22:35:14 GMT  
		Size: 32.1 MB (32075742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a81b12a77e7a9477d1a105303d27254c73190734cf81bd973e9982e1cd74e60d`  
		Last Modified: Wed, 20 May 2026 05:28:33 GMT  
		Size: 3.7 MB (3714480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b806b18244dfeb41b537dd959921447ff02ac3ac393a23094c56954f83fa295a`  
		Last Modified: Wed, 20 May 2026 05:28:33 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4df9bea285c84afce3f4ea81480123b28e83cca01cb8d63e9c47e904aa551e2e`  
		Last Modified: Wed, 20 May 2026 18:19:10 GMT  
		Size: 43.9 MB (43861227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c393d4bde8829e458a5f73b47fc30322bf2d04b0cd3f39a83c82964565d68ed0`  
		Last Modified: Wed, 20 May 2026 18:19:09 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim-bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:4f8882a52f4c5dab54b9903c596c6d1091904ccbe93988345f06e73e6a7b4058
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2625334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2c9f26b886480a2c1c99b959f532497d7a11888496507ae198ffd03d599283f`

```dockerfile
```

-	Layers:
	-	`sha256:fa30c2f61fd12757ddaa297923c97d47a60cf0c268963374cb10898dd31435c3`  
		Last Modified: Wed, 20 May 2026 18:19:09 GMT  
		Size: 2.6 MB (2602080 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9920496b2c3d8c044b4b41ef15e4cc1db47a5cee7fbd0d503e722451ab11c98`  
		Last Modified: Wed, 20 May 2026 18:19:08 GMT  
		Size: 23.3 KB (23254 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:slim-bookworm` - linux; s390x

```console
$ docker pull ruby@sha256:911e1ab8749599f383c4f74208ab8e777463885e262c6528bce3252dc70b7cb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73160294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a7422505eef13198920ce272fd18f78b0a2005616f1d75cfaa8f34510ad9b21`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 02:57:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 02:57:11 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 11 Jun 2026 03:00:04 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 03:00:04 GMT
ENV RUBY_VERSION=4.0.5
# Thu, 11 Jun 2026 03:00:04 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/4.0/ruby-4.0.5.tar.xz
# Thu, 11 Jun 2026 03:00:04 GMT
ENV RUBY_DOWNLOAD_SHA256=5dc5521ea54c726e6cc10b1b5a0f4004b27b482e61c04c99aed79315e30895e5
# Thu, 11 Jun 2026 03:00:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 		${rustArch:+--enable-zjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 11 Jun 2026 03:00:04 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 11 Jun 2026 03:00:04 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 11 Jun 2026 03:00:04 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 03:00:04 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 11 Jun 2026 03:00:04 GMT
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
	-	`sha256:e64531c02cd98cfc811f77dcd63d7f933e54ada9aca32e3aeaecc272e7b79ca1`  
		Last Modified: Thu, 11 Jun 2026 03:00:21 GMT  
		Size: 43.1 MB (43092951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31e844ab99d415fa5d4553e1a35f03423c38b127a61bff670fe26a7eb2409131`  
		Last Modified: Thu, 11 Jun 2026 03:00:21 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim-bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:7881759b0c3dc00617fd6dbe7b06f31dd40d1dcdc32ca5940fd02a82e986eaa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2617742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fe26a944354d9e88ed249f3883a7ea01a17042c7aa18e7c8821e31165f2270e`

```dockerfile
```

-	Layers:
	-	`sha256:fc746bc0d2b9f36c988d6c2e54098d3a1cd5d4872e715024c70e67cae99014ca`  
		Last Modified: Thu, 11 Jun 2026 03:00:21 GMT  
		Size: 2.6 MB (2594538 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae1c1d52d06fde47d9f1eb9a3604b6ae75eb69e0f67864e91e0e48bfd2fc7d64`  
		Last Modified: Thu, 11 Jun 2026 03:00:20 GMT  
		Size: 23.2 KB (23204 bytes)  
		MIME: application/vnd.in-toto+json
