## `ruby:4-bookworm`

```console
$ docker pull ruby@sha256:4ca45c63e012dd4ace6d74ef21192591994015a761a59b8b267cde348f937847
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

### `ruby:4-bookworm` - linux; amd64

```console
$ docker pull ruby@sha256:acd939dd237066a74ccb4b7947f40e57ada013b78c7f09a451d658341a726132
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **397.5 MB (397513102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f96f355964fcb1a67d067399ea47d0f8a3aebb07987b5f25fbde8edb6cb1925`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:37:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:24:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 00:19:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:20:10 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 17 Mar 2026 02:22:18 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 02:22:18 GMT
ENV RUBY_VERSION=4.0.1
# Tue, 17 Mar 2026 02:22:18 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/4.0/ruby-4.0.1.tar.xz
# Tue, 17 Mar 2026 02:22:18 GMT
ENV RUBY_DOWNLOAD_SHA256=0531fe57dfdb56bf591620d2450642ea0e0964f3512a6ebee7dc9305de69395f
# Tue, 17 Mar 2026 02:22:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 		${rustArch:+--enable-zjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 17 Mar 2026 02:22:18 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 17 Mar 2026 02:22:18 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 17 Mar 2026 02:22:18 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:22:18 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 17 Mar 2026 02:22:18 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:9d2f29087bcd6d99efd909a99095549425cd63e27c71b3bf37f108c6b7c370f9`  
		Last Modified: Mon, 16 Mar 2026 21:52:42 GMT  
		Size: 48.5 MB (48488584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26fa3468d221545a43d2151f3977695a31857f9342ba842627d03c9fa1b2ae02`  
		Last Modified: Mon, 16 Mar 2026 22:37:09 GMT  
		Size: 24.0 MB (24038304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cf051f1897bf7109af670b243c7791c62723fc1ebbfa516af2522da6c8c99a9`  
		Last Modified: Mon, 16 Mar 2026 23:25:05 GMT  
		Size: 64.4 MB (64395521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:505954b662451663b30768d461d6881e47bb272f6bc64e4d297f5cf79b9000cb`  
		Last Modified: Tue, 17 Mar 2026 00:20:24 GMT  
		Size: 211.5 MB (211529392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14ec4c5d20786d7fc263edae1a5f70793fd026dd7586beee1647398deb4c7ef2`  
		Last Modified: Tue, 17 Mar 2026 02:22:37 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4819a9804d4dd033bb90c964264633c1939e31888e1fabbab155206e59697d0`  
		Last Modified: Tue, 17 Mar 2026 02:22:38 GMT  
		Size: 49.1 MB (49060969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ce0d637de9ea02bcd68cb1a8efcfe8587cb32a7257a5ce691111a980dc5cdfb`  
		Last Modified: Tue, 17 Mar 2026 02:22:37 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:4-bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:9f90f69034b4f80bedfbd56a60b06700f0f6d19ccad139c05714d54b02fd3368
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (16003355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8a798f15de5476f507fb6222fceac27af6c42c661c6019699a43e4f82e6db50`

```dockerfile
```

-	Layers:
	-	`sha256:af717effbd2c3cf0d2f9b65c6c02f43189965f978f3a070ef0369b04b1435c0a`  
		Last Modified: Tue, 17 Mar 2026 02:22:37 GMT  
		Size: 16.0 MB (15981439 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16483c388686d419ea7e189d15ed3ed5072bd748caf52aae88b4082ef1429a26`  
		Last Modified: Tue, 17 Mar 2026 02:22:37 GMT  
		Size: 21.9 KB (21916 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:4-bookworm` - linux; arm variant v5

```console
$ docker pull ruby@sha256:0e82624c26131071f7077f8843a109a7caa37fcbc88aab483dbcca083af3de43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **357.6 MB (357604976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b80683a573bcfffb29ce34a6f74c42c97c06001daaae5d1d0d5d9931efe1380`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 23:16:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:08:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:18:16 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 04:37:01 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 17 Mar 2026 04:39:19 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 04:39:19 GMT
ENV RUBY_VERSION=4.0.1
# Tue, 17 Mar 2026 04:39:19 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/4.0/ruby-4.0.1.tar.xz
# Tue, 17 Mar 2026 04:39:19 GMT
ENV RUBY_DOWNLOAD_SHA256=0531fe57dfdb56bf591620d2450642ea0e0964f3512a6ebee7dc9305de69395f
# Tue, 17 Mar 2026 04:39:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 		${rustArch:+--enable-zjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 17 Mar 2026 04:39:19 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 17 Mar 2026 04:39:19 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 17 Mar 2026 04:39:19 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 04:39:19 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 17 Mar 2026 04:39:19 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:a889e82787049133d77ffad9b735ec4a592f071dd0e1873ff586ba91994e03fb`  
		Last Modified: Mon, 16 Mar 2026 21:51:55 GMT  
		Size: 46.0 MB (46021486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1a2ee884acc42f13388cd68befd38ba7c8e48ff32ebffc04bc5ff13735cd047`  
		Last Modified: Mon, 16 Mar 2026 23:16:33 GMT  
		Size: 22.7 MB (22713788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d9a7ffdc9dcaed1952881119614bd002f2a5fee9ea4f873345f94e374aee1d1`  
		Last Modified: Tue, 17 Mar 2026 01:08:47 GMT  
		Size: 62.0 MB (62008826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:720cfe4e1a6c516451ce3d3a12001bb932d9c5e2c070a0568c3e00188ebd94f6`  
		Last Modified: Tue, 17 Mar 2026 02:18:53 GMT  
		Size: 184.8 MB (184788403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbd15f32ec0cf193650b98f650c3248a7f6514349847968efc215fed0f8a49cc`  
		Last Modified: Tue, 17 Mar 2026 04:39:38 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2be32a651b6a595581273bcd070eb8e1d062244b7dbba183fef13b97d973676e`  
		Last Modified: Tue, 17 Mar 2026 04:39:40 GMT  
		Size: 42.1 MB (42072141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf6f73657d410e9147c0b110ca761769e2d2051e4d1c68dbe3b2906a041472a9`  
		Last Modified: Tue, 17 Mar 2026 04:39:38 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:4-bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:004a849896a1928cbd8d1e6d1a46f34c8c819d517e100d620c522bee4231d964
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.8 MB (15800461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34647016bedcde0cd206dbdf34514f8c7709867c8c1e6518c2547bb803763ea5`

```dockerfile
```

-	Layers:
	-	`sha256:a4bc6bbe89e638b6ffd478757196cfdc29921bc0fcf4cf980d3cb5353ad277b4`  
		Last Modified: Tue, 17 Mar 2026 04:39:39 GMT  
		Size: 15.8 MB (15778439 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:129f3ad9aa067d83cd3061b4c3fcde8f38af2d5ffba6d805ef105480a96b1f4b`  
		Last Modified: Tue, 17 Mar 2026 04:39:38 GMT  
		Size: 22.0 KB (22022 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:4-bookworm` - linux; arm variant v7

```console
$ docker pull ruby@sha256:1f64c0362d93dc0068a9ec2b821516c358045909cc2e63183169c45db6ba934f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.1 MB (343115163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3f817611b41c22e97e08701ffae64c3b81afa84f84715098145e8494f65a8f3`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 23:18:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 00:51:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:15:28 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:37:50 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 17 Mar 2026 02:39:59 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 02:39:59 GMT
ENV RUBY_VERSION=4.0.1
# Tue, 17 Mar 2026 02:39:59 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/4.0/ruby-4.0.1.tar.xz
# Tue, 17 Mar 2026 02:39:59 GMT
ENV RUBY_DOWNLOAD_SHA256=0531fe57dfdb56bf591620d2450642ea0e0964f3512a6ebee7dc9305de69395f
# Tue, 17 Mar 2026 02:39:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 		${rustArch:+--enable-zjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 17 Mar 2026 02:39:59 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 17 Mar 2026 02:39:59 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 17 Mar 2026 02:39:59 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:40:00 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 17 Mar 2026 02:40:00 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:3e574dbe918dfcf76ab4fd7736cc3c62e552f2465f49a512ed26cfc623807024`  
		Last Modified: Mon, 16 Mar 2026 21:56:33 GMT  
		Size: 44.2 MB (44207568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab92577caba10dd52b0a4a93a140b02839815621e1e55d6eef1c846ec1932e81`  
		Last Modified: Mon, 16 Mar 2026 23:18:55 GMT  
		Size: 21.9 MB (21942056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c259f98025fcc3d44333815b426fe9bea34608d38b537248297aff1482d389`  
		Last Modified: Tue, 17 Mar 2026 00:51:25 GMT  
		Size: 59.7 MB (59652088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9200d3b121f4de1ac4dca30995995f1d7ba9452339fd7ac2494bda683c4f5df5`  
		Last Modified: Tue, 17 Mar 2026 01:16:02 GMT  
		Size: 175.4 MB (175431210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7d6c8b1d3ed02b22adde87606650ba1a2d5ab5bc9a66221eadcdd4ec83865cb`  
		Last Modified: Tue, 17 Mar 2026 02:40:18 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c6d9076fd69efbdbcc336f27be893b7e92ab04552231d3efb0a843172cc57e1`  
		Last Modified: Tue, 17 Mar 2026 02:40:20 GMT  
		Size: 41.9 MB (41881910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef5a2035c31e42a9ecc01a3ee897eb9577c706a51513ed7b1661dd41dc9b47f9`  
		Last Modified: Tue, 17 Mar 2026 02:40:18 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:4-bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:10b4004cfdda7f1fe5e52ce8b41ab3be7c8227a9df08baf9bc15c03f56c30203
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.8 MB (15805937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfd0961f8b6b7270d3ae4174a07b87e9339452ef81b1b3d1a8bef3dca9d92292`

```dockerfile
```

-	Layers:
	-	`sha256:2081161ac472260b7a5c21165147b0787e9ffe8bcd934aaa69966d468bacfd0d`  
		Last Modified: Tue, 17 Mar 2026 02:40:19 GMT  
		Size: 15.8 MB (15783915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe261365d351d7730d9921be89cce2fdecc9cedfc755d70e2ed0a99c0e6c99bc`  
		Last Modified: Tue, 17 Mar 2026 02:40:18 GMT  
		Size: 22.0 KB (22022 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:4-bookworm` - linux; arm64 variant v8

```console
$ docker pull ruby@sha256:f5d9b81236cb9502f97a5ec587c575cefcdbed1905477386702f9bc203502392
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **388.3 MB (388349517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f40dff2d4412e2600aafe3b8174e44f4e203d4117865f3aea4bded1d2143ae3`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:39:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:30:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 00:19:50 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:26:30 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 17 Mar 2026 02:28:39 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 02:28:39 GMT
ENV RUBY_VERSION=4.0.1
# Tue, 17 Mar 2026 02:28:39 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/4.0/ruby-4.0.1.tar.xz
# Tue, 17 Mar 2026 02:28:39 GMT
ENV RUBY_DOWNLOAD_SHA256=0531fe57dfdb56bf591620d2450642ea0e0964f3512a6ebee7dc9305de69395f
# Tue, 17 Mar 2026 02:28:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 		${rustArch:+--enable-zjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 17 Mar 2026 02:28:39 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 17 Mar 2026 02:28:39 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 17 Mar 2026 02:28:39 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:28:40 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 17 Mar 2026 02:28:40 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:2ea98bb5eec9d02a0d7b59638c683db4e1e749f998a317bc731e9506f8480b12`  
		Last Modified: Mon, 16 Mar 2026 21:52:02 GMT  
		Size: 48.4 MB (48373032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efbce225727d69d170353500d8834770da849cbdcea48de37e492fe14ef880d0`  
		Last Modified: Mon, 16 Mar 2026 22:39:28 GMT  
		Size: 23.6 MB (23604701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bda59add442110ab916af1231a98d110e965b9b107829a3f0920d6789fa955d0`  
		Last Modified: Mon, 16 Mar 2026 23:30:22 GMT  
		Size: 64.5 MB (64479442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a8feb033ce1635588aeb9a2f147293a6c61823ffee25286cf2fe9a0da9e069c`  
		Last Modified: Tue, 17 Mar 2026 00:20:30 GMT  
		Size: 203.1 MB (203069864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:510c265233f1282816eb203fbdfc72d03ba853575ae207a0ceb9059baa801277`  
		Last Modified: Tue, 17 Mar 2026 02:29:00 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c6c69d682d462f1e4c05f9fed6ffea11c293cb54c1cd7839de97058bb5bec2e`  
		Last Modified: Tue, 17 Mar 2026 02:29:01 GMT  
		Size: 48.8 MB (48822145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:776433808a8aad211d1b6c8e8889d21497fe37a80e1c0ac83653289456b5252f`  
		Last Modified: Tue, 17 Mar 2026 02:29:00 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:4-bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:c19a467eb8d291e7ffd0a154970ac9c7766493180ba18a74d580464e17e30bb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (16032015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:953e2a6585cd0937127084cf0645f14e262ea02038e87f2e142ba530ea1c6fbe`

```dockerfile
```

-	Layers:
	-	`sha256:be287203f45a9cd279f25d3a7daec59fd0172bc1e957ccd403ba5d414f652ab5`  
		Last Modified: Tue, 17 Mar 2026 02:29:01 GMT  
		Size: 16.0 MB (16009965 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f689d2fa7ae299c85c7a5be79b017b393e62029241732b384b045ae87925d937`  
		Last Modified: Tue, 17 Mar 2026 02:29:00 GMT  
		Size: 22.1 KB (22050 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:4-bookworm` - linux; 386

```console
$ docker pull ruby@sha256:7fabdf94894b10e345a07394ef4f4f52a615d0e4b43fbc7fa8b9bbc06ded99a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **392.9 MB (392883501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:047f86b3e44e3f3633945fb5db629ae3b129e3bc61e1f7a3333ac1deb7d89db1`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:43:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:41:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 00:19:36 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:40:40 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 17 Mar 2026 01:42:31 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 01:42:31 GMT
ENV RUBY_VERSION=4.0.1
# Tue, 17 Mar 2026 01:42:31 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/4.0/ruby-4.0.1.tar.xz
# Tue, 17 Mar 2026 01:42:31 GMT
ENV RUBY_DOWNLOAD_SHA256=0531fe57dfdb56bf591620d2450642ea0e0964f3512a6ebee7dc9305de69395f
# Tue, 17 Mar 2026 01:42:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 		${rustArch:+--enable-zjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 17 Mar 2026 01:42:31 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 17 Mar 2026 01:42:31 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 17 Mar 2026 01:42:31 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 01:42:31 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 17 Mar 2026 01:42:31 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:400234fd447028a685a307ac0360522f0cd83d85515ddb6a2bf38049ebfe1f8f`  
		Last Modified: Mon, 16 Mar 2026 21:53:35 GMT  
		Size: 49.5 MB (49477654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ed7cf39578e27046e7ba7fa5d4d45df198790a004a9eb86583e977b3b055c88`  
		Last Modified: Mon, 16 Mar 2026 22:43:53 GMT  
		Size: 24.9 MB (24871994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73d9d2da3801adad27eefa73bb7b5ab6c0c94f46583823a923caa8e9b995a97b`  
		Last Modified: Mon, 16 Mar 2026 23:41:39 GMT  
		Size: 66.2 MB (66234305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b28332827a450f227b37bf43cea8589364d96cbbc006b009e7d22789f013ded4`  
		Last Modified: Tue, 17 Mar 2026 00:20:17 GMT  
		Size: 210.5 MB (210473623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a18dd5d2bc0c51931a254420701119dcd981bee64eb2b58e1df91d9bcf458177`  
		Last Modified: Tue, 17 Mar 2026 01:42:48 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16a9dd4c21c2493366b82552faade9650e65b277d010834033da1e7b9bc00486`  
		Last Modified: Tue, 17 Mar 2026 01:42:49 GMT  
		Size: 41.8 MB (41825593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f70052ca9c325e384eba3588f48184199aa6476f535695d12f4cdbc20d4d52a`  
		Last Modified: Tue, 17 Mar 2026 01:42:48 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:4-bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:c844c4878e3ef1467978649719e6996b95186a754edb1e8c99c5e3ace5afb6f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (15981534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:719d0f517263953f1efd9041d6ec106c6301f827dde09609570f4a41f416ccd0`

```dockerfile
```

-	Layers:
	-	`sha256:a0377f80df7ae61181aef25fd79782d3b0e382035162c5d2fe37cfbe92d72b6e`  
		Last Modified: Tue, 17 Mar 2026 01:42:49 GMT  
		Size: 16.0 MB (15959655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c1fb282fcb56cd56f74dae85f3811d8f94d7b558404edd3679ac7f1c0c4abb5`  
		Last Modified: Tue, 17 Mar 2026 01:42:48 GMT  
		Size: 21.9 KB (21879 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:4-bookworm` - linux; mips64le

```console
$ docker pull ruby@sha256:d8ec53dab1787a1e285772e852b6115261c6f3c50a8a0b988d9a01d20b69811e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **369.4 MB (369427578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc5577124367e0308eefae2daef24599b1b2cd30a822c13505efaa73af879fcc`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1771804800'
# Wed, 25 Feb 2026 06:07:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 25 Feb 2026 11:29:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 25 Feb 2026 12:13:28 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 25 Feb 2026 17:42:23 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 25 Feb 2026 17:55:18 GMT
ENV LANG=C.UTF-8
# Wed, 25 Feb 2026 17:55:18 GMT
ENV RUBY_VERSION=4.0.1
# Wed, 25 Feb 2026 17:55:18 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/4.0/ruby-4.0.1.tar.xz
# Wed, 25 Feb 2026 17:55:18 GMT
ENV RUBY_DOWNLOAD_SHA256=0531fe57dfdb56bf591620d2450642ea0e0964f3512a6ebee7dc9305de69395f
# Wed, 25 Feb 2026 17:55:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 		${rustArch:+--enable-zjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 25 Feb 2026 17:55:18 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 25 Feb 2026 17:55:18 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 25 Feb 2026 17:55:18 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 25 Feb 2026 17:55:20 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 25 Feb 2026 17:55:20 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:6ec71ee94fb878725e70f6a21c20349985b89066361ee1f753b3854cfa2c839a`  
		Last Modified: Tue, 24 Feb 2026 18:41:37 GMT  
		Size: 48.8 MB (48782510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ea2283ea3597dab73b85bc0ebe9635f3297b9d6d4b8ff5df7913003859ba369`  
		Last Modified: Wed, 25 Feb 2026 06:07:50 GMT  
		Size: 23.6 MB (23615315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:372ec86799dac23af2f0ffbced98ecf9eceeaa5ddf68be3af3cc474182e97448`  
		Last Modified: Wed, 25 Feb 2026 11:30:27 GMT  
		Size: 63.3 MB (63310148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef2370d1847154e56fd3c4e4c8b7f77f8fe2f13b47db8c406f787a33dd6eea5d`  
		Last Modified: Wed, 25 Feb 2026 12:16:43 GMT  
		Size: 190.3 MB (190275067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d8981a10b723cd598225e629d7b34b77fd799caf77e1c9d2b532a0d12b98ec`  
		Last Modified: Wed, 25 Feb 2026 17:56:28 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf8d429d2cd79dd57cb5704138f8db125d2a590d299bfa04c11b64dd78c8c401`  
		Last Modified: Wed, 25 Feb 2026 17:56:33 GMT  
		Size: 43.4 MB (43444205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48384878e08f18ce8c4bdfe05b898ab4f0376a0ba54f95d956a15ec30c677bef`  
		Last Modified: Wed, 25 Feb 2026 17:56:28 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:4-bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:f0f469832258f8810fb453d3aef964f3f2878985b9176f82e04d682437c49100
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.8 KB (21773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59ed210564dd9a619e737fe6320e513f162dacaa16ce1faa0f29010a4ac2219f`

```dockerfile
```

-	Layers:
	-	`sha256:4c329732bf8a7a6cee6fdea406105f37d7b6fc52a0eda5235d2c26302cd4555b`  
		Last Modified: Wed, 25 Feb 2026 17:56:28 GMT  
		Size: 21.8 KB (21773 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:4-bookworm` - linux; ppc64le

```console
$ docker pull ruby@sha256:737ca91558d9d418c910e3054f430e4e07684e4e56e5d163181907360076d019
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **406.4 MB (406366257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eaf653de2f6eec8bafcc89587297169f37966075f7b5758e0fd4e287c961621`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 21:18:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 25 Feb 2026 02:56:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 25 Feb 2026 06:16:55 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 25 Feb 2026 13:32:53 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 25 Feb 2026 13:36:29 GMT
ENV LANG=C.UTF-8
# Wed, 25 Feb 2026 13:36:29 GMT
ENV RUBY_VERSION=4.0.1
# Wed, 25 Feb 2026 13:36:29 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/4.0/ruby-4.0.1.tar.xz
# Wed, 25 Feb 2026 13:36:29 GMT
ENV RUBY_DOWNLOAD_SHA256=0531fe57dfdb56bf591620d2450642ea0e0964f3512a6ebee7dc9305de69395f
# Wed, 25 Feb 2026 13:36:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 		${rustArch:+--enable-zjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 25 Feb 2026 13:36:29 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 25 Feb 2026 13:36:29 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 25 Feb 2026 13:36:29 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 25 Feb 2026 13:36:30 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 25 Feb 2026 13:36:30 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:605d3e8e339092bb5c341e87f55fee22f143aaa738eb91d341b5fc6aa27b2b5b`  
		Last Modified: Tue, 24 Feb 2026 18:41:51 GMT  
		Size: 52.3 MB (52336797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5ba53e63c4e3e4d88f0425bc79a37e364db9aabbff9c13ece5cecc63ec880f3`  
		Last Modified: Tue, 24 Feb 2026 21:19:17 GMT  
		Size: 25.7 MB (25671399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5eaeecfe60befcd3d5daac43038587e48eaaea46a2b5f8466018b05c5579686`  
		Last Modified: Wed, 25 Feb 2026 02:57:13 GMT  
		Size: 69.8 MB (69846164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14f4312b16c51bbd6e954a27bda969cc71b767dbba23b0d13c6ef19e992222f9`  
		Last Modified: Wed, 25 Feb 2026 06:18:31 GMT  
		Size: 214.6 MB (214555058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f9dcef4041662ee455bd4b694415039fd4da91e8730477ebb3cba244454d96d`  
		Last Modified: Wed, 25 Feb 2026 13:37:14 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:179649e4e0fe4f26d690b4c1f605f0f90f3e9fc23be5be610a1a2284b480f84f`  
		Last Modified: Wed, 25 Feb 2026 13:37:15 GMT  
		Size: 44.0 MB (43956505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd945452a0f00be4416b080c86568d8753170a3f2303bcdb2e1bee108d4b52cd`  
		Last Modified: Wed, 25 Feb 2026 13:37:14 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:4-bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:695825a20277b7c09d389d9d85e0145e937e4b5ab08d1b497e20a1d11979464e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (15979922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad613c9bab1171042785590ef9dba05d75da7210211333982fbefdd47a6da06d`

```dockerfile
```

-	Layers:
	-	`sha256:ee5556818cc3ec18546f55e99c17b14e7bdcff44ca34730cdbdafbefbf896a02`  
		Last Modified: Wed, 25 Feb 2026 13:37:14 GMT  
		Size: 16.0 MB (15957958 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06009ccd8b9385a179998ef50eeaf325203d1bca19af59ea6be8043fe924595b`  
		Last Modified: Wed, 25 Feb 2026 13:37:14 GMT  
		Size: 22.0 KB (21964 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:4-bookworm` - linux; s390x

```console
$ docker pull ruby@sha256:fecf8c707e6b9b906b1c1a4bf5f1bc2e89ce31624a73fbbcb7394991c4afdf4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **361.4 MB (361449391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9dfe1c578e65d5004f8c866cc503523fb944c1328deeea760fbec5d9946a40e`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 23:44:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:33:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:17:47 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 09:24:43 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 17 Mar 2026 09:32:42 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 09:32:42 GMT
ENV RUBY_VERSION=4.0.1
# Tue, 17 Mar 2026 09:32:42 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/4.0/ruby-4.0.1.tar.xz
# Tue, 17 Mar 2026 09:32:42 GMT
ENV RUBY_DOWNLOAD_SHA256=0531fe57dfdb56bf591620d2450642ea0e0964f3512a6ebee7dc9305de69395f
# Tue, 17 Mar 2026 09:32:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 		${rustArch:+--enable-zjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 17 Mar 2026 09:32:42 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 17 Mar 2026 09:32:42 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 17 Mar 2026 09:32:42 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 09:32:46 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 17 Mar 2026 09:32:46 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:7dbc3949555449666cc7651209b926019d3fc7f1511f7ebcd8979762b12d59c1`  
		Last Modified: Mon, 16 Mar 2026 21:51:27 GMT  
		Size: 47.1 MB (47147919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d904b886f0656b8d9f7b2cc64089c6c03aa31b22b97fbf96b0bc6c4e3726e429`  
		Last Modified: Mon, 16 Mar 2026 23:44:29 GMT  
		Size: 24.0 MB (24033614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3244a56b42252330a5ec4502181ecac45b16d96de3113430b375f7d10e72bde6`  
		Last Modified: Tue, 17 Mar 2026 01:33:52 GMT  
		Size: 63.5 MB (63501466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce6ecbe55d971e05ad1df82bad38bb9cb8aa1893bd6b359e40868f6d09c40969`  
		Last Modified: Tue, 17 Mar 2026 02:18:46 GMT  
		Size: 183.6 MB (183569528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e0cc731a0d4d9bcf4026f38ed4b6af70cd8ef20c2661ca26e2c6cb428bce4e2`  
		Last Modified: Tue, 17 Mar 2026 09:34:24 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae540481dbd2ed96c958e39e8d32af59ce4b3ac1af4cb6370f7188806adbe23`  
		Last Modified: Tue, 17 Mar 2026 09:34:33 GMT  
		Size: 43.2 MB (43196532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7236fb9fb7e69c503d7eaf5c7253670ac5c4d05a56c44ac7a07b3651b4b85a11`  
		Last Modified: Tue, 17 Mar 2026 09:34:26 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:4-bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:266054cb3072658b7cfb69675d5a4f00d085c0603e964dd04944869568564960
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.8 MB (15810952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc96b8480c123b0c7ea8cbaaff3ede75e0ef363f060037b6cbc5ae4604df56f1`

```dockerfile
```

-	Layers:
	-	`sha256:30e5493205f1d3561647008604b85d3c0bdeabccc1c5aad7a72e0bddf03e7bee`  
		Last Modified: Tue, 17 Mar 2026 09:34:30 GMT  
		Size: 15.8 MB (15789037 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1c22642e9edef4e1e9e99a136bcb98e52df8c960928a223f641ee762072ce3d`  
		Last Modified: Tue, 17 Mar 2026 09:34:28 GMT  
		Size: 21.9 KB (21915 bytes)  
		MIME: application/vnd.in-toto+json
