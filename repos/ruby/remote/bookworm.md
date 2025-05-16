## `ruby:bookworm`

```console
$ docker pull ruby@sha256:370e6be29a1cecbf44993087d2750e7d9e1570fde5b97c74325063b1750d11d0
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
$ docker pull ruby@sha256:f007088d172a6c95144deec01519b2fdc03d47575cdabda3bc8b0ca682898ed0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.7 MB (389725985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de3d2d45c9d6be69a188cd1c3ad0b54976df6783f41c522ea8b8c9ca544aeb0e`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
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
	-	`sha256:cf05a52c02353f0b2b6f9be0549ac916c3fb1dc8d4bacd405eac7f28562ec9f2`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 48.5 MB (48491199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63964a8518f54dc31f8df89d7f06714c7a793aa1aa08a64ae3d7f4f4f30b4ac8`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 24.0 MB (24011181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca513cad200b13ead2c745498459eed58a6db3480e3ba6117f854da097262526`  
		Last Modified: Thu, 08 May 2025 17:04:41 GMT  
		Size: 64.4 MB (64394427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c187b51b626e1d60ab369727b81f440adea9d45e97a45e137fc318be0bb7f09f`  
		Last Modified: Thu, 08 May 2025 17:05:14 GMT  
		Size: 211.4 MB (211356050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e17ee552dfe9952ea3186c5bd26dbcb8ced249aa240de1fd3a425077fc945de`  
		Last Modified: Fri, 16 May 2025 13:05:13 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc1db167008462e1797c94f01115bf9ad73cae3ee3048ad6d485d4b7f6962d6a`  
		Last Modified: Fri, 16 May 2025 13:05:16 GMT  
		Size: 41.5 MB (41472795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:148ac9b7d94b1dddacde975f0ab3a9fe096a399d42d28709a8982c37451bca22`  
		Last Modified: Fri, 16 May 2025 13:05:06 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:6366888617b90d65bf1265a9197d9904f4909907ade7174276320e164231d4e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15710203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6d96fb29222488fc852dde733e3c17578192b5ef5c186bf6e80ab45ccf73a34`

```dockerfile
```

-	Layers:
	-	`sha256:dcf58cf13274b7c87ed86ff4dee9600ba770826aa190c09defde1360b704173a`  
		Last Modified: Fri, 16 May 2025 15:03:58 GMT  
		Size: 15.7 MB (15687534 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:297111f8c5cc180ca80f3d1ae3d8bfaafa5a11f4d914f5d1bbb911a571d19d4f`  
		Last Modified: Fri, 16 May 2025 15:03:57 GMT  
		Size: 22.7 KB (22669 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:bookworm` - linux; arm variant v5

```console
$ docker pull ruby@sha256:4c82fc4e04b94e3c895ed5edb0bea00b11be41318ed5a8edafcbc66310817e63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.6 MB (352615957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b780e5238bc98e0eddd5c03b86af7158dc0279b9e0165de656f5f465c7fe7cb`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1745798400'
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
	-	`sha256:41b62f0ff831a6d9573670f580122f67e27137902fa02ca0a3faf11fda42603f`  
		Last Modified: Thu, 08 May 2025 17:16:08 GMT  
		Size: 46.0 MB (46026796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:933aa71bcd4cf4d4ade7e455a6a748ec9d00e74ad6f8b2dfd8f9c9b70593ba3a`  
		Last Modified: Thu, 08 May 2025 17:15:59 GMT  
		Size: 22.7 MB (22689607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:461cae6835e6d9e4c238b202d114b5fb2f2b659479fcad91acee966b7bf3bcc9`  
		Last Modified: Thu, 08 May 2025 17:16:02 GMT  
		Size: 62.0 MB (62005790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dfb6286f141608ba5fe6c6ba2dc6eccf0574268a7436cd81d4de08cd3894433`  
		Last Modified: Thu, 08 May 2025 17:16:17 GMT  
		Size: 184.7 MB (184655994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6fb29ff64b5521e879229e1017c87b1af21c59fdefb847fc4d248137891c79d`  
		Last Modified: Fri, 09 May 2025 06:45:51 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de0668ac0c860a1e43f8812f61fcb481a9e5ecf85950e4e78b3340a08bcf0d25`  
		Last Modified: Fri, 16 May 2025 15:04:00 GMT  
		Size: 37.2 MB (37237436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2a69b14a2d505bdda0e88efe35e23f22c0e3bfecd7784f1a277e9f81922200f`  
		Last Modified: Fri, 16 May 2025 15:03:59 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:4a41c9888f2b0146fb44ad4ab1c1df06a48191ae44e5762bc87dbe02d3e40f79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15507440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20cad1fc499d88f0a20ceaa7d3ebea6cf305929ff9b0aa256becbe8a0dee8583`

```dockerfile
```

-	Layers:
	-	`sha256:6000b0e63d80087f2d5360474c9876699920f6725a2e0ef65cd770ff8a1c3fc7`  
		Last Modified: Fri, 16 May 2025 15:04:00 GMT  
		Size: 15.5 MB (15484637 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5d5fabdd242f1ad4f69e76a68d3e9c3349590c96ced3f791dd007951e10b2e0`  
		Last Modified: Fri, 16 May 2025 15:03:59 GMT  
		Size: 22.8 KB (22803 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:bookworm` - linux; arm variant v7

```console
$ docker pull ruby@sha256:085dec887656724fda6eae20e40aa311bb3961be2b5ef9758392724663ca1b1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.1 MB (338143027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:628bb02720f5972e30e57d5fa09c242d58fc8a82c5898aa2eff94040f38a43e0`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1745798400'
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
	-	`sha256:a735d4b4a53e8e11448d15bc50ce4670d54dff52e426cf0510c9b713d3a7ad09`  
		Last Modified: Thu, 08 May 2025 17:04:48 GMT  
		Size: 44.2 MB (44197079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b01e6436acd06b177253a4ba25e5179715088c2f493e89c91bbf6fdc41a2034`  
		Last Modified: Thu, 08 May 2025 17:05:35 GMT  
		Size: 21.9 MB (21918380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3553b1499305feec4f182c1e2562e06daaecb3dc337d83b89b8c909f46c0a1`  
		Last Modified: Thu, 08 May 2025 17:05:43 GMT  
		Size: 59.6 MB (59640211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5d55cc6c59023a65c15579520e32553ab9f1e2d6377e8e4dd69393e113713d3`  
		Last Modified: Thu, 08 May 2025 17:14:19 GMT  
		Size: 175.3 MB (175316182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cba866b093607826f7bc899bd0151259947595263da799f490ccff32b94eadcf`  
		Last Modified: Fri, 09 May 2025 01:12:41 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:577f6158ace36c8ef212bc3cf5dd404d757766441436baffda0a7d319623500a`  
		Last Modified: Fri, 16 May 2025 15:04:04 GMT  
		Size: 37.1 MB (37070845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c47563f429d928c837fa97bd83e836b5e6c08c18915190f7520f17bca080362`  
		Last Modified: Fri, 16 May 2025 15:04:02 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:f63e6054bdf5133b46c5073d7cc9d65380b6adb33e0d7c2a8442876baccb7bc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15512914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc86a7be251fa18df4a407755ed52a21edfcc5a7f9499745bb4c1bccd227a672`

```dockerfile
```

-	Layers:
	-	`sha256:7bfd206e5f8e8fc269a03e7143385552e010dc5cd6a8d9918405d5498dec6520`  
		Last Modified: Fri, 16 May 2025 15:04:02 GMT  
		Size: 15.5 MB (15490111 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e44adc27ed137ceed81fd183a56f202a01faa3fb0e0705bc9f53f158ab70ea97`  
		Last Modified: Fri, 16 May 2025 15:04:01 GMT  
		Size: 22.8 KB (22803 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:bookworm` - linux; arm64 variant v8

```console
$ docker pull ruby@sha256:b700f422dbb9c6bd8cc59c5b0be12692d125fb36db73712b499c7c0c9bf29058
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **380.3 MB (380338589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:138dd1428e555959dedb41c9efca7faea6fba8ad7bacda82a31ad0f1afa692e0`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
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
	-	`sha256:de07ba6f486e0ce29760ab32d4381edabbc660a04c493e95eb9a8056925d8955`  
		Last Modified: Thu, 08 May 2025 17:04:44 GMT  
		Size: 48.3 MB (48327644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84649bff67ea459549b6f371f7045d9968d6ebf370b815c922a625f3ab065724`  
		Last Modified: Thu, 08 May 2025 17:04:42 GMT  
		Size: 23.5 MB (23544262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48a2a14f59a002f5ef50911a0687d30beadf65bbe35bde8bd3823c3496cbd465`  
		Last Modified: Thu, 08 May 2025 17:04:49 GMT  
		Size: 64.4 MB (64355683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d41c7623f41e51939686bf861fe89538ae4dc84481ff4136b55524e770d2603`  
		Last Modified: Thu, 08 May 2025 17:04:51 GMT  
		Size: 202.7 MB (202748227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdad7cb423a11d6a003686256726fc9c450cfc3e320fef8e2066545e9814184a`  
		Last Modified: Thu, 08 May 2025 17:06:17 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b05e8cfff30a9c9ad8549c67d85247713c0a0a5f2446b22e596e9fcad245bf38`  
		Last Modified: Fri, 16 May 2025 13:11:49 GMT  
		Size: 41.4 MB (41362440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:512d184fbe5c01d816ef79b17490ac84e9873d42d04f64959df8c03f2542c1a9`  
		Last Modified: Fri, 16 May 2025 13:11:45 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:4435469476c8c90577717b273bff4a7eb2c99ca901dc0739efef6748a3355f0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15738957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6b0db19679bccbd901d51b389e7ec7a505ced157e5113f39fce1b76403d78e9`

```dockerfile
```

-	Layers:
	-	`sha256:9c401088950ff30bc412c6200818876afaca175a155629aa13e6cf6ddf3585c9`  
		Last Modified: Fri, 16 May 2025 15:03:43 GMT  
		Size: 15.7 MB (15716107 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d15cf6c98e7d88ec1668246a3a90215c958188b1b9f5aa155cf0a33690a4d47e`  
		Last Modified: Fri, 16 May 2025 15:03:42 GMT  
		Size: 22.9 KB (22850 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:bookworm` - linux; 386

```console
$ docker pull ruby@sha256:8099ce27415a894e79beec7ba4f96c20c8a5e100ee8cc9bc9ee83ef224528e34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **387.9 MB (387909400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a17ffc80ec56cc42d7c6f6d2adea55cbafcfbce274622528fd7ff26e3d2265a1`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1745798400'
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
	-	`sha256:d6426ff7fee55f1c5da8050672c1463528bb15df73bf93e3ac0a5200042f6c3f`  
		Last Modified: Thu, 08 May 2025 17:05:10 GMT  
		Size: 49.5 MB (49478572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8121c387e441201e2e932ee9747762becb1f76490293a373bd9505310d1fe4e`  
		Last Modified: Thu, 08 May 2025 17:05:06 GMT  
		Size: 24.8 MB (24847147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ce8929d56fab56325a8eea211cb4cd1021bc6ffc1e7a794d505ddbe638b23cd`  
		Last Modified: Thu, 08 May 2025 17:05:07 GMT  
		Size: 66.2 MB (66228922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1528cc13747bb103866d00332de43f9304156fef5a2f396b15d9e173b1365f5`  
		Last Modified: Thu, 08 May 2025 17:39:23 GMT  
		Size: 210.3 MB (210293092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:762d9b01cc31993895da79a13386d9611d80442d5ec50f7bfae00bb16cef5475`  
		Last Modified: Fri, 16 May 2025 15:03:43 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70056c51f37bf489a799ec5f4ceb7b9faa746922642b6963d0b640e92ab85c03`  
		Last Modified: Fri, 16 May 2025 15:03:46 GMT  
		Size: 37.1 MB (37061336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38950bbe5088523eddf5571f3063c177f204b3ffe11b7c64684037629e5520ea`  
		Last Modified: Fri, 16 May 2025 15:03:44 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:aecd9e241b8200781fd76518f5ed95eb980af040abf548e742d45c20b10a5301
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15688384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7e79392562fe01b1654c8aabeee6b79d65d27b01fac2b9f39e0936bc2f9c9e5`

```dockerfile
```

-	Layers:
	-	`sha256:3534ecf1875ff0a003343d36f8ef6abb4e805b6836bcaaf85f4f6898cc4c85d5`  
		Last Modified: Fri, 16 May 2025 15:03:47 GMT  
		Size: 15.7 MB (15665771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5596e4e15aa34d9c0010689794389b04b73a4d2ad51c3c82d927265a3d5557e6`  
		Last Modified: Fri, 16 May 2025 15:03:47 GMT  
		Size: 22.6 KB (22613 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:bookworm` - linux; mips64le

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
		Last Modified: Thu, 08 May 2025 19:59:58 GMT  
		Size: 48.8 MB (48775438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1d3e6811de68483322bf4607ec4cf0620d9d7f95dc19ce670b2ee81bd283341`  
		Last Modified: Thu, 08 May 2025 19:59:57 GMT  
		Size: 23.6 MB (23595734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b1d30b00e6e88ef455123e625951481f519a50849cb9e967c590e851c17b408`  
		Last Modified: Thu, 08 May 2025 19:59:58 GMT  
		Size: 63.3 MB (63308148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91d3c73f9a369d68121002b85e15bed118b5f9aea42d9fe654c6ac01aefd9236`  
		Last Modified: Thu, 08 May 2025 20:00:03 GMT  
		Size: 189.9 MB (189942024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:495aacae52b348c708667baeb4ee7b479493676c6a8de8c9def6f9ee00460b86`  
		Last Modified: Fri, 16 May 2025 15:03:47 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91d0b06233c94cd703f0c2ec9ec6deb80bc039a9dfe5a343322c97ee7887491d`  
		Last Modified: Fri, 16 May 2025 15:03:50 GMT  
		Size: 38.5 MB (38470193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f30ee4524489d6efac853ebdbd454a01da01e8bcce6c3693940bf60dc9bfed51`  
		Last Modified: Fri, 16 May 2025 15:03:48 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:bookworm` - unknown; unknown

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
		Last Modified: Fri, 16 May 2025 15:03:48 GMT  
		Size: 22.6 KB (22560 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:bookworm` - linux; ppc64le

```console
$ docker pull ruby@sha256:b34f7ca05421c4d9d92377542838856df1b7f0f095166cd8c266519d1d2d9831
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **401.1 MB (401141250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39600dbb37b97cf9493419b16de87f5fa8f9d1314e8c0d3dafd97b473107c2f8`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1745798400'
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
	-	`sha256:33862e890d6c23fba01df0303b503e727dad5c72574fdf8af76d76dc3140d561`  
		Last Modified: Thu, 08 May 2025 17:13:17 GMT  
		Size: 52.3 MB (52332129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4617415431bf61f96c81d815cfb6cf010eef7bd0d8a8de24b02c1a7fe8407026`  
		Last Modified: Thu, 08 May 2025 17:13:13 GMT  
		Size: 25.7 MB (25650113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cae70f40efc6df1466aa415707fbf58268a1633e6ab2dde78f23ec024d7c1e42`  
		Last Modified: Thu, 08 May 2025 17:13:18 GMT  
		Size: 69.8 MB (69840424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3f7f895e65e8530bee082db2e14aefaa34547b4753e60990faca2b691714e63`  
		Last Modified: Thu, 08 May 2025 17:24:00 GMT  
		Size: 214.4 MB (214409240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17f60a16ffd60fb88310306453b49210f356b44460691b4fd8408088a2f15c90`  
		Last Modified: Fri, 09 May 2025 06:45:50 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcf2dfc73b1368b685afab688035d20a5bfcb33a860d432b0a8a1bd07da5ccf3`  
		Last Modified: Fri, 16 May 2025 15:03:52 GMT  
		Size: 38.9 MB (38909012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7be34b6ff7732c5c86d721d7e7224edf2293c7718c2348e5d98fe9300d4d9bd2`  
		Last Modified: Fri, 16 May 2025 15:03:49 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:385052c3d4eec36a86e478335bd80d3a0a641eaf0a4adb572ba21ac2e247b656
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15686807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3040909e637a600f734a65b06664c745efaeb991553613a077c86fa66b557676`

```dockerfile
```

-	Layers:
	-	`sha256:b5f8ccdb5fa08d7a121a887c12a277a3084a60c872e1acddbce5e28761f4a731`  
		Last Modified: Fri, 16 May 2025 15:03:51 GMT  
		Size: 15.7 MB (15664066 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d148b3b56942370e67820f9533c1a20e66d8903a11f67e968c935cc3e2db4f6c`  
		Last Modified: Fri, 16 May 2025 15:03:51 GMT  
		Size: 22.7 KB (22741 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:bookworm` - linux; s390x

```console
$ docker pull ruby@sha256:9040a7491106e20003acec62d586aa5e2960e69614955ebeb0e8ec1c247f61a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **356.2 MB (356160215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42fbdfa85326bb09388a3824b261ac9ea9d449d8b0003f6094c8989fb6a13a70`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1745798400'
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
	-	`sha256:a5e7ec27bb28a531688c62bada8c4b448d8e280327ecabb8be798bc43be30c38`  
		Last Modified: Thu, 08 May 2025 17:04:50 GMT  
		Size: 47.2 MB (47151332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c05c607354a47eba0ce7493f4dc26e0f40aaeea360944111a83eeeeb61083045`  
		Last Modified: Thu, 08 May 2025 17:16:24 GMT  
		Size: 24.0 MB (24008311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15250b46b7f7ffe8ad5ce0f3a2d64d0437e4fdf3d36b87579551846c0b2dd2bc`  
		Last Modified: Thu, 08 May 2025 19:32:33 GMT  
		Size: 63.5 MB (63496877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbfe8bd3e826ba76e4ad73b0a5ce638276af95b860bec9b25c2754c5600c5a61`  
		Last Modified: Thu, 08 May 2025 19:32:39 GMT  
		Size: 183.4 MB (183405963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33d66d93e6fe5ebbb7f57773385bf8dea2a317b37cd7c3f04b113245bd38414a`  
		Last Modified: Fri, 16 May 2025 15:03:52 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f021e24a7f10b7577c18b80bff9ec9a20e91986585ba996fcf16eb4e7049ae00`  
		Last Modified: Fri, 16 May 2025 15:03:55 GMT  
		Size: 38.1 MB (38097400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c543f92d96fcc46ea19ceb8ebde3559c32ac9f9bda30cab3ce7cc96a7e29b836`  
		Last Modified: Fri, 16 May 2025 15:03:53 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:b3530b0d438af5632b0f9ec790cdcbac6bbd4081b9c3e2a4ed7581f3afe78e83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15520748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70ba5894eb288da4de1af404b07544ea687eeec0484ef53a5859f6740062160a`

```dockerfile
```

-	Layers:
	-	`sha256:4d2b851c6dc43bd68b89f03bdb429a72f924b20e01a8671e91c9252e6301e07a`  
		Last Modified: Fri, 16 May 2025 15:03:55 GMT  
		Size: 15.5 MB (15498079 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e28afe0f17f2ba169e3703e8e49969dc7d3161122f1f3178eaba4da9ce1f9386`  
		Last Modified: Fri, 16 May 2025 15:03:54 GMT  
		Size: 22.7 KB (22669 bytes)  
		MIME: application/vnd.in-toto+json
