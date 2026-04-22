## `ruby:bookworm`

```console
$ docker pull ruby@sha256:f2b955f1654739bb554f350d88b8bb18f3e888c1bcd233b5de34fe5b17d92d51
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

### `ruby:bookworm` - linux; amd64

```console
$ docker pull ruby@sha256:cb7b0ed375e9577fd787d56c8ded159ab3863b6f4e2ae81ed88773467615cf87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **397.5 MB (397541531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a932997512a6b66a7a503677b0e8943bad833b0bcef3a187642004704b48342`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 05:00:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 05:12:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 06:12:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 07:28:45 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 22 Apr 2026 07:30:40 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 07:30:40 GMT
ENV RUBY_VERSION=4.0.3
# Wed, 22 Apr 2026 07:30:40 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/4.0/ruby-4.0.3.tar.xz
# Wed, 22 Apr 2026 07:30:40 GMT
ENV RUBY_DOWNLOAD_SHA256=22cf6005d25bbe496b5ebe9224d63a1aaabfbfe02591bb5d612517c5a7836f29
# Wed, 22 Apr 2026 07:30:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 		${rustArch:+--enable-zjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 22 Apr 2026 07:30:40 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 22 Apr 2026 07:30:40 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 22 Apr 2026 07:30:40 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 07:30:40 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 22 Apr 2026 07:30:40 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:db53381ee51f9e43304e236099ba097ae1b33ae41a8007e0b6319992eb55fd00`  
		Last Modified: Wed, 22 Apr 2026 00:15:45 GMT  
		Size: 48.5 MB (48488628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5203b2bfeff92b72e816dc6cbb1f16856f0cd592e521e3c0cfa195a78fe180e`  
		Last Modified: Wed, 22 Apr 2026 05:01:15 GMT  
		Size: 24.0 MB (24042234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fcda2b4d7993820b00c5488d173051e76d01ba6b85620617ba77001b0f9e2fa`  
		Last Modified: Wed, 22 Apr 2026 05:12:28 GMT  
		Size: 64.4 MB (64396988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2933ecab0f11302fd71f29aa83ad2904683246f7a8320ad0dc3a60b23f05fee9`  
		Last Modified: Wed, 22 Apr 2026 06:13:02 GMT  
		Size: 211.5 MB (211545979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473e25dd526ef1423c8426f0d8e2b17987142d173d1ccafc1b63122a539b2fc1`  
		Last Modified: Wed, 22 Apr 2026 07:30:57 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ddd10ba76d8de307d5ee4607ef7462e3372175b672531dc8582de93829e4677`  
		Last Modified: Wed, 22 Apr 2026 07:30:58 GMT  
		Size: 49.1 MB (49067370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d9720bd07c42de4cb868a2209916f21142c85fad32f1f80440282123a87249d`  
		Last Modified: Wed, 22 Apr 2026 07:30:57 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:68c5126d1575439a6137feac66e74464542eb3460aaa1276a128ec7224753334
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (16003361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3cb10d95778e757e988136d556c335a9e1ca1d9f847a0e70c4a22933ce02c05`

```dockerfile
```

-	Layers:
	-	`sha256:edd04a3168cc96abc4edc46ff0955b52e71eb9076c87ba6a33434646ac7c77e0`  
		Last Modified: Wed, 22 Apr 2026 07:30:58 GMT  
		Size: 16.0 MB (15981445 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce9edc19ef63f8b6d8819fdc5e90cc8c3f39ff6df93843d05e3982c99e5c70eb`  
		Last Modified: Wed, 22 Apr 2026 07:30:57 GMT  
		Size: 21.9 KB (21916 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:bookworm` - linux; arm variant v5

```console
$ docker pull ruby@sha256:218d3abf05c8c2e1e39df969708b8dc53bb59e9df1251e879d016ecf6c71df67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **357.6 MB (357630480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09905ee8e354091fcb6ee8c74a2cd59d220f3938a8f9fdfb42ec2ba1820294c0`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 02:16:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 04:08:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 05:13:55 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 07:05:47 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 22 Apr 2026 07:07:59 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 07:07:59 GMT
ENV RUBY_VERSION=4.0.3
# Wed, 22 Apr 2026 07:07:59 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/4.0/ruby-4.0.3.tar.xz
# Wed, 22 Apr 2026 07:07:59 GMT
ENV RUBY_DOWNLOAD_SHA256=22cf6005d25bbe496b5ebe9224d63a1aaabfbfe02591bb5d612517c5a7836f29
# Wed, 22 Apr 2026 07:07:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 		${rustArch:+--enable-zjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 22 Apr 2026 07:07:59 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 22 Apr 2026 07:07:59 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 22 Apr 2026 07:07:59 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 07:07:59 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 22 Apr 2026 07:07:59 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:4c47739de5592cd0e20e88645e3c951f4f15c777c5919d72ffd47300390dc284`  
		Last Modified: Wed, 22 Apr 2026 00:15:32 GMT  
		Size: 46.0 MB (46021502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0c7875a3d22c687eb5bf820de1b373b9b156f8c8be64706cf9bd3621ed23fd9`  
		Last Modified: Wed, 22 Apr 2026 02:17:06 GMT  
		Size: 22.7 MB (22716442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6225320cd10febcf4143fdb335076e5aeb16ced496a60fcc373793ab7ed3e8d7`  
		Last Modified: Wed, 22 Apr 2026 04:08:58 GMT  
		Size: 62.0 MB (62008562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52d8eefd089eff71f9faac454ebec89a0afde64344b69335ea01f0152d56180e`  
		Last Modified: Wed, 22 Apr 2026 05:14:33 GMT  
		Size: 184.8 MB (184803016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f6324a791b3e6ac77f63c0eebb136441da4a08fc67922277f024dbbad45c7d3`  
		Last Modified: Wed, 22 Apr 2026 07:08:18 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0b28fc45b8b2d0e36bd43d02dcd4f9e4edc5d35b0b8b9de49026fe3df9e9ea3`  
		Last Modified: Wed, 22 Apr 2026 07:08:19 GMT  
		Size: 42.1 MB (42080626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:512f4b073bd3d1b2eb02454aed1adf77a32fc86b4ef62aaa7489ac04a9696510`  
		Last Modified: Wed, 22 Apr 2026 07:08:17 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:24b0b56b48c9953f65c24bd88c07bb5d34d2b20b9ae5462ca0891659a1f72928
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.8 MB (15800467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8938b3cbdbe8efb5308c4781774a81ab440ec9fc26cddbd4941445a838423172`

```dockerfile
```

-	Layers:
	-	`sha256:ef3b59e626fcc3d3e561af65abe5a694e04ded6855b0e27527619faa3f46ca7d`  
		Last Modified: Wed, 22 Apr 2026 07:08:18 GMT  
		Size: 15.8 MB (15778445 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d09ee15a32ca7a383eb2baa1e5bafb66ceaf0843ee5aae5f8dcdf4b7954c7539`  
		Last Modified: Wed, 22 Apr 2026 07:08:17 GMT  
		Size: 22.0 KB (22022 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:bookworm` - linux; arm variant v7

```console
$ docker pull ruby@sha256:3d3be0083a9a6ee2abd927596b0c138a7dfbe531494ce965206c913524e54915
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.1 MB (343140580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aabefe62658df91ea8c98af84b48e724215b4383fc27b12c184feab34fad5ed4`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 02:18:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 03:52:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 04:15:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 06:08:59 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 22 Apr 2026 06:11:10 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 06:11:10 GMT
ENV RUBY_VERSION=4.0.3
# Wed, 22 Apr 2026 06:11:10 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/4.0/ruby-4.0.3.tar.xz
# Wed, 22 Apr 2026 06:11:10 GMT
ENV RUBY_DOWNLOAD_SHA256=22cf6005d25bbe496b5ebe9224d63a1aaabfbfe02591bb5d612517c5a7836f29
# Wed, 22 Apr 2026 06:11:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 		${rustArch:+--enable-zjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 22 Apr 2026 06:11:10 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 22 Apr 2026 06:11:10 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 22 Apr 2026 06:11:10 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 06:11:10 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 22 Apr 2026 06:11:10 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:a78e7b2123c5c35e65ee1cc17df0d11c1db8ab3c4fe80b457270c2d9ae5003b1`  
		Last Modified: Wed, 22 Apr 2026 00:16:29 GMT  
		Size: 44.2 MB (44207655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:218160481dc948cfbf943718a4363de6a3663997f19a965c7b86136ac3e28f30`  
		Last Modified: Wed, 22 Apr 2026 02:18:15 GMT  
		Size: 21.9 MB (21946340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3960cd47ab70e092f1d1162d4a33a761e2cfa64e09c3ca3118416ced1e6f99de`  
		Last Modified: Wed, 22 Apr 2026 03:52:25 GMT  
		Size: 59.7 MB (59652860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be89c631972f8c2581832e16afa81d0da42d77106101a938f8eea5df87a114ce`  
		Last Modified: Wed, 22 Apr 2026 04:16:12 GMT  
		Size: 175.4 MB (175449156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75b501038d026188dfbf0a040f74c25517b4e30df220f211be300a9497732d24`  
		Last Modified: Wed, 22 Apr 2026 06:11:29 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a07b071f9316197124044c1f4641c33144c641a00544ee0d88e0463a06eece55`  
		Last Modified: Wed, 22 Apr 2026 06:11:30 GMT  
		Size: 41.9 MB (41884236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbe85b507639c9ec17a519641a51761467af0ad0bf09942814913c76e4d352cd`  
		Last Modified: Wed, 22 Apr 2026 06:11:29 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:5e37327d3d2b3311a49fc5d41fb8ed98533eb634c9f9f8f915ddbde1479ab9b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.8 MB (15805941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:360f4facbbb8a08f5545e9474fcdca54f1b9fbf680268384e270df94e413d92f`

```dockerfile
```

-	Layers:
	-	`sha256:8ee560c1dcd198137f6ced430058a6eb3f8d34b711d6f905cd78059a0a70cebe`  
		Last Modified: Wed, 22 Apr 2026 06:11:29 GMT  
		Size: 15.8 MB (15783921 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07bfd1db3f6905519944185412f755e9bcefd96f24affc4bbcf3390cc5e54ccd`  
		Last Modified: Wed, 22 Apr 2026 06:11:29 GMT  
		Size: 22.0 KB (22020 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:bookworm` - linux; arm64 variant v8

```console
$ docker pull ruby@sha256:6a5d8a0ef9e3ff6cee28b9330bec1fa143a08ff3589ad7187db9fc5e249a79c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **388.3 MB (388349914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93665bfcdb0268fe2ef0ea9d84f00c788fc0a25dd17395e9ebf4fa582e8259cd`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:42:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:32:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 03:16:35 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 04:58:42 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 22 Apr 2026 05:00:42 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 05:00:42 GMT
ENV RUBY_VERSION=4.0.3
# Wed, 22 Apr 2026 05:00:42 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/4.0/ruby-4.0.3.tar.xz
# Wed, 22 Apr 2026 05:00:42 GMT
ENV RUBY_DOWNLOAD_SHA256=22cf6005d25bbe496b5ebe9224d63a1aaabfbfe02591bb5d612517c5a7836f29
# Wed, 22 Apr 2026 05:00:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 		${rustArch:+--enable-zjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 22 Apr 2026 05:00:42 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 22 Apr 2026 05:00:42 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 22 Apr 2026 05:00:42 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 05:00:42 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 22 Apr 2026 05:00:42 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:30de66f8fdafab67e88d876087f571a693a1a6c4cf0abc29efbf88ea878e0d29`  
		Last Modified: Wed, 22 Apr 2026 00:15:43 GMT  
		Size: 48.4 MB (48373071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bb7bd28fbdfe678a7f45878b7b1c07dbbc0fa7753b0312aa8fd049667a9e137`  
		Last Modified: Wed, 22 Apr 2026 01:43:06 GMT  
		Size: 23.6 MB (23609423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:599d07e8492bcee46202f5eae3e3010a470acc5139840e6d14556aefa3fc355f`  
		Last Modified: Wed, 22 Apr 2026 02:32:24 GMT  
		Size: 64.5 MB (64479606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f77b2a79d553481e7f962631ac14425d8c654928f18cdc3d1f265ceb460486e`  
		Last Modified: Wed, 22 Apr 2026 03:17:17 GMT  
		Size: 203.1 MB (203064331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d3eb54a6bbefe4507fee4bafb05288ac5b3bc3a71e90d90fe3384f67f9b4121`  
		Last Modified: Wed, 22 Apr 2026 05:01:02 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2a73127536f57732cfb4b2c64dba966f24da301507d327528c9f95ca2cb09b8`  
		Last Modified: Wed, 22 Apr 2026 05:01:04 GMT  
		Size: 48.8 MB (48823151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdedbe0d05b6782a330259e751762b61a2fdd9515de944c6a7f7285c02ef8aff`  
		Last Modified: Wed, 22 Apr 2026 05:01:04 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:c502c315b27d5e6ad1f4f17067b80bbc6aa9b2f7f42dcbd36c85651f8df67fee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (16032021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:119d6836bfdca06bbb5f75a4c4868bffa2be3fc73a6484c21e13b3b1afc1bf93`

```dockerfile
```

-	Layers:
	-	`sha256:36a69a1d1601d72b989b8b193ac0cbb77549ca95af9b868731cfc8bad67619c9`  
		Last Modified: Wed, 22 Apr 2026 05:01:02 GMT  
		Size: 16.0 MB (16009971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:040663145407344dd6a98a106dcc913025f583b1460ba7a5526d446b8def6021`  
		Last Modified: Wed, 22 Apr 2026 05:01:02 GMT  
		Size: 22.1 KB (22050 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:bookworm` - linux; 386

```console
$ docker pull ruby@sha256:fe9d245a65fbfc816fb8469381baf9b6a019885434f7b02d53f1cc9a3381ea38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **392.9 MB (392904715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d26897236b9964f6095b5605144475a472740718f9b9d32c273e0dd550dd0f3`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:42:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 05:02:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 08:19:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 09:45:06 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 22 Apr 2026 09:46:54 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 09:46:54 GMT
ENV RUBY_VERSION=4.0.3
# Wed, 22 Apr 2026 09:46:54 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/4.0/ruby-4.0.3.tar.xz
# Wed, 22 Apr 2026 09:46:54 GMT
ENV RUBY_DOWNLOAD_SHA256=22cf6005d25bbe496b5ebe9224d63a1aaabfbfe02591bb5d612517c5a7836f29
# Wed, 22 Apr 2026 09:46:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 		${rustArch:+--enable-zjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 22 Apr 2026 09:46:54 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 22 Apr 2026 09:46:54 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 22 Apr 2026 09:46:54 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 09:46:54 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 22 Apr 2026 09:46:54 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:1f607c56991d572a9c9e62692330777522b959fe17a14367be35d12959214fa4`  
		Last Modified: Wed, 22 Apr 2026 00:16:17 GMT  
		Size: 49.5 MB (49477718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5d771f6f5a1356deff0c1540de8894e5249a2f8c97ba7961a41235129f48c60`  
		Last Modified: Wed, 22 Apr 2026 01:42:30 GMT  
		Size: 24.9 MB (24875723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dd81f3dc271c0572c6da562bcce13d5c0a8f379729949fde98b0b1e57ca2e4c`  
		Last Modified: Wed, 22 Apr 2026 05:02:53 GMT  
		Size: 66.2 MB (66235084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd1be51e246f00329f40c9ef8eca7bc1cfa31a9c7c2682672c63705ce9f093cf`  
		Last Modified: Wed, 22 Apr 2026 08:20:11 GMT  
		Size: 210.5 MB (210480286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:527210a97e9d54eea618fe6500853cb341062b8d51583af746c443d6836f3583`  
		Last Modified: Wed, 22 Apr 2026 09:47:11 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d1dda4ed38a7b0d31a7adde86eae8016f1b3dfd244e91a61fcf8e152f31875b`  
		Last Modified: Wed, 22 Apr 2026 09:47:12 GMT  
		Size: 41.8 MB (41835572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b38fe7035bba2721eda6ec630e367b67a181284426cb73b41613d92b3870aee8`  
		Last Modified: Wed, 22 Apr 2026 09:47:11 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:d98e6dbe1c4e8af87d3a0614781d09cb712662e34424b53f0b8477570b0a70ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (15981541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b6c77367cb5f434c8350d272d0b29bfbd9be81c155c3d0c757e460b96169b03`

```dockerfile
```

-	Layers:
	-	`sha256:e172b71910ce5197eb22d7ee81b69176594d3448f22677502c348da7e3143e3a`  
		Last Modified: Wed, 22 Apr 2026 09:47:12 GMT  
		Size: 16.0 MB (15959661 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1920e6d4352eb15208c147e85c137498633350f0471e0e395055b8d4e90cec2`  
		Last Modified: Wed, 22 Apr 2026 09:47:11 GMT  
		Size: 21.9 KB (21880 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:bookworm` - linux; mips64le

```console
$ docker pull ruby@sha256:1d55aa2f192fcfc6e1fc77e706e7d94dc8507e37de5247f9c679ecea29873e7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **369.5 MB (369467852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83eae56f89c832b1d80c4ca0052a69d393abaf3b572f9d9159e999b3fb4d7b96`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 15:01:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 20:27:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 21:13:49 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Apr 2026 02:56:57 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 21 Apr 2026 17:40:27 GMT
ENV LANG=C.UTF-8
# Tue, 21 Apr 2026 17:40:27 GMT
ENV RUBY_VERSION=4.0.3
# Tue, 21 Apr 2026 17:40:27 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/4.0/ruby-4.0.3.tar.xz
# Tue, 21 Apr 2026 17:40:27 GMT
ENV RUBY_DOWNLOAD_SHA256=22cf6005d25bbe496b5ebe9224d63a1aaabfbfe02591bb5d612517c5a7836f29
# Tue, 21 Apr 2026 17:40:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 		${rustArch:+--enable-zjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 21 Apr 2026 17:40:27 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 21 Apr 2026 17:40:27 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 21 Apr 2026 17:40:27 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Apr 2026 17:40:29 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 21 Apr 2026 17:40:29 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:7a9b4a7963b008240d9a254ca4fd1193c938bed0a9c6fe9c04630f13b1a17a44`  
		Last Modified: Tue, 07 Apr 2026 00:09:37 GMT  
		Size: 48.8 MB (48782593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5370b42611bdad35bb24b3e5a6a342f00eb8523dc8562b7babeca6f19608f4c`  
		Last Modified: Tue, 07 Apr 2026 15:01:37 GMT  
		Size: 23.6 MB (23615262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df968e8deea10f7e740272ffa34126abe9d9673e41bbeb7f3f0d785055e19a4d`  
		Last Modified: Tue, 07 Apr 2026 20:28:18 GMT  
		Size: 63.3 MB (63310060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b53c7b0b2e97b69159bf66fea4289733960187b119fb6e9314dead68e1f1231`  
		Last Modified: Tue, 07 Apr 2026 21:17:05 GMT  
		Size: 190.3 MB (190313710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f7124a27aa656c1bc037581c23843e1334ba7a5bfeb986b805d707310f6295b`  
		Last Modified: Wed, 08 Apr 2026 03:11:02 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86c695afcaab5df2083061ef6a634ef4d3d243fd6dabeba2298c4c153b29bf5e`  
		Last Modified: Tue, 21 Apr 2026 17:41:46 GMT  
		Size: 43.4 MB (43445892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7012349129aa5023027d6a17d4d78ba8b04cfa9969aa10adff14f70cb5134755`  
		Last Modified: Tue, 21 Apr 2026 17:41:42 GMT  
		Size: 145.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:148ba19832f404f74bf09189b8fc5b2f47cd9332e796200635426d12f7457331
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.8 KB (21773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09d40e1c9c71f967397be8daee480d68da365eecda3a10ec250e077bed2411f9`

```dockerfile
```

-	Layers:
	-	`sha256:63a9d9fd508bd1cbcf0f4cf6c8f2011f0356eab93bcb182bac8aaecfe14b57c7`  
		Last Modified: Tue, 21 Apr 2026 17:41:42 GMT  
		Size: 21.8 KB (21773 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:bookworm` - linux; ppc64le

```console
$ docker pull ruby@sha256:8d3e88741fdc5995a6d2f42ffe44ad12959e13e252439aa40acba1ad78c7da3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **406.4 MB (406406738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b0f06dfbb11a17d6fafbe1180d9a302d24deef18fb579309a7af841d5820549`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 04:21:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 09:50:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 18:06:54 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Apr 2026 01:45:18 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 21 Apr 2026 17:40:15 GMT
ENV LANG=C.UTF-8
# Tue, 21 Apr 2026 17:40:15 GMT
ENV RUBY_VERSION=4.0.3
# Tue, 21 Apr 2026 17:40:15 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/4.0/ruby-4.0.3.tar.xz
# Tue, 21 Apr 2026 17:40:15 GMT
ENV RUBY_DOWNLOAD_SHA256=22cf6005d25bbe496b5ebe9224d63a1aaabfbfe02591bb5d612517c5a7836f29
# Tue, 21 Apr 2026 17:40:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 		${rustArch:+--enable-zjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 21 Apr 2026 17:40:15 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 21 Apr 2026 17:40:15 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 21 Apr 2026 17:40:15 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Apr 2026 17:40:15 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 21 Apr 2026 17:40:15 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:6b775f7ad22043f8bb75d535d8a1279e43453a08a4a9e6a0b48c020c9b387079`  
		Last Modified: Tue, 07 Apr 2026 00:09:43 GMT  
		Size: 52.3 MB (52336938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a522a501745b6503b15f6badc6170d6fa2321f26576c47b363acd8cb21b2ee`  
		Last Modified: Tue, 07 Apr 2026 04:21:54 GMT  
		Size: 25.7 MB (25671577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f98ce990098f8650217504a159d9031cc264dd29e8af85f749d78eacc319c5a`  
		Last Modified: Tue, 07 Apr 2026 09:51:25 GMT  
		Size: 69.8 MB (69846122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e63dc56fac65223b1a7667756725ea07ddf7bf4cb03642cc9106da638edca86e`  
		Last Modified: Tue, 07 Apr 2026 18:09:19 GMT  
		Size: 214.6 MB (214586971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a16872daa91caba9787bad81b8975d047572372231b9603ba4c805f7e6df00dc`  
		Last Modified: Wed, 08 Apr 2026 01:49:07 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af8dd63e76af0e4c7232a9f152ff923404bbf1978a54ff4331528951ce3a384e`  
		Last Modified: Tue, 21 Apr 2026 17:41:16 GMT  
		Size: 44.0 MB (43964795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:693f91824d79d3cd819961757b1f39c1e49a4739bd81e3770803dabe57b135b4`  
		Last Modified: Tue, 21 Apr 2026 17:41:15 GMT  
		Size: 145.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:2d4fbc10eb02c79f1ff2ae3c092ab9d50c9ba7a1c3dc0284709c3a8901d4d607
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (15979927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcb846d8bfc997622217530cd127b986369865935e9747efd057bb9c0367000f`

```dockerfile
```

-	Layers:
	-	`sha256:326b99a47c4ebd82e7bfe7aed3f04e7c129fa1213a360d7a4ff489403d399f6f`  
		Last Modified: Tue, 21 Apr 2026 17:41:15 GMT  
		Size: 16.0 MB (15957964 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c41b6303370f9d3f393a3bac718de758a0919ca66ede958969c40e708310a7d3`  
		Last Modified: Tue, 21 Apr 2026 17:41:15 GMT  
		Size: 22.0 KB (21963 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:bookworm` - linux; s390x

```console
$ docker pull ruby@sha256:972789cb07134e45554ac9f0ecf57ab8a9133ab4225e028be741701ca4f4e233
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **361.5 MB (361451293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0c026d7f67c768eca777752145a987d24f613c2bb50723f3d47dc8e67a19c4b`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 02:31:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 04:20:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 05:13:20 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 09:42:19 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 22 Apr 2026 09:45:43 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 09:45:43 GMT
ENV RUBY_VERSION=4.0.3
# Wed, 22 Apr 2026 09:45:43 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/4.0/ruby-4.0.3.tar.xz
# Wed, 22 Apr 2026 09:45:43 GMT
ENV RUBY_DOWNLOAD_SHA256=22cf6005d25bbe496b5ebe9224d63a1aaabfbfe02591bb5d612517c5a7836f29
# Wed, 22 Apr 2026 09:45:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 		${rustArch:+--enable-zjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 22 Apr 2026 09:45:43 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 22 Apr 2026 09:45:43 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 22 Apr 2026 09:45:43 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 09:45:44 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 22 Apr 2026 09:45:44 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:65a8acd2327b0f3316fe8707ebd5c99b15e79306d4eca71f3e635588795ae2bb`  
		Last Modified: Wed, 22 Apr 2026 00:15:31 GMT  
		Size: 47.1 MB (47147970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac385f32c2d6e9209dd9f8ada378863aba00921ac3815f399e84f802ea5ce36e`  
		Last Modified: Wed, 22 Apr 2026 02:32:03 GMT  
		Size: 24.0 MB (24036363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8df5494ce4223646f47cc2e95923748571f15dc98fdcd0c46696a358fa2128f`  
		Last Modified: Wed, 22 Apr 2026 04:20:41 GMT  
		Size: 63.5 MB (63500148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f897cf0b1d07756a3ff6dc04beacb6e6510a8778c56dc69d1a9dd01701400550`  
		Last Modified: Wed, 22 Apr 2026 05:14:17 GMT  
		Size: 183.6 MB (183571818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f34048e23322a094f78fb6d5a8173773f2433082676d7f6f0f43d3c8780257a5`  
		Last Modified: Wed, 22 Apr 2026 09:46:23 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c78a6658c7b339d8629675a8c2a15a2ff0f9d5b497d364071c4920becc83ab82`  
		Last Modified: Wed, 22 Apr 2026 09:46:25 GMT  
		Size: 43.2 MB (43194661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3e942c480da5b7ca2756b0fbca19ab95342d8c9af9564045228e43e6bda39b8`  
		Last Modified: Wed, 22 Apr 2026 09:46:23 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:e1a04489f5f065eba41e30587f95c19c1e4ad7d83eebf0981beb6898a5991a53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.8 MB (15810959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aee2bd772fec583a0f1bba5a5908bb17f0b174906d47b2413b98661ecc194330`

```dockerfile
```

-	Layers:
	-	`sha256:a122728e4665c4000d450ff6cabaede2a20d7797843dd707a6e6bb188baba484`  
		Last Modified: Wed, 22 Apr 2026 09:46:24 GMT  
		Size: 15.8 MB (15789043 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7513b4d25b747b527d30cf6e5a25aa0d784793d74f66e4ae5c1c6e56bab5745a`  
		Last Modified: Wed, 22 Apr 2026 09:46:23 GMT  
		Size: 21.9 KB (21916 bytes)  
		MIME: application/vnd.in-toto+json
