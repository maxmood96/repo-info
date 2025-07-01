## `ruby:3-slim-bullseye`

```console
$ docker pull ruby@sha256:1f1f07e4cdce1de1f1b4b560e27e2ccc6103b0d497c200d057dc48cc9507ec06
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

### `ruby:3-slim-bullseye` - linux; amd64

```console
$ docker pull ruby@sha256:9c9721f2a002cdb67549626b7187ffb99d3cebf80fd2494cb841e54922956681
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.7 MB (72667941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:508902131d8a7094fb915dbffeb90f58f606b5bf4ca7511cc519234f7dd6e51d`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 14 May 2025 23:03:19 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1751241600'
# Wed, 14 May 2025 23:03:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
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
	-	`sha256:cc41ef31545f10925901837c6dea7e184299788097caaa3fabb57ed109c52a98`  
		Last Modified: Tue, 01 Jul 2025 01:14:42 GMT  
		Size: 30.3 MB (30256047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea482f76027ad7c653227e2c38391b4700d4cc9daee9ff4b1d5866c947cf70af`  
		Last Modified: Tue, 01 Jul 2025 02:38:58 GMT  
		Size: 1.1 MB (1068027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ba012625bcca3afcc24c5ca6f8dfc08557e99220a28a2fbfe989e7da9d00b90`  
		Last Modified: Tue, 01 Jul 2025 02:38:53 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a56d0443419a83bb4a2dac0daae85c0d789dc9f885ebf5a365622d615079819`  
		Last Modified: Tue, 01 Jul 2025 02:39:20 GMT  
		Size: 41.3 MB (41343536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bad6a6613a68e959bdcf459e879d31e7f8ffbf9c349e7f22e7fa011722b53f69`  
		Last Modified: Tue, 01 Jul 2025 02:38:54 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-slim-bullseye` - unknown; unknown

```console
$ docker pull ruby@sha256:675ad666b324747bd1cfd8927853f5c14b212ef81f0382c6c9bc00dbb833215f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2913550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86ff218ab80f75aebdd773a1c6cf638b7aa470bc245dd8769f71354d879bdbc3`

```dockerfile
```

-	Layers:
	-	`sha256:8539940d496cf8a2f2a0d618e6703134d1941b42e8e9a24b62d301ee6d575ea1`  
		Last Modified: Tue, 01 Jul 2025 05:57:43 GMT  
		Size: 2.9 MB (2890755 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:356810957309bbce8268f02e1c4477e6a0a1c42cfeda6ab734c93302520b3ad3`  
		Last Modified: Tue, 01 Jul 2025 05:57:44 GMT  
		Size: 22.8 KB (22795 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-slim-bullseye` - linux; arm variant v7

```console
$ docker pull ruby@sha256:5ae716a611f1c777d95620627a081b4e5b4cdaa761a19e81385efbe7a224f490
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.2 MB (63191440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9649267bccf28192314a3bf8a3cf38547613b95b49302019717e2e4c3bec4770`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 14 May 2025 23:03:19 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1751241600'
# Wed, 14 May 2025 23:03:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
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
	-	`sha256:96b51e81cdb8508366118f41a9ec499f52f0d0211b084d5d516e1be131b35266`  
		Last Modified: Tue, 01 Jul 2025 01:15:21 GMT  
		Size: 25.5 MB (25544163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec148d7b8a0724d10a0851d5c62efcd4f185072b18802bcd3523f06b7288a20d`  
		Last Modified: Tue, 01 Jul 2025 17:34:56 GMT  
		Size: 1.0 MB (1033014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69626d7f8958685e25dde73f19bd030c03780b419fe6db9ae7233a814266a9ee`  
		Last Modified: Tue, 01 Jul 2025 17:34:55 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec57add4ba151cc3ee43613760fca85eae8f368abda502dd9553b62642e85a2e`  
		Last Modified: Tue, 01 Jul 2025 17:42:06 GMT  
		Size: 36.6 MB (36613930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42321cd57a9ad904b9427e8f7d3c35c0b9af36dcfd3db77f154e27c423827d5c`  
		Last Modified: Tue, 01 Jul 2025 17:42:00 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-slim-bullseye` - unknown; unknown

```console
$ docker pull ruby@sha256:d5fe00f202e507082c6698ce4ffb4f229cb8ff18995f1fe9b9aad0a0fa8d0094
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2915889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cb03d1127c84518fca87d0701607acdcf51100018ca139ff34d066bd1dc8509`

```dockerfile
```

-	Layers:
	-	`sha256:c811a47be923ff509bf52029d243416364742c3b4250dda6b1e4217c21b273a8`  
		Last Modified: Tue, 01 Jul 2025 20:57:48 GMT  
		Size: 2.9 MB (2892979 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08a696d61c7dab5e7a3a250dbfbf106dccfe26109fb7ee73ad64693ee99b6398`  
		Last Modified: Tue, 01 Jul 2025 20:57:49 GMT  
		Size: 22.9 KB (22910 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull ruby@sha256:c401bcc3fa3c8e619dba928945c137ffebbef82dc3544c071af65e57217a4f6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (70999360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7124602ebc38eb9f75ae3f61e5d8d4695d16d799a88abe1170c92b381c816bd8`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 14 May 2025 23:03:19 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1751241600'
# Wed, 14 May 2025 23:03:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
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
	-	`sha256:00ce3d02ade4a2c8e5e37b1a218bb5c24c995bd8757095b89316c42854286fe8`  
		Last Modified: Tue, 01 Jul 2025 01:15:35 GMT  
		Size: 28.7 MB (28744140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4bb58bcf51737a3f273a2de946db941abe3644c0d4e35c2f71ed7c6b121e873`  
		Last Modified: Tue, 01 Jul 2025 11:22:03 GMT  
		Size: 1.1 MB (1055222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd1d6229983cb5e87f4a66dbc1c070a056f4b0618619662c395ef17653725ff8`  
		Last Modified: Tue, 01 Jul 2025 11:22:03 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19fb1581e649ead40d3a27c410b5aa09fe1b34b2ee09b2cd84caf29c9184995f`  
		Last Modified: Tue, 01 Jul 2025 11:28:06 GMT  
		Size: 41.2 MB (41199669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00b9df64154eb3e4329694620c4c9c3a0ded6828efcae326920554b17f62b3c4`  
		Last Modified: Tue, 01 Jul 2025 11:28:02 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-slim-bullseye` - unknown; unknown

```console
$ docker pull ruby@sha256:00e93262e573f4c9e71c4e14eb1f31d842517bdc9fa61c016c49665af1cf2888
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2913948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b59221e59028c1f418cbeea2d79e072328f52b145a2bf60506efb3fdba3a875`

```dockerfile
```

-	Layers:
	-	`sha256:3f5976f93da7fa0e115758d4f36ae32d8be43bd988cd90ec17c93639f7570412`  
		Last Modified: Tue, 01 Jul 2025 14:57:45 GMT  
		Size: 2.9 MB (2891007 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65dba7c1cf858a5d1cf7d8ea01c7e85b502f130396142dbeede5baa4d3fa3164`  
		Last Modified: Tue, 01 Jul 2025 14:57:45 GMT  
		Size: 22.9 KB (22941 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-slim-bullseye` - linux; 386

```console
$ docker pull ruby@sha256:6cafb6c2a974f4d9504efe43d01f07c36adb569c521b9a69a4b8c8df2a2910f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.0 MB (68983469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec101fb35a9d1da976afa3815c28e09e6eb17f7ea094ee33f250a637c2a5ab00`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 14 May 2025 23:03:19 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1751241600'
# Wed, 14 May 2025 23:03:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
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
	-	`sha256:40be1da6146972d9df50a98eef7b5c0f729cd95a3a38782418f354f3b9355a9a`  
		Last Modified: Tue, 01 Jul 2025 01:14:57 GMT  
		Size: 31.2 MB (31189680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac02e81411a12491cd8e420a77c08a1d65afac70c89d8fb249e64f65ec2b63bc`  
		Last Modified: Tue, 01 Jul 2025 02:33:24 GMT  
		Size: 1.1 MB (1080107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7470f313112f858e6ed757f0717290d68b51e165d84c5d77418db40f7e75b935`  
		Last Modified: Tue, 01 Jul 2025 02:33:24 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:544a3f9d083c79020d6218fe416467598088614e7405070ce45c582431ae36e9`  
		Last Modified: Tue, 01 Jul 2025 02:33:26 GMT  
		Size: 36.7 MB (36713351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcbb0e57a5977d81680887b3b231c8a534f245f9b5ef88a247dddd2d6a033dd0`  
		Last Modified: Tue, 01 Jul 2025 02:33:23 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-slim-bullseye` - unknown; unknown

```console
$ docker pull ruby@sha256:5cfde0046bb08264c4741bc7c9959700876fb5a17323ce337af9eabad0ee0e0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2910689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5df35f85e8b0d0ac59f2f36c03ad0002cb3efdf26aa67c284cda4921a919de48`

```dockerfile
```

-	Layers:
	-	`sha256:c5a2a4ac0cbdc7a6f8dd3c3c28b4cb89a80880871fff80c58cd8e022cd26d30e`  
		Last Modified: Tue, 01 Jul 2025 05:57:59 GMT  
		Size: 2.9 MB (2887932 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12a1aa07f9210d21118ad43bf2959cd7dcda99b6de5a69b2b1f2daa79f7e5bfa`  
		Last Modified: Tue, 01 Jul 2025 05:58:00 GMT  
		Size: 22.8 KB (22757 bytes)  
		MIME: application/vnd.in-toto+json
