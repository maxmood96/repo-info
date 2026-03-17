## `ruby:3-bookworm`

```console
$ docker pull ruby@sha256:c1bea11acfe43099327f46614c88d8c309c4964c3d43e62daa8828abd11357c5
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

### `ruby:3-bookworm` - linux; amd64

```console
$ docker pull ruby@sha256:1f5ac08a466cad2153dab055aad13192a89d6a25dccd7770c9efe141753f5ff7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **390.0 MB (390000751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95e99c4a0e0bb43d5d4b0c33373405e3951bf2c53ecfa9b0160c27c4a4706a71`
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
# Tue, 17 Mar 2026 02:21:04 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 17 Mar 2026 02:23:13 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 02:23:13 GMT
ENV RUBY_VERSION=3.4.9
# Tue, 17 Mar 2026 02:23:13 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Tue, 17 Mar 2026 02:23:13 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Tue, 17 Mar 2026 02:23:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 17 Mar 2026 02:23:13 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 17 Mar 2026 02:23:13 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 17 Mar 2026 02:23:13 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:23:13 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 17 Mar 2026 02:23:13 GMT
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
	-	`sha256:d59145270e64cc57e2e8e34d8a6cfc755954a917458305da58e5fdb786eaceca`  
		Last Modified: Tue, 17 Mar 2026 02:23:31 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae6fc0049ddda5915f7ac25998804bde171558910a257b2341d2579c340cc70c`  
		Last Modified: Tue, 17 Mar 2026 02:23:33 GMT  
		Size: 41.5 MB (41548618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acdf4e9b1a6d932033b706cea4ce720a1b2d14f2851596753c81458f2bd97704`  
		Last Modified: Tue, 17 Mar 2026 02:23:29 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:9c3ed3eaaad1ee07b26655c4f8a927ab46aa930cbfdd46285b7507d9eab4b119
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (16006632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b3f45bbc07de547e67f3cc4f4493a53b7b08f878b75222783677dc4512bf778`

```dockerfile
```

-	Layers:
	-	`sha256:34677824f9e4de2450433d55d86af6f2ba2e8d5a50b6524176c00de6fc310940`  
		Last Modified: Tue, 17 Mar 2026 02:23:32 GMT  
		Size: 16.0 MB (15985130 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82d68d5cce8c5af9bca8fb31951f9be00e579edbf61aa9ca552f94153ae3ed28`  
		Last Modified: Tue, 17 Mar 2026 02:23:31 GMT  
		Size: 21.5 KB (21502 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-bookworm` - linux; arm variant v5

```console
$ docker pull ruby@sha256:c904615a39dddd175864eccfda262fa19c5db9b54f6cc1eefc78edae5843ba92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.8 MB (352841147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62ae144011e614a63f27c9509fcfdafa7f12061a803b91bb6b1d10750e236928`
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
# Tue, 17 Mar 2026 04:37:49 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 17 Mar 2026 04:40:00 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 04:40:00 GMT
ENV RUBY_VERSION=3.4.9
# Tue, 17 Mar 2026 04:40:00 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Tue, 17 Mar 2026 04:40:00 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Tue, 17 Mar 2026 04:40:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 17 Mar 2026 04:40:00 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 17 Mar 2026 04:40:00 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 17 Mar 2026 04:40:00 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 04:40:01 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 17 Mar 2026 04:40:01 GMT
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
	-	`sha256:14c6c4859ad8c719c84e2e240385c89c18c965cce1cd3ab3d2d5f0b76d455205`  
		Last Modified: Tue, 17 Mar 2026 04:40:19 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f9961e23ae4d8fd02d2c0088ad43a259876b9c6df65787004408594bc19134d`  
		Last Modified: Tue, 17 Mar 2026 04:40:20 GMT  
		Size: 37.3 MB (37308312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9294745f638c45abeca72e4b562eb9bdb63ada7bb3d1068e3feab778808a206e`  
		Last Modified: Tue, 17 Mar 2026 04:40:19 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:5d87aa951c05c899408f24a266fbf6d333c2931c4900f8277b0978ad44d4e1f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.8 MB (15803723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f08d0aa779300d604b1fd7044231318dc0318da626ff2e27e89b0c9a3a279ba`

```dockerfile
```

-	Layers:
	-	`sha256:a4f7e5a88d049f7382042a102b1fc3c6b839b8163f81bb8df2daec62b566878a`  
		Last Modified: Tue, 17 Mar 2026 04:40:19 GMT  
		Size: 15.8 MB (15782122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd3f7fc4bd1068cc012ec57fd28af05a19e8354e607e46b8982ef5fc1353e724`  
		Last Modified: Tue, 17 Mar 2026 04:40:19 GMT  
		Size: 21.6 KB (21601 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-bookworm` - linux; arm variant v7

```console
$ docker pull ruby@sha256:adefb19807df4976b1ac84304ecc4d15b6305292969d6425e73d7436fe97a391
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.4 MB (338374201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caf8b9f1c514cde84c6c4b12bd31516749c45f68e011e94ee34b460e94503e2a`
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
# Tue, 17 Mar 2026 02:37:51 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 17 Mar 2026 02:40:02 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 02:40:02 GMT
ENV RUBY_VERSION=3.4.9
# Tue, 17 Mar 2026 02:40:02 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Tue, 17 Mar 2026 02:40:02 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Tue, 17 Mar 2026 02:40:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 17 Mar 2026 02:40:02 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 17 Mar 2026 02:40:02 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 17 Mar 2026 02:40:02 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:40:02 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 17 Mar 2026 02:40:02 GMT
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
	-	`sha256:59a51d2d03a3015f42f2781517c3d2f0b696a41a1272a1a46bb638e50d0e054a`  
		Last Modified: Tue, 17 Mar 2026 02:40:20 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:518e22e0edec5189cc3806958a8af2f477ee248687f49181293da4f3adafe988`  
		Last Modified: Tue, 17 Mar 2026 02:40:22 GMT  
		Size: 37.1 MB (37140947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e49cf7f7854efbf5877290e65a0116f10771d635d2be4b5c09f146ab3ef2edd`  
		Last Modified: Tue, 17 Mar 2026 02:40:20 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:18d3a87f93f4576c57bee82f58a3b7bec64090364fae1f3365257d957644e26e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.8 MB (15809199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3f87a317b450aeda187a7355c6c2c1ea35d2278220968608cc158b2a8cf1f1b`

```dockerfile
```

-	Layers:
	-	`sha256:44391555e3ccdd49b8c3a312474f382238a2978318e02b9fbddb7e19195e98e1`  
		Last Modified: Tue, 17 Mar 2026 02:40:21 GMT  
		Size: 15.8 MB (15787598 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73a37fd0271b6363f3e52d0e5cb57b74b74fd765b91765efc87f78734fc3830e`  
		Last Modified: Tue, 17 Mar 2026 02:40:20 GMT  
		Size: 21.6 KB (21601 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-bookworm` - linux; arm64 variant v8

```console
$ docker pull ruby@sha256:4c67d387d8c6095ed7c46edcfec680e4d4161fabe7b73da8e47326d0902f417b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **381.0 MB (380963921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8687bec40aa82f844ad6e15aaca227609b70723b2611b7a33b5008cfc0f4ba6`
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
# Tue, 17 Mar 2026 02:26:52 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 17 Mar 2026 02:28:56 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 02:28:56 GMT
ENV RUBY_VERSION=3.4.9
# Tue, 17 Mar 2026 02:28:56 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Tue, 17 Mar 2026 02:28:56 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Tue, 17 Mar 2026 02:28:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 17 Mar 2026 02:28:56 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 17 Mar 2026 02:28:56 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 17 Mar 2026 02:28:56 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:28:57 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 17 Mar 2026 02:28:57 GMT
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
	-	`sha256:9cc8e609dc9308271fae76a5aeff94d1157c20e72067ddf9771168aa90b3408f`  
		Last Modified: Tue, 17 Mar 2026 02:29:15 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d805bf9530ef6841b67e1c5fe5caf60fcfac3706b16eef2087fbf189ce2f250a`  
		Last Modified: Tue, 17 Mar 2026 02:29:17 GMT  
		Size: 41.4 MB (41436550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1db93b9862723955856f7d438e3c170a3c8c88ab0bd379e69e98e8d5493702c`  
		Last Modified: Tue, 17 Mar 2026 02:29:15 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:367a2d1e31aa1ec15ffb86310c8a73ce170f969b5cd8e6b651f1843852223a9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (16035269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d0647a862faba3f0b3f9fafc8c93bc0f561202a3ac08b61b1cb7db8a1e7b32f`

```dockerfile
```

-	Layers:
	-	`sha256:a97b1db0a69af3f20d32f2d7f9f0a4a4ec03d76e9cee43fd1dd88f6128538cb4`  
		Last Modified: Tue, 17 Mar 2026 02:29:16 GMT  
		Size: 16.0 MB (16013644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6d55057e2fcb12923ab03ccc3c9cba508e13acd3828fa2ae91607dda6c8cdc4`  
		Last Modified: Tue, 17 Mar 2026 02:29:15 GMT  
		Size: 21.6 KB (21625 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-bookworm` - linux; 386

```console
$ docker pull ruby@sha256:3215d693b9ed2a3272db50315816d93dab921a63f2d21653ed480ae6eef369d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **388.1 MB (388148595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d415c3d06d39b3aa43de0a5b835b493a1fe90e78bbc36b4213df2c3731f55345`
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
# Tue, 17 Mar 2026 01:41:33 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 17 Mar 2026 01:43:22 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 01:43:22 GMT
ENV RUBY_VERSION=3.4.9
# Tue, 17 Mar 2026 01:43:22 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Tue, 17 Mar 2026 01:43:22 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Tue, 17 Mar 2026 01:43:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 17 Mar 2026 01:43:22 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 17 Mar 2026 01:43:22 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 17 Mar 2026 01:43:22 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 01:43:22 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 17 Mar 2026 01:43:22 GMT
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
	-	`sha256:160b2a73a5a8c7a5d2c985fa8e781611154455b031978c95d932d630b96d21b9`  
		Last Modified: Tue, 17 Mar 2026 01:43:38 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e43514a5b1158f95ee5799140f84b7b11c621485eea16f82144d765b2ee16ece`  
		Last Modified: Tue, 17 Mar 2026 01:43:39 GMT  
		Size: 37.1 MB (37090687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96b3a6b26d3a81f54d6f5c6c073fb7c9e0e6dfdbc5c992326a231be14b5c0382`  
		Last Modified: Tue, 17 Mar 2026 01:43:38 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:e428c85b3f99d99255e492ce66c9c72f1f1aa31766cdbdb2436d93623b41a58b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (15984822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f3cbe13ec3c0ac2e5f72c0aae0b925781c5a493b9a7b5d02eb005fb0176f723`

```dockerfile
```

-	Layers:
	-	`sha256:7a32595d5f379341227957687069c6fb315bdaa26762739393d74ef67dca9ddd`  
		Last Modified: Tue, 17 Mar 2026 01:43:39 GMT  
		Size: 16.0 MB (15963351 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f063707526d1cd0b2c7a3910793f158b47401ff30898302a3c13e7d0b0236654`  
		Last Modified: Tue, 17 Mar 2026 01:43:38 GMT  
		Size: 21.5 KB (21471 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-bookworm` - linux; mips64le

```console
$ docker pull ruby@sha256:709db4bff1dc943acd28f6a6bf9f0eda09e183aaf060371440a828bce9d3cf44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.5 MB (364467233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:703c08880c4472c9a128baba57a081427b22ddff4bb98811aeb8ca67ff4d9478`
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
# Wed, 11 Mar 2026 18:23:42 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 11 Mar 2026 18:36:21 GMT
ENV LANG=C.UTF-8
# Wed, 11 Mar 2026 18:36:21 GMT
ENV RUBY_VERSION=3.4.9
# Wed, 11 Mar 2026 18:36:21 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Wed, 11 Mar 2026 18:36:21 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Wed, 11 Mar 2026 18:36:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 11 Mar 2026 18:36:21 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 11 Mar 2026 18:36:21 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 11 Mar 2026 18:36:21 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Mar 2026 18:36:23 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 11 Mar 2026 18:36:23 GMT
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
	-	`sha256:423d25085b37fa0b7ff83953ba656d60788dc6b6b27d1e88056613546194c2bb`  
		Last Modified: Wed, 11 Mar 2026 18:37:34 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a1805ab92d0ee8079498ab33ce6096e2e0ac006c6549720c99f6acb8fb99530`  
		Last Modified: Wed, 11 Mar 2026 18:37:39 GMT  
		Size: 38.5 MB (38483858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51bf98aa2fb01c6d62b84b92703096861d25b45c67833bb93c0d2d8e56aa0ac5`  
		Last Modified: Wed, 11 Mar 2026 18:37:34 GMT  
		Size: 145.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:218d0d62561c2f193219b5c9895029acff8bacc0b1a3422922d835865d70deab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.4 KB (21351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:695873ecfb0d017ea8faa28a0d0fe29af1fb07a067efc3a59bd227cb48249463`

```dockerfile
```

-	Layers:
	-	`sha256:aae2f70b7a961546f99562a10ad2b869f3b2a27877fdb33446d7cf458c5aea0b`  
		Last Modified: Wed, 11 Mar 2026 18:37:34 GMT  
		Size: 21.4 KB (21351 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-bookworm` - linux; ppc64le

```console
$ docker pull ruby@sha256:282cd3a596ae70a2fd0f5a6f67a293cac59858575551ce04e37f56413b55afaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **401.4 MB (401368118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6628f16e9c593321d12d11a89fed33f555e60e0e5209d6179a7639983ce00ed1`
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
# Wed, 11 Mar 2026 18:45:20 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 11 Mar 2026 18:48:53 GMT
ENV LANG=C.UTF-8
# Wed, 11 Mar 2026 18:48:53 GMT
ENV RUBY_VERSION=3.4.9
# Wed, 11 Mar 2026 18:48:53 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Wed, 11 Mar 2026 18:48:53 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Wed, 11 Mar 2026 18:48:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 11 Mar 2026 18:48:53 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 11 Mar 2026 18:48:53 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 11 Mar 2026 18:48:53 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Mar 2026 18:48:53 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 11 Mar 2026 18:48:53 GMT
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
	-	`sha256:32edbbc9f54a7bd4d59d7a3e5445b3040b3fb39e21a3cf5606ea31dd70c97aa0`  
		Last Modified: Wed, 11 Mar 2026 18:49:37 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:221cd80865e89162b624bc13f93eab614c4e513c25c3bc8e6f2e9ce13b12dea6`  
		Last Modified: Wed, 11 Mar 2026 18:49:42 GMT  
		Size: 39.0 MB (38958367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9c42fd7dc57af2629ed6a54288f589f01427651613e2307f1a8e48bd894b88c`  
		Last Modified: Wed, 11 Mar 2026 18:49:37 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:3f3dfc6dbeb16b5662b2e6a07813aefa0c5493832076dc4860f4abd32bbf53b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (15983188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66e032d53eade89c43ab788c51aaeedc88555a1e4cb044e0266919421cd69e05`

```dockerfile
```

-	Layers:
	-	`sha256:3df143957caedbd8809c4d29009051cacd282dc7f400c8c1409c4fb16e239ec3`  
		Last Modified: Wed, 11 Mar 2026 18:49:41 GMT  
		Size: 16.0 MB (15961643 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:581625067d96cf56258d6d735ef03bf1d42f778f7fa44ce5d3ed79a27610c7e2`  
		Last Modified: Wed, 11 Mar 2026 18:49:37 GMT  
		Size: 21.5 KB (21545 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-bookworm` - linux; s390x

```console
$ docker pull ruby@sha256:1a554830a688a1033eb9b41251cbc6beea35226df3db8e8d9db343ef1dd81b2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **356.4 MB (356392282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb9281255fda7df6aadba34b60c05531e3e95a421c5f87f43d079ea58f16a85a`
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
# Tue, 17 Mar 2026 09:28:04 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 17 Mar 2026 09:35:58 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 09:35:58 GMT
ENV RUBY_VERSION=3.4.9
# Tue, 17 Mar 2026 09:35:58 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Tue, 17 Mar 2026 09:35:58 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Tue, 17 Mar 2026 09:35:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 17 Mar 2026 09:35:58 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 17 Mar 2026 09:35:58 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 17 Mar 2026 09:35:58 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 09:36:02 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 17 Mar 2026 09:36:02 GMT
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
	-	`sha256:eccd875b7790048fd37e3e9d36b77dfd22ee1fa97b86a79e4f73e6161afd1bd3`  
		Last Modified: Tue, 17 Mar 2026 09:37:32 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33f8151b7db64ad472ac3b7f7abbce42a7ab611d3ca5c1326ee909a2d9393c5f`  
		Last Modified: Tue, 17 Mar 2026 09:37:38 GMT  
		Size: 38.1 MB (38139423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c30fa3c18c4db69d011284a8d1a663f0cf188f969dac6235c8d91bd16eec227d`  
		Last Modified: Tue, 17 Mar 2026 09:37:32 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:5a5451c56f58fa82f4d6025606af4ab7a61a89916cb1178f67babfd6efb2e034
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.8 MB (15814231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:367996a827377fcfff4dff34b5e34359a74a7c6fb0ce1896746b279fd205dbce`

```dockerfile
```

-	Layers:
	-	`sha256:0aa8fc2b58216cf751a0d1b75ee4d19581dc29d1552392560d53f66593be06cf`  
		Last Modified: Tue, 17 Mar 2026 09:37:37 GMT  
		Size: 15.8 MB (15792728 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85b2512e5b6082b0bd27e985ce80071fb380b690dca83716c3a554c0bbfb3844`  
		Last Modified: Tue, 17 Mar 2026 09:37:29 GMT  
		Size: 21.5 KB (21503 bytes)  
		MIME: application/vnd.in-toto+json
