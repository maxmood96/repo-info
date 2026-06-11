## `ruby:3-trixie`

```console
$ docker pull ruby@sha256:ebb35d4f6c902f367e7384778490a4346d8280589d55141ae47920bb8ba890e4
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

### `ruby:3-trixie` - linux; amd64

```console
$ docker pull ruby@sha256:c46fdce6b09576b4994aee22480b9994854158d23346446c25ac24f093281457
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **421.2 MB (421150723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:869746fa525eb315b2b567958117aae60a3bb4d4d1503caf3126bf97ece23639`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:42:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 02:24:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 03:16:38 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 04:57:50 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 11 Jun 2026 04:59:41 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 04:59:41 GMT
ENV RUBY_VERSION=3.4.9
# Thu, 11 Jun 2026 04:59:41 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Thu, 11 Jun 2026 04:59:41 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Thu, 11 Jun 2026 04:59:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 11 Jun 2026 04:59:41 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 11 Jun 2026 04:59:41 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 11 Jun 2026 04:59:41 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 04:59:41 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 11 Jun 2026 04:59:41 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:ef1b08ddd59d42b444e8f9c68a6cebbed70636aed0c242fdccb0bd61b61ba26b`  
		Last Modified: Wed, 10 Jun 2026 23:40:27 GMT  
		Size: 49.3 MB (49317121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b365b6ff7b7e310e1b9a88f996e65b89969c7fa450492b68249d1d1c38e0676`  
		Last Modified: Thu, 11 Jun 2026 00:42:51 GMT  
		Size: 25.6 MB (25635173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ca884014342f240be01d391b498c3ec61b2f4af2c205e7e9a0b5ac2cb2f24c4`  
		Last Modified: Thu, 11 Jun 2026 02:25:01 GMT  
		Size: 67.8 MB (67784745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:442cca122a8b0987d6ea29e5fa7d0b8caf699cb127ec5fdbd8191faf86da521f`  
		Last Modified: Thu, 11 Jun 2026 03:17:25 GMT  
		Size: 236.2 MB (236195157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6a00a56edba99d21a229e2149fe43ce096b662098d8c36ed06b800af1f55a28`  
		Last Modified: Thu, 11 Jun 2026 04:59:58 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d3ad6fec9b2f080c64e100f63f11d9a809058a569ee2381457f61662c86f5e5`  
		Last Modified: Thu, 11 Jun 2026 05:00:00 GMT  
		Size: 42.2 MB (42218196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6de2daec025d532e7f8f1cab5d1eb9e06553a8a7f2ac98a030e6c1d1ca401f9`  
		Last Modified: Thu, 11 Jun 2026 04:59:58 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-trixie` - unknown; unknown

```console
$ docker pull ruby@sha256:a2177505a723c2dd1b5fb367aa1188afa7515ae19b36b7d8ba241561923d90f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17343972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a123153deb6f8d9d27492f3155dad9c47ed84d0b888ae12b77ad592bbe0c53a`

```dockerfile
```

-	Layers:
	-	`sha256:999da4149904c882b0c319be8213e5a6a119adbe3567755728dfe768ccf14a03`  
		Last Modified: Thu, 11 Jun 2026 04:59:59 GMT  
		Size: 17.3 MB (17321644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c04ec1e34e6cb2b8405e7418cf888dbf77167fcd61f2a5bdb4d1afbfc3752be`  
		Last Modified: Thu, 11 Jun 2026 04:59:58 GMT  
		Size: 22.3 KB (22328 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-trixie` - linux; arm variant v5

```console
$ docker pull ruby@sha256:f2990ad7f555c0ede3b9dba4e1149f1b08bcc82048a8f9ada7c7f105f70ed9f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **381.1 MB (381146074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e59885b0c32b733e56c3348d3985bca49108826933907164571c7ab24e1761b4`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 01:21:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 02:46:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 03:17:15 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 05:57:22 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 11 Jun 2026 05:59:52 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 05:59:52 GMT
ENV RUBY_VERSION=3.4.9
# Thu, 11 Jun 2026 05:59:52 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Thu, 11 Jun 2026 05:59:52 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Thu, 11 Jun 2026 05:59:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 11 Jun 2026 05:59:52 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 11 Jun 2026 05:59:52 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 11 Jun 2026 05:59:52 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 05:59:52 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 11 Jun 2026 05:59:52 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:f4fdc449648c31ec97234c27647662108b2d6bce3fe83032a1af88265bf2ff35`  
		Last Modified: Wed, 10 Jun 2026 23:40:32 GMT  
		Size: 47.5 MB (47494811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d3be6b9d9888f84dbe643ff398f469da8712a1ac207b5975f98e812dad9062c`  
		Last Modified: Thu, 11 Jun 2026 01:21:44 GMT  
		Size: 24.4 MB (24364313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8792c8246eb40706682474cfe0f7440cebb3cc0986b9ca229c49e962ffcf1a6`  
		Last Modified: Thu, 11 Jun 2026 02:47:03 GMT  
		Size: 65.3 MB (65343335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f7b86ea0c9c12834d9987a5aba7edb243efd890b016aa990296ef6c59ec8764`  
		Last Modified: Thu, 11 Jun 2026 03:18:03 GMT  
		Size: 205.9 MB (205901022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f501bb5304c2ca1b2e27f9f5e552455cc25a98d506690f754d93c51b27fe60d1`  
		Last Modified: Thu, 11 Jun 2026 06:00:12 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1730a7f77f68f6243150f4ee51e35e1f6615026037fb06c606a9f7476c363d2c`  
		Last Modified: Thu, 11 Jun 2026 06:00:15 GMT  
		Size: 38.0 MB (38042261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffa535da3ea63254dfc445b47271c68f06c0451f8b2a189b17bbc06af37f313f`  
		Last Modified: Thu, 11 Jun 2026 06:00:13 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-trixie` - unknown; unknown

```console
$ docker pull ruby@sha256:4de3aa528aa53b621f9de69b51c7eeee6df6aad2ae601bddb5f7595b2bec5e39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17106316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e4a9fec46d769cacf65351708d2e0a7d252d777678dbc24970b34851122c833`

```dockerfile
```

-	Layers:
	-	`sha256:d48b0fe9cfb9e4001ae9240fa7cb5ee383de0643d86785ef0230d2a86dca68d6`  
		Last Modified: Thu, 11 Jun 2026 06:00:14 GMT  
		Size: 17.1 MB (17083866 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c3227e4c89afce49993b0f1350191433744537d19813ca93eaa283e33995b13`  
		Last Modified: Thu, 11 Jun 2026 06:00:13 GMT  
		Size: 22.4 KB (22450 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-trixie` - linux; arm variant v7

```console
$ docker pull ruby@sha256:9e7cda790dd89974fafc21ad86063f4196d4eea2ae860611492b0bef47ccdf27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.5 MB (363519869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84a4b202aaecc1170b5b4a0bc5c5104fddc02e068380cb8d7c86d7cf1526e963`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 01:27:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 02:45:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 03:20:35 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 06:21:23 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 11 Jun 2026 06:23:38 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 06:23:38 GMT
ENV RUBY_VERSION=3.4.9
# Thu, 11 Jun 2026 06:23:38 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Thu, 11 Jun 2026 06:23:38 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Thu, 11 Jun 2026 06:23:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 11 Jun 2026 06:23:38 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 11 Jun 2026 06:23:38 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 11 Jun 2026 06:23:38 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 06:23:38 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 11 Jun 2026 06:23:38 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:df041f2d52cc5410fddc569f8ab35cdfdd35a38e037f7aab971e409724bfd203`  
		Last Modified: Wed, 10 Jun 2026 23:42:20 GMT  
		Size: 45.7 MB (45748641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04879054973f6f0ae366a776f1ee6e23a5ae9b6072a5861ec514fdf29f7dbd68`  
		Last Modified: Thu, 11 Jun 2026 01:27:20 GMT  
		Size: 23.6 MB (23635995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5e960af1a374080feee4d695210e1cc29cde28cd70c56fad7cb555534519a7e`  
		Last Modified: Thu, 11 Jun 2026 02:45:25 GMT  
		Size: 62.7 MB (62746530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cac73cee70686b08f055d8018f863fcf7893405b9bdfc486e8925b277b27f125`  
		Last Modified: Thu, 11 Jun 2026 03:21:13 GMT  
		Size: 193.5 MB (193489305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72206dbe7f981f758d7cb2d6cef8df5afa11aa62fcbe776257d30e4b77e8ede3`  
		Last Modified: Thu, 11 Jun 2026 06:23:57 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed889a2175f954888113b7c1e78a0d9745c40e898e1ae3df2077e356e2052ef`  
		Last Modified: Thu, 11 Jun 2026 06:23:59 GMT  
		Size: 37.9 MB (37899067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98f4f372fbae6c53a7679f34f9d5badb41d7e3aed8a9e4323508638fb18aacb3`  
		Last Modified: Thu, 11 Jun 2026 06:23:57 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-trixie` - unknown; unknown

```console
$ docker pull ruby@sha256:5fe3a1ef1acdce4debb0b9960ec7945e7443c9ce1064b2e8a2f62fb145fc7f77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17112106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:684cfbf0e9f0cdb1aa9dc0bef2a7278b96be7f200f7abb9a56ac75c60812b879`

```dockerfile
```

-	Layers:
	-	`sha256:7c29ef55a13a94b8cda58d1c4e9233d8c455d9cb005bcceb36b8c2ba12980dcd`  
		Last Modified: Thu, 11 Jun 2026 06:23:58 GMT  
		Size: 17.1 MB (17089656 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9912937ffc8b7007e2621a67aff894521ca3a03d5f98476eb824722cf9be4b5`  
		Last Modified: Thu, 11 Jun 2026 06:23:57 GMT  
		Size: 22.4 KB (22450 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-trixie` - linux; arm64 variant v8

```console
$ docker pull ruby@sha256:9b02ee727046bf93cbaf85f7f3350382d87bfc9446adff4da4162b9b0ae08fe3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **410.8 MB (410840992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e51c49352b05dbda5b391927d5871f5a6c0af4ee7e0f222bf83c3e4285e2a7ea`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:44:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 02:22:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 03:16:43 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 05:06:06 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 11 Jun 2026 05:08:12 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 05:08:12 GMT
ENV RUBY_VERSION=3.4.9
# Thu, 11 Jun 2026 05:08:12 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Thu, 11 Jun 2026 05:08:12 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Thu, 11 Jun 2026 05:08:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 11 Jun 2026 05:08:12 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 11 Jun 2026 05:08:12 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 11 Jun 2026 05:08:12 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 05:08:12 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 11 Jun 2026 05:08:12 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:ed660e1af0f5da9e93a4c43fb29e86cb46fe69c76bcf11a3de9c57c987acab82`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 49.7 MB (49678169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd2ab02859108b91c1c26f2badd015b5215eb066b7ef4f3a22bd1536a8debe96`  
		Last Modified: Thu, 11 Jun 2026 00:44:32 GMT  
		Size: 25.0 MB (25026911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f2e427d8856f71d8d3667d1c4d9274b8aca2bd9d228387c51c211909e51263f`  
		Last Modified: Thu, 11 Jun 2026 02:22:21 GMT  
		Size: 67.6 MB (67599934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df3bbd0b4297d07a9ba4bb3bfa1d7d9179e010ad584caad22d552ff94eb33b93`  
		Last Modified: Thu, 11 Jun 2026 03:17:28 GMT  
		Size: 226.3 MB (226344743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed60b893824247023d58d12b595ffd451c29126cca9422400db3094000631229`  
		Last Modified: Thu, 11 Jun 2026 05:08:33 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4871b7cdff44d05412be861f690444dd3b37d724d4da6050efc267ccf2bb5972`  
		Last Modified: Thu, 11 Jun 2026 05:08:35 GMT  
		Size: 42.2 MB (42190903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00d9d33f7a3aa6a927ce1ad91e2d3153cc705f1838324af40d16305f6ad1d9e4`  
		Last Modified: Thu, 11 Jun 2026 05:08:33 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-trixie` - unknown; unknown

```console
$ docker pull ruby@sha256:fa99f300e8c2d4ee1aadea827679496a128a29873b53707292aa591a19a700fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 MB (17427823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43558f3ebf9c67715ed02ba5970e1a101bf499e161e5f98eaaaaf903d2aab370`

```dockerfile
```

-	Layers:
	-	`sha256:1915a946b96bef6e8ab9aebae44d36bddb35938dc15d8018bbf8430ecc5ecf4c`  
		Last Modified: Thu, 11 Jun 2026 05:08:34 GMT  
		Size: 17.4 MB (17405337 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25eeff640db56c481d8d7dc6dc5f048aca1b8c361067f5aefa513f666ed799e4`  
		Last Modified: Thu, 11 Jun 2026 05:08:33 GMT  
		Size: 22.5 KB (22486 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-trixie` - linux; 386

```console
$ docker pull ruby@sha256:821d0799613999231f1561267214a85e53f7943864a103960d0acc6141b93af0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **425.5 MB (425537333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d329eb492f6650805655ee6ccea9f54e6b3eea0fd809a36aca0d92f7b68d3c19`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:45:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 02:24:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 03:17:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 04:41:17 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 11 Jun 2026 04:43:31 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 04:43:31 GMT
ENV RUBY_VERSION=3.4.9
# Thu, 11 Jun 2026 04:43:31 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Thu, 11 Jun 2026 04:43:31 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Thu, 11 Jun 2026 04:43:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 11 Jun 2026 04:43:31 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 11 Jun 2026 04:43:31 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 11 Jun 2026 04:43:31 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 04:43:31 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 11 Jun 2026 04:43:31 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:b32240bef83f1a91259785f4f0dac80386c2d42ea09a3339118c915f47000b2f`  
		Last Modified: Wed, 10 Jun 2026 23:40:31 GMT  
		Size: 50.8 MB (50835563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f54ac1ec51d3293c1ade0065529ca23d5fc365d00997ff4e5a290cef3692dc04`  
		Last Modified: Thu, 11 Jun 2026 00:45:24 GMT  
		Size: 26.8 MB (26797651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90e0028665ad759d9a734f0342c043d69fa3d024141c3329c900f163c639953f`  
		Last Modified: Thu, 11 Jun 2026 02:25:16 GMT  
		Size: 69.8 MB (69823550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f398ec52d006b7e150c01db07e84aaa4183c30e7fc5a4bf0eb653a31cc3531`  
		Last Modified: Thu, 11 Jun 2026 03:18:01 GMT  
		Size: 240.3 MB (240309514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5bd4a6830770a3bb32ef3c81a20db5a8be5f5445239a97744dc7b85c465148a`  
		Last Modified: Thu, 11 Jun 2026 04:43:56 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49b0365f87324fbe0df0013a3d373f64483e65cc90d11ad64a2ee1ab12b70e17`  
		Last Modified: Thu, 11 Jun 2026 04:43:57 GMT  
		Size: 37.8 MB (37770721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aaf1f9be70eb07d27e3a902d715b942f353fe4fc2cf8a61dc6bb7cdd4de649f`  
		Last Modified: Thu, 11 Jun 2026 04:43:56 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-trixie` - unknown; unknown

```console
$ docker pull ruby@sha256:d63391af567742c1c2afd85b96c9d03175bb46d50ca5a0ee5a98376cc91430aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17313509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7505665b8ee65da2d268969828a0c6549958b4fc03e3303e31dd14b6a9bcf6a1`

```dockerfile
```

-	Layers:
	-	`sha256:98e18d1650a9aa86d7f5f648f5567f5c5d9c2d73277bc40c671160835cee228a`  
		Last Modified: Thu, 11 Jun 2026 04:43:56 GMT  
		Size: 17.3 MB (17291228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3720130ec843a961e337868d8ea6448d52d69cf78954fc139ef653a2c06956ef`  
		Last Modified: Thu, 11 Jun 2026 04:43:56 GMT  
		Size: 22.3 KB (22281 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-trixie` - linux; ppc64le

```console
$ docker pull ruby@sha256:9ef9487d4c7088d3683d5bd841cecf7af53ae1876de0f115be421527eb3b18ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **424.1 MB (424131155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08e07fb74533df2ca920e5e7b04ab42e532ac942db80a805e37aecade34c1fca`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 01:14:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 06:52:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 09:10:35 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 16:38:05 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 20 May 2026 16:48:37 GMT
ENV LANG=C.UTF-8
# Wed, 20 May 2026 16:48:37 GMT
ENV RUBY_VERSION=3.4.9
# Wed, 20 May 2026 16:48:37 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Wed, 20 May 2026 16:48:37 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Wed, 20 May 2026 16:48:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 20 May 2026 16:48:37 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 20 May 2026 16:48:37 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 20 May 2026 16:48:37 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 16:48:38 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 20 May 2026 16:48:38 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:55497c62a793e62a2e78a3fd85fcedf060da73e331ad107733199ea991106b96`  
		Last Modified: Tue, 19 May 2026 22:37:59 GMT  
		Size: 53.1 MB (53132182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:743dcca676e80d0b7074d4f03820f8068053078d4942f2a921fdf172c62897ae`  
		Last Modified: Wed, 20 May 2026 01:14:53 GMT  
		Size: 27.0 MB (27021149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7396fcf223bd659e5dda1b961ab403e3df6f9d118708751addc02badc2015799`  
		Last Modified: Wed, 20 May 2026 06:53:00 GMT  
		Size: 73.0 MB (73042459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06bf5baaa69eb61df93cfa5666d94d0c8ad399bda9d0ffc7582002bfe76ba1b4`  
		Last Modified: Wed, 20 May 2026 09:11:54 GMT  
		Size: 231.3 MB (231309802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3a827019ca6a075a777f97c71322790638e3439d836c137831fd0925eb9a36c`  
		Last Modified: Wed, 20 May 2026 16:43:18 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14a76900364680985d7b59409298258768dbc3378c7b7789da427636eb25f5d3`  
		Last Modified: Wed, 20 May 2026 16:49:42 GMT  
		Size: 39.6 MB (39625230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e47e2b29d3a9a82330508c436877354a54b7990f2ad4d15ada808ca8e593bd90`  
		Last Modified: Wed, 20 May 2026 16:49:41 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-trixie` - unknown; unknown

```console
$ docker pull ruby@sha256:021f3cb94500f7f50ce319436b0c7aa9d94692c56e8ef29c9a961c5e82381ad9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17329371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1492cf96ef0147d8cc3354c821938c5643f4784b08f72df42034b87e9834d119`

```dockerfile
```

-	Layers:
	-	`sha256:0c8316290e4d283810c01f11279c5ec281d2538fa9d607db56ed7c18957b0d03`  
		Last Modified: Wed, 20 May 2026 16:49:42 GMT  
		Size: 17.3 MB (17306983 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7cdab59b496f9173261d8113accc7b81e9c051941fa360d159e27e230d5138a6`  
		Last Modified: Wed, 20 May 2026 16:49:41 GMT  
		Size: 22.4 KB (22388 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-trixie` - linux; riscv64

```console
$ docker pull ruby@sha256:269073a1a4481ec974674462e1c85e705eed2ea9162428b259f774d1f47a329f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **501.4 MB (501403240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52118160069e0198b23c1eb9376b1b3f64331d40bf37c5f2c87f18bfd505a3c3`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1779062400'
# Thu, 21 May 2026 14:01:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Sat, 23 May 2026 06:47:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Sun, 24 May 2026 16:10:35 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Mon, 25 May 2026 15:38:39 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Mon, 25 May 2026 19:50:19 GMT
ENV LANG=C.UTF-8
# Mon, 25 May 2026 19:50:19 GMT
ENV RUBY_VERSION=3.4.9
# Mon, 25 May 2026 19:50:19 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Mon, 25 May 2026 19:50:19 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Mon, 25 May 2026 19:50:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Mon, 25 May 2026 19:50:19 GMT
ENV GEM_HOME=/usr/local/bundle
# Mon, 25 May 2026 19:50:19 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Mon, 25 May 2026 19:50:19 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 25 May 2026 19:50:19 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Mon, 25 May 2026 19:50:19 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:e6afb0d9fe2fdfebacf2ccb9782fd129d9e416f637c13f72c2f0427e69c04c88`  
		Last Modified: Tue, 19 May 2026 23:49:54 GMT  
		Size: 47.8 MB (47796268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0db76586e2d1a29e7feb120e0fcc7fa49e8df54823efd2e1b4e13ca0fe4ab60d`  
		Last Modified: Thu, 21 May 2026 14:02:51 GMT  
		Size: 25.0 MB (24966381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:244bfe91065712f707f8614b6bb5478bb453a0332b440e47735c29ab8e1ac33e`  
		Last Modified: Sat, 23 May 2026 06:51:24 GMT  
		Size: 66.7 MB (66673209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a8f35c8d582e48fd3c4a67d2b915e9d1e65af5e2b508fad51fd8349c7c518af`  
		Last Modified: Sun, 24 May 2026 16:26:19 GMT  
		Size: 323.9 MB (323891607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8709dae68c51a6b078a3a98d9102c24872f580b7a8e65a0b2d863e59bee223d`  
		Last Modified: Mon, 25 May 2026 17:42:09 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a78708b7f51285da48057e1cb6c5d7af2bb932e6f0426c6f3aff383c146d9314`  
		Last Modified: Mon, 25 May 2026 19:58:37 GMT  
		Size: 38.1 MB (38075443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35fd5977b4f36e0b254dcd3bc6665f87ba4301a995949d604800969dd1781f80`  
		Last Modified: Mon, 25 May 2026 19:58:29 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-trixie` - unknown; unknown

```console
$ docker pull ruby@sha256:f8664bff48abc9423efe322e8433adba1e616eb95ff985b6e57dae38cdde7e13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 MB (17400157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec40e256ed520c42bf46f235dae6659bb14d4956003235b1d8e35988bca4a2cb`

```dockerfile
```

-	Layers:
	-	`sha256:16bc534a38b9df741b2a7476c7e19a4c05da1b282b6529578852272f75bea70b`  
		Last Modified: Mon, 25 May 2026 19:58:34 GMT  
		Size: 17.4 MB (17377770 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b336efd568a98507b30153fd6f56d92813cf29d62a44a3b872ac976a31e16267`  
		Last Modified: Mon, 25 May 2026 19:58:28 GMT  
		Size: 22.4 KB (22387 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-trixie` - linux; s390x

```console
$ docker pull ruby@sha256:4093fa9298b54b9c0903ded0053ffb10f89bb19341864282608818ed3bdcf98c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **390.9 MB (390873852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c24fd4008da911b74e675026f760c526382ef5d6e8fc5f4d322b16bdf73c631e`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 01:44:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 03:26:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 04:14:58 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 08:55:49 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 11 Jun 2026 09:03:24 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 09:03:24 GMT
ENV RUBY_VERSION=3.4.9
# Thu, 11 Jun 2026 09:03:24 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Thu, 11 Jun 2026 09:03:24 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Thu, 11 Jun 2026 09:03:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 11 Jun 2026 09:03:24 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 11 Jun 2026 09:03:24 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 11 Jun 2026 09:03:24 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 09:03:24 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 11 Jun 2026 09:03:24 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:0ebf827318debac5b829e4cd5c36e0122490cf2392f532aa02b2b0999d5c1b37`  
		Last Modified: Wed, 10 Jun 2026 23:42:35 GMT  
		Size: 49.4 MB (49385897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b58925113278ed74d68122ff77b22976b064cb872b273063a3ab182209055ee`  
		Last Modified: Thu, 11 Jun 2026 01:44:45 GMT  
		Size: 26.8 MB (26803918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c67e4e83aa860c5b719a4e0cc01db908ae525049821b3c459f866ed434f070e`  
		Last Modified: Thu, 11 Jun 2026 03:27:03 GMT  
		Size: 68.7 MB (68653348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5ee4e18810194ccfb4c065c512c41bbd68891231f3d39485a8c21bfe151d5c2`  
		Last Modified: Thu, 11 Jun 2026 04:15:57 GMT  
		Size: 206.7 MB (206707893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dfb53e544aeafe7c6df262440b9a0cc69b7f3cf9068996af88acc286ed26986`  
		Last Modified: Thu, 11 Jun 2026 08:58:45 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c2b5285e570533ced13819e5ec69e28d5cd903af68bf36bad87c2bbb709d0e7`  
		Last Modified: Thu, 11 Jun 2026 09:04:00 GMT  
		Size: 39.3 MB (39322463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5975d51ee88aa4a1cf7d88eb76473de7edd7f4868ecaf976e7f9e02134941cdf`  
		Last Modified: Thu, 11 Jun 2026 09:03:59 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-trixie` - unknown; unknown

```console
$ docker pull ruby@sha256:dc7c9a21018dc4c5ec2153bed8e59e8ee7256d0b542ce7aae79ae2c3499265d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17121204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fb8dd95457cf2107caa26343e28bbdaa18f5ac17ca0c809f81904a8d6f73da2`

```dockerfile
```

-	Layers:
	-	`sha256:66d9b364d489c181a86dbe980855450f278e5e5606e8bc0b5f0f77efae0b3cdf`  
		Last Modified: Thu, 11 Jun 2026 09:03:59 GMT  
		Size: 17.1 MB (17098877 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f195bdbf6052d013d79d1f9b6fa6456aa6cbd60103cf25a0480755489629fe7`  
		Last Modified: Thu, 11 Jun 2026 09:03:59 GMT  
		Size: 22.3 KB (22327 bytes)  
		MIME: application/vnd.in-toto+json
