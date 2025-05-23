## `ruby:latest`

```console
$ docker pull ruby@sha256:b92f553dd84fe32a5b9db7035d82930e3045828846595310219815c2abeb42d4
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

### `ruby:latest` - linux; amd64

```console
$ docker pull ruby@sha256:e209295996f9da3f687b1f1f6956705945042f1986f93c61d17fdfa5515139a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.7 MB (389741655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4351ba9d9918f17a5c6ef03c76a6c1922bcb711d002e090fae90114da802be3f`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 May 2025 23:03:19 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 14 May 2025 23:03:19 GMT
ENV LANG=C.UTF-8
# Wed, 14 May 2025 23:03:19 GMT
ENV RUBY_VERSION=3.4.4
# Wed, 14 May 2025 23:03:19 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.4.tar.xz
# Wed, 14 May 2025 23:03:19 GMT
ENV RUBY_DOWNLOAD_SHA256=f76d63efe9499dedd8526b74365c0c811af00dc9feb0bed7f5356488476e28f4
# Wed, 14 May 2025 23:03:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 14 May 2025 23:03:19 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 14 May 2025 23:03:19 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 14 May 2025 23:03:19 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 May 2025 23:03:19 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 14 May 2025 23:03:19 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:3e6b9d1a95114e19f12262a4e8a59ad1d1a10ca7b82108adcf0605a200294964`  
		Last Modified: Wed, 21 May 2025 22:27:42 GMT  
		Size: 48.5 MB (48488245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37927ed901b1b2608b72796c6881bf645480268eca4ac9a37b9219e050bb4d84`  
		Last Modified: Wed, 21 May 2025 23:20:21 GMT  
		Size: 24.0 MB (24015635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b2f47ad4443652b9b5cc81a95ede249fd976310efdbee159f29638783778c0`  
		Last Modified: Wed, 21 May 2025 23:37:25 GMT  
		Size: 64.4 MB (64399858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e23f099911d692f62b851cf49a1e93294288a115f5cd2d014180e4d3684d34ab`  
		Last Modified: Thu, 22 May 2025 00:12:38 GMT  
		Size: 211.4 MB (211362119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac675c320b8675c50728c6baf5f47255ea779d44bf2376e3a07ee0039ed6ca0a`  
		Last Modified: Thu, 22 May 2025 01:25:10 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bcd789427f3e74c34be9d0a82c811605154823a429300abcb0115a4bc3a0bd4`  
		Last Modified: Thu, 22 May 2025 01:25:11 GMT  
		Size: 41.5 MB (41475466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84936d5a32de1ccec7ae740032267fe38c504f19247c4a89fe6bac3a82641acb`  
		Last Modified: Thu, 22 May 2025 01:25:10 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:latest` - unknown; unknown

```console
$ docker pull ruby@sha256:94fe5d0df33eaa712b39f08b4a6011cb1671c657141cbd1316b8f96e701a972a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15708966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1708fde48c4e81696d6fc618770235b92f0f017103f8090cdea3ce0867df1b07`

```dockerfile
```

-	Layers:
	-	`sha256:4bfd49363c14d4707237ebd22e55f1fb4a4a61f8b47c0be407691a9c4fe07e1e`  
		Last Modified: Thu, 22 May 2025 01:25:10 GMT  
		Size: 15.7 MB (15686297 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f11e0475b471db7709cc2a9206be85dd904f2f6e9635f6da25021aa24331179`  
		Last Modified: Thu, 22 May 2025 01:25:10 GMT  
		Size: 22.7 KB (22669 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:latest` - linux; arm variant v5

```console
$ docker pull ruby@sha256:cf590e15cb3454e0cf8bfea054f2a65c5913d3c023d2c5b03f7aa289719192fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.6 MB (352589360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba1bd04a18dc1dbbc9bda0e7256f4057d221cb8af2a1555e3aa9d3f92f229d9c`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1747699200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 May 2025 23:03:19 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 14 May 2025 23:03:19 GMT
ENV LANG=C.UTF-8
# Wed, 14 May 2025 23:03:19 GMT
ENV RUBY_VERSION=3.4.4
# Wed, 14 May 2025 23:03:19 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.4.tar.xz
# Wed, 14 May 2025 23:03:19 GMT
ENV RUBY_DOWNLOAD_SHA256=f76d63efe9499dedd8526b74365c0c811af00dc9feb0bed7f5356488476e28f4
# Wed, 14 May 2025 23:03:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 14 May 2025 23:03:19 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 14 May 2025 23:03:19 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 14 May 2025 23:03:19 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 May 2025 23:03:19 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 14 May 2025 23:03:19 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:d34b66573dd99436757429c603646ae3e6d1948a3fa85413a39cf069620a7229`  
		Last Modified: Wed, 21 May 2025 22:27:39 GMT  
		Size: 46.0 MB (46021484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a2b51cc5977be0e2fae0a0314b991e4f90fafc6823a929775d09884dc18bcd7`  
		Last Modified: Thu, 22 May 2025 01:13:36 GMT  
		Size: 22.7 MB (22694185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:662df94d663c1ee85e74f3b73f3f19049f9727ed40e72aa3497df0e6f9da2a46`  
		Last Modified: Thu, 22 May 2025 04:44:17 GMT  
		Size: 62.0 MB (61998014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8567f3e20a3cd49e5c90cc3030da69c78ab60ff177b208c180331479f5965090`  
		Last Modified: Thu, 22 May 2025 06:35:21 GMT  
		Size: 184.6 MB (184635154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebe419b62093293268f22d6bd64924d79be4255563fd397a23ce41082cb918a9`  
		Last Modified: Thu, 22 May 2025 12:23:24 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:474ab15ba0bc68d6420cbc164f628ad5b0ad0c5707d97689f087e67b4458c955`  
		Last Modified: Thu, 22 May 2025 12:26:51 GMT  
		Size: 37.2 MB (37240190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:138a5418950d46123af9e70c4895e09054337b3e8aeec7f543daaa49d309680a`  
		Last Modified: Thu, 22 May 2025 12:26:49 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:latest` - unknown; unknown

```console
$ docker pull ruby@sha256:c1bb5ea7b4ddc3d337274035fc0f9f8b591d5eb19b4737306901a5ed06b9e902
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15506131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:460cb63f8e57863bd75db90dd64c15c7c58f6cdc45cdea038046939ae2743d0e`

```dockerfile
```

-	Layers:
	-	`sha256:3de1e0f8baac972efc004b02902ce77edd975afb23d2fcb19c59941ec0279e47`  
		Last Modified: Thu, 22 May 2025 12:26:50 GMT  
		Size: 15.5 MB (15483328 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e917a3c12af2f7d5b89c3de2ffd59b6b9afb6a98f337559eafc4750fe9c9d857`  
		Last Modified: Thu, 22 May 2025 12:26:49 GMT  
		Size: 22.8 KB (22803 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:latest` - linux; arm variant v7

```console
$ docker pull ruby@sha256:a9b62aa9b17116f5feaf81149d6e8e1b2440e71b9a147970963670c378fbf1c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.2 MB (338152237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e775aacd58bc8fd6d705cacf6d6e482e21413ff546b586c1dc715ebba07db82`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1747699200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 May 2025 23:03:19 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 14 May 2025 23:03:19 GMT
ENV LANG=C.UTF-8
# Wed, 14 May 2025 23:03:19 GMT
ENV RUBY_VERSION=3.4.4
# Wed, 14 May 2025 23:03:19 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.4.tar.xz
# Wed, 14 May 2025 23:03:19 GMT
ENV RUBY_DOWNLOAD_SHA256=f76d63efe9499dedd8526b74365c0c811af00dc9feb0bed7f5356488476e28f4
# Wed, 14 May 2025 23:03:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 14 May 2025 23:03:19 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 14 May 2025 23:03:19 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 14 May 2025 23:03:19 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 May 2025 23:03:19 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 14 May 2025 23:03:19 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:3a781f536825e084b88c231841be4d1c7df016a4aa2ebdd27d7431b5f1ab3419`  
		Last Modified: Wed, 21 May 2025 22:27:37 GMT  
		Size: 44.2 MB (44202771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b02150b4002b569f2f9be5055a06c94a228e07937f6f39fd4d84b52042b2f01`  
		Last Modified: Thu, 22 May 2025 02:28:04 GMT  
		Size: 21.9 MB (21924635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2c061a668a2586bc3366d21d8a069b30ac6fdff27bb5140a653d59b71241213`  
		Last Modified: Thu, 22 May 2025 12:11:29 GMT  
		Size: 59.7 MB (59656286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a22ee2db9f8d2ea3317ceb36f4b9bc7895f6cb8402903d639c8083eaec948450`  
		Last Modified: Thu, 22 May 2025 15:31:57 GMT  
		Size: 175.3 MB (175297793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:156fb86f72a9c3b08ac2426e3db59296da5bc877f83fb128af0a15719d8c52a4`  
		Last Modified: Fri, 23 May 2025 03:00:56 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:276a38bb573251043e4006a152ce6ac3dec0ab01cd6d4ab8c1dd7f522c1e2c96`  
		Last Modified: Fri, 23 May 2025 03:06:53 GMT  
		Size: 37.1 MB (37070421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0120d3a9dca1670ed250ba1ebdf090093a3ceaa3011f84319c1e4d6b10bf3d95`  
		Last Modified: Fri, 23 May 2025 03:06:51 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:latest` - unknown; unknown

```console
$ docker pull ruby@sha256:67c8b0b226f24617e6e0944694745acb63a21d9f0f4d07085e371fdb8e34bf4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15511605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:026b3664f462bda46f441074d1696fd708c0bd86900675a3603d4130f1dd7725`

```dockerfile
```

-	Layers:
	-	`sha256:e7eec9bb26257751524c0ad7417c3b9a599e1a6d30e59b08f251d1ac2f7315d6`  
		Last Modified: Fri, 23 May 2025 03:06:52 GMT  
		Size: 15.5 MB (15488802 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a04cc4654b0efbd043a217abd4e7294a267f98e461b97ee62eaa9fa8d3fe41c`  
		Last Modified: Fri, 23 May 2025 03:06:51 GMT  
		Size: 22.8 KB (22803 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:latest` - linux; arm64 variant v8

```console
$ docker pull ruby@sha256:5bb5ff87bfd4585a3d82dadab094c494d816ede7b666b2c26a59ea438b10760e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **380.4 MB (380398618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac62bff25a39da35e78dd67a9a3fbe03ffb078792be0e869c0eb4812ac3f4458`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 May 2025 23:03:19 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 14 May 2025 23:03:19 GMT
ENV LANG=C.UTF-8
# Wed, 14 May 2025 23:03:19 GMT
ENV RUBY_VERSION=3.4.4
# Wed, 14 May 2025 23:03:19 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.4.tar.xz
# Wed, 14 May 2025 23:03:19 GMT
ENV RUBY_DOWNLOAD_SHA256=f76d63efe9499dedd8526b74365c0c811af00dc9feb0bed7f5356488476e28f4
# Wed, 14 May 2025 23:03:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 14 May 2025 23:03:19 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 14 May 2025 23:03:19 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 14 May 2025 23:03:19 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 May 2025 23:03:19 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 14 May 2025 23:03:19 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:1a12b4ea7c0ce04aa0e98be0a8c9942162bac71426f734fe6d3bf988bc9e2627`  
		Last Modified: Wed, 21 May 2025 22:27:39 GMT  
		Size: 48.3 MB (48327181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:280bbe393e788ced1dcb033580604b24de083601624337be66b3ec31781dae40`  
		Last Modified: Thu, 22 May 2025 02:47:26 GMT  
		Size: 23.6 MB (23551398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f4f297e4f699ae0f384d5cc1ea42065f58a115aa0a634d427cbb186f91cb4d0`  
		Last Modified: Thu, 22 May 2025 09:17:58 GMT  
		Size: 64.4 MB (64361989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b58ee5cb7152015437e4a9b3066ae9e25a26a3bef6617d0b7f25368511c2d954`  
		Last Modified: Thu, 22 May 2025 12:26:26 GMT  
		Size: 202.8 MB (202762554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:068f48871ce1606ccda1f9f81ceaa701c52188bc411af9397fb88e457f26dcfe`  
		Last Modified: Thu, 22 May 2025 19:37:47 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bee08f06c8791bb26766480b73f7eeca82e9082c02daee004c12271b3f70477`  
		Last Modified: Thu, 22 May 2025 19:43:21 GMT  
		Size: 41.4 MB (41395164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:259c98299e2cb4b4da4abf10df13af9cb1ad3f8a386cc73f3769cef50c8005bb`  
		Last Modified: Thu, 22 May 2025 19:43:19 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:latest` - unknown; unknown

```console
$ docker pull ruby@sha256:e405fe0cfd0ecefcde8ab0b8ad0dc22af1af3a77c791af92eb02deb0c3191648
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15737721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65c4ccfe126ebd1be97b30c504cc184252352e24bc2a1d9bb809d06485eaf983`

```dockerfile
```

-	Layers:
	-	`sha256:619d6db829bcb5ed8f2edaa426892a3f3c265268ce33adf5d1adae5bc29e455b`  
		Last Modified: Thu, 22 May 2025 19:43:20 GMT  
		Size: 15.7 MB (15714870 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9fc9efabe44ed2da5d15284229889cf9913f64160b5a91125a58a0c05201eb2c`  
		Last Modified: Thu, 22 May 2025 19:43:19 GMT  
		Size: 22.9 KB (22851 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:latest` - linux; 386

```console
$ docker pull ruby@sha256:d489e215442d6ae21738413fe0c2db2cec51c8af4247b6c848673d6843511c10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **387.9 MB (387917956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2105ebdeac13122f95341159f039013a61f175fff43497dd728bb66be5acf99`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1747699200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 May 2025 23:03:19 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 14 May 2025 23:03:19 GMT
ENV LANG=C.UTF-8
# Wed, 14 May 2025 23:03:19 GMT
ENV RUBY_VERSION=3.4.4
# Wed, 14 May 2025 23:03:19 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.4.tar.xz
# Wed, 14 May 2025 23:03:19 GMT
ENV RUBY_DOWNLOAD_SHA256=f76d63efe9499dedd8526b74365c0c811af00dc9feb0bed7f5356488476e28f4
# Wed, 14 May 2025 23:03:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 14 May 2025 23:03:19 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 14 May 2025 23:03:19 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 14 May 2025 23:03:19 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 May 2025 23:03:19 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 14 May 2025 23:03:19 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:7bdd0d6ce898fe017a461e5f67ccf41a15f147063ffe1c496fb7e5f75037adfb`  
		Last Modified: Wed, 21 May 2025 22:27:49 GMT  
		Size: 49.5 MB (49471562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:296134322e370a0aab10509f2b47d9ce416e7da5a792e7f8badd9284ecbabeb0`  
		Last Modified: Wed, 21 May 2025 23:20:06 GMT  
		Size: 24.9 MB (24855668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cc8c7f8292580c2c70e8cb47ec957249f0882ee6ee3737bf3250e44650a38db`  
		Last Modified: Wed, 21 May 2025 23:37:30 GMT  
		Size: 66.2 MB (66224115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e426a3a2617e34e93d75e9b5c79113e976623e3633255f578a7087d4221ba47`  
		Last Modified: Thu, 22 May 2025 00:12:45 GMT  
		Size: 210.3 MB (210303724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1d6e3a926b2f7a7ffc9bbbc381342efdcde3a1d9628380a65b0d06911e1c8cb`  
		Last Modified: Thu, 22 May 2025 01:21:24 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bfd7392b9eb2fda284a370f316d471888e1f9d494ff594d7a8edb5884fd35c7`  
		Last Modified: Thu, 22 May 2025 01:21:25 GMT  
		Size: 37.1 MB (37062556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:944f248ac8083e3ab00ec7f944a4108eb1890aaf164ec9c77f3f05b525aaf613`  
		Last Modified: Thu, 22 May 2025 01:21:24 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:latest` - unknown; unknown

```console
$ docker pull ruby@sha256:9dd7171dfec678ba640ef93bfa2150e32908a9da4a523a27a5234c265c709b52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15687113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abd74130ca28191f8cb4c56a5d0fc33b08b960f0f5fb6b0f05b20371bd5d95ea`

```dockerfile
```

-	Layers:
	-	`sha256:020b3edea260a0ee25a74e54102ca3c421ab109a1bcc6b299d9a3e00becc7ade`  
		Last Modified: Thu, 22 May 2025 01:21:25 GMT  
		Size: 15.7 MB (15664500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d17ffb1ca9e47e07ab6030f82e03d77600ace390095884a30c2486110e6775f9`  
		Last Modified: Thu, 22 May 2025 01:21:23 GMT  
		Size: 22.6 KB (22613 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:latest` - linux; mips64le

```console
$ docker pull ruby@sha256:e73bc071b630b442b21951f4691c2313b9c6e4dbfd0873bf05f032176fd49564
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.1 MB (364091869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40d649de041d4de0c713e230cbe234c14d8a6d36be4d86dfb218f4ee8fb2b2db`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 May 2025 23:03:19 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 14 May 2025 23:03:19 GMT
ENV LANG=C.UTF-8
# Wed, 14 May 2025 23:03:19 GMT
ENV RUBY_VERSION=3.4.4
# Wed, 14 May 2025 23:03:19 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.4.tar.xz
# Wed, 14 May 2025 23:03:19 GMT
ENV RUBY_DOWNLOAD_SHA256=f76d63efe9499dedd8526b74365c0c811af00dc9feb0bed7f5356488476e28f4
# Wed, 14 May 2025 23:03:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 14 May 2025 23:03:19 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 14 May 2025 23:03:19 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 14 May 2025 23:03:19 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 May 2025 23:03:19 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 14 May 2025 23:03:19 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:fa5acbf36757d3126014bc0e0a159fb5593a1d68ddba5992ef7ac9aa3e7db8dc`  
		Last Modified: Mon, 28 Apr 2025 21:10:59 GMT  
		Size: 48.8 MB (48775438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1d3e6811de68483322bf4607ec4cf0620d9d7f95dc19ce670b2ee81bd283341`  
		Last Modified: Tue, 29 Apr 2025 12:43:07 GMT  
		Size: 23.6 MB (23595734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b1d30b00e6e88ef455123e625951481f519a50849cb9e967c590e851c17b408`  
		Last Modified: Tue, 29 Apr 2025 21:16:09 GMT  
		Size: 63.3 MB (63308148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91d3c73f9a369d68121002b85e15bed118b5f9aea42d9fe654c6ac01aefd9236`  
		Last Modified: Wed, 30 Apr 2025 03:16:35 GMT  
		Size: 189.9 MB (189942024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:495aacae52b348c708667baeb4ee7b479493676c6a8de8c9def6f9ee00460b86`  
		Last Modified: Fri, 16 May 2025 00:18:24 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91d0b06233c94cd703f0c2ec9ec6deb80bc039a9dfe5a343322c97ee7887491d`  
		Last Modified: Fri, 16 May 2025 00:18:27 GMT  
		Size: 38.5 MB (38470193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f30ee4524489d6efac853ebdbd454a01da01e8bcce6c3693940bf60dc9bfed51`  
		Last Modified: Fri, 16 May 2025 00:18:24 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:latest` - unknown; unknown

```console
$ docker pull ruby@sha256:25fac1c3e5b487c29478630be19c10d498f08f32a055752b2bcc78e4e9a3a5c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.6 KB (22560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77f740ca09dc65fb7ec837ddbb5b9346e1aa35f18e0bfc6edc775c8370beaa31`

```dockerfile
```

-	Layers:
	-	`sha256:df921c9627370cbefc72a54b334a3672fcc5b8695a524cb22dda7574932171d3`  
		Last Modified: Fri, 16 May 2025 00:18:23 GMT  
		Size: 22.6 KB (22560 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:latest` - linux; ppc64le

```console
$ docker pull ruby@sha256:0550c7c0f8d791324ba4cc9a7b23efa2b9d9ce8198bf5af0ed0fe00945edf747
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **401.2 MB (401153703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:029a1bab6901cee922e48886d5b4e57d9d33358fd34c18bcc85328d618e2a44c`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1747699200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 May 2025 23:03:19 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 14 May 2025 23:03:19 GMT
ENV LANG=C.UTF-8
# Wed, 14 May 2025 23:03:19 GMT
ENV RUBY_VERSION=3.4.4
# Wed, 14 May 2025 23:03:19 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.4.tar.xz
# Wed, 14 May 2025 23:03:19 GMT
ENV RUBY_DOWNLOAD_SHA256=f76d63efe9499dedd8526b74365c0c811af00dc9feb0bed7f5356488476e28f4
# Wed, 14 May 2025 23:03:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 14 May 2025 23:03:19 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 14 May 2025 23:03:19 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 14 May 2025 23:03:19 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 May 2025 23:03:19 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 14 May 2025 23:03:19 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:996840ee350796081b3c80118ca1a58ce8212c6fdf88c454706a16457903a0c9`  
		Last Modified: Wed, 21 May 2025 22:27:49 GMT  
		Size: 52.3 MB (52331619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d82206e3ae1269ed70d5c84db92f6478d2de4719db96fab0f36254db269f0fa`  
		Last Modified: Thu, 22 May 2025 11:54:40 GMT  
		Size: 25.7 MB (25657297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c498d213a2aac9e38fe414de433d75bc8ba03faa40c2b4f0690897cf17174f58`  
		Last Modified: Thu, 22 May 2025 16:52:03 GMT  
		Size: 69.8 MB (69839678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd5288618fea79e9a348995382235e6bee52819db4047a345ffaeaddd2b82e06`  
		Last Modified: Thu, 22 May 2025 17:38:45 GMT  
		Size: 214.4 MB (214416172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd75905d9d9832f48b7420713bc2df330ddabf4c549cd9c41856b36289226e3f`  
		Last Modified: Fri, 23 May 2025 00:26:20 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:956d1a71054a1091820474497b8ce57cd61c707d1288ece9865575f6783d6e84`  
		Last Modified: Fri, 23 May 2025 00:30:18 GMT  
		Size: 38.9 MB (38908606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d787c1424bf90ebeb94df52a7ce6473bc96f15aea685c4744fdcdb71789e462`  
		Last Modified: Fri, 23 May 2025 00:30:17 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:latest` - unknown; unknown

```console
$ docker pull ruby@sha256:744ef2fbe288fbd0c2e757f1ae6904405e13c0d9736d2e8906dc807e6ff30eea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15685566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97b0a2b0ebaca9f3367a40524707068f7e6dd958cf028aa4288073fcfc8e66c9`

```dockerfile
```

-	Layers:
	-	`sha256:57da0915a5493ef15199d161f2de1c9e5038365beca6d6e86485b91fa2b2f280`  
		Last Modified: Fri, 23 May 2025 00:30:17 GMT  
		Size: 15.7 MB (15662825 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:315e7ab5c95edbb36450c2f1a3310108b16c597e22d881faffa50139cff34046`  
		Last Modified: Fri, 23 May 2025 00:30:17 GMT  
		Size: 22.7 KB (22741 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:latest` - linux; s390x

```console
$ docker pull ruby@sha256:183d9dcad8e0f1231b8fb41c13b3f2007df1f81921c34b7d580e38eadaed7e1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **356.2 MB (356157985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:915cc599b51cca3225de65bb03cb2df06c076ae98de30bf2f478c3ee98be0a3b`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1747699200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 May 2025 23:03:19 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 14 May 2025 23:03:19 GMT
ENV LANG=C.UTF-8
# Wed, 14 May 2025 23:03:19 GMT
ENV RUBY_VERSION=3.4.4
# Wed, 14 May 2025 23:03:19 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.4.tar.xz
# Wed, 14 May 2025 23:03:19 GMT
ENV RUBY_DOWNLOAD_SHA256=f76d63efe9499dedd8526b74365c0c811af00dc9feb0bed7f5356488476e28f4
# Wed, 14 May 2025 23:03:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 14 May 2025 23:03:19 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 14 May 2025 23:03:19 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 14 May 2025 23:03:19 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 May 2025 23:03:19 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 14 May 2025 23:03:19 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:47f9a2c2279c9df9e222a4c8af501e43b0b5e2552eda9597a97162080b8f106b`  
		Last Modified: Wed, 21 May 2025 22:28:14 GMT  
		Size: 47.1 MB (47143842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c86a43d043466908a6aee9cc569c707c9cb9b87fe3e55b5a27e7fe7f7f27d73c`  
		Last Modified: Thu, 22 May 2025 01:01:58 GMT  
		Size: 24.0 MB (24014856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85bf0b00f04b5784c02aa34bd5edd104e26e960d8480606e6f206c6a22330235`  
		Last Modified: Thu, 22 May 2025 04:37:16 GMT  
		Size: 63.5 MB (63498527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3151505c70d8a7022bb518bbfce9c7488d1dd6ab624e1d96b883eb0654da7562`  
		Last Modified: Thu, 22 May 2025 06:39:53 GMT  
		Size: 183.4 MB (183405201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e81476f32350c38e35cde33eb4b9a75848a0d70dcf6525abafce9a43b85b011`  
		Last Modified: Thu, 22 May 2025 11:55:35 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c12eb9f9bf70a3542f1e32ac81209c6f5f621f60a9febd2ce3724cc1829e35e`  
		Last Modified: Thu, 22 May 2025 11:58:39 GMT  
		Size: 38.1 MB (38095227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd164bf0c9a01626332ccdae4cafe5bf0c48f8a9885f1409648aeaff79bbdd8a`  
		Last Modified: Thu, 22 May 2025 11:58:38 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:latest` - unknown; unknown

```console
$ docker pull ruby@sha256:433af410a0bd5a50713c553cd0de0b7daf67a594895d2f328b2ce001e5fb0e5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15519457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d9f6be9496b532e382e17a9ecfb272e32354a76706013dcf5d4e58714733aea`

```dockerfile
```

-	Layers:
	-	`sha256:bc132d6f27cfae444ce9278454cf9e8063fbdd4056e7f46de5dbc53fee529ba2`  
		Last Modified: Thu, 22 May 2025 11:58:38 GMT  
		Size: 15.5 MB (15496788 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae743dba0288129d6c919bc748b9f5e4762fb073848ec3e23e324da9c343f8b3`  
		Last Modified: Thu, 22 May 2025 11:58:38 GMT  
		Size: 22.7 KB (22669 bytes)  
		MIME: application/vnd.in-toto+json
