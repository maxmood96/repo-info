## `ruby:3-alpine`

```console
$ docker pull ruby@sha256:45bdd95e337296472eafa907dc53cfbcf1e3878a11795062f47392d4c251add9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
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

### `ruby:3-alpine` - linux; amd64

```console
$ docker pull ruby@sha256:cda25e169e9bf68141ea34d3bc19f2a9ad6c809a093f13054e6ba59c96f21f62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.1 MB (43120357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f83744592a9399261980950d140768ce3b4974863b3c8b68aedec639685bba6b`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 11 Mar 2026 18:37:55 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 11 Mar 2026 18:40:11 GMT
ENV LANG=C.UTF-8
# Wed, 11 Mar 2026 18:40:11 GMT
ENV RUBY_VERSION=3.4.9
# Wed, 11 Mar 2026 18:40:11 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Wed, 11 Mar 2026 18:40:11 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Wed, 11 Mar 2026 18:40:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 11 Mar 2026 18:40:11 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 11 Mar 2026 18:40:11 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 11 Mar 2026 18:40:11 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Mar 2026 18:40:11 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 11 Mar 2026 18:40:11 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7880da1bfd5b14154cb45089d913e2481434be383f65400a04e13a2a36d60a90`  
		Last Modified: Wed, 11 Mar 2026 18:40:18 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d27f06a84614baf14305fe010590c159dca2e4914f8b21500a61f082e2b60801`  
		Last Modified: Wed, 11 Mar 2026 18:40:19 GMT  
		Size: 39.3 MB (39258205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3bfd5d71c93a02421ba583dfd370e0ec47ac2c335e761091c7bda4fe0578c85`  
		Last Modified: Wed, 11 Mar 2026 18:40:18 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-alpine` - unknown; unknown

```console
$ docker pull ruby@sha256:0b38bb674791cd8c8413f2c6b4b3f7936e99d7705af99e10ae15810e9f0f1627
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.2 KB (229187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0edf8a3c8a6a08ee5b7254a11cd47a831dac92b68a4b29ec61aa55c552a9e98`

```dockerfile
```

-	Layers:
	-	`sha256:44e98f17e199b5b476194431c0f0fecdeed0ea5fcbee1069b676510922809804`  
		Last Modified: Wed, 11 Mar 2026 18:40:17 GMT  
		Size: 206.1 KB (206132 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8f3c446b615437f29c63883dca5917c5553f943f6e30e5b2043f3dca5a88b56`  
		Last Modified: Wed, 11 Mar 2026 18:40:18 GMT  
		Size: 23.1 KB (23055 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-alpine` - linux; arm variant v6

```console
$ docker pull ruby@sha256:093376616fab8dcfcb302a66a7e5f3a85e05417e4daf606068ba9e977b4624d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.5 MB (38474026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acd257519f8e8122df68fab60f5096f51093f6fdea24e8d10a11bca565712190`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Wed, 11 Mar 2026 18:34:19 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 11 Mar 2026 18:36:51 GMT
ENV LANG=C.UTF-8
# Wed, 11 Mar 2026 18:36:51 GMT
ENV RUBY_VERSION=3.4.9
# Wed, 11 Mar 2026 18:36:51 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Wed, 11 Mar 2026 18:36:51 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Wed, 11 Mar 2026 18:36:51 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 11 Mar 2026 18:36:51 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 11 Mar 2026 18:36:51 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 11 Mar 2026 18:36:51 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Mar 2026 18:36:51 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 11 Mar 2026 18:36:51 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fde66386be7bfeb6e24848587efbcbf54b931f0be2ace9852d8541398379cb2`  
		Last Modified: Wed, 11 Mar 2026 18:36:56 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:633d28dd5c4d53c7e28dbed3cd43005bcc9553c3ecc0f4d36a22937dc88c6188`  
		Last Modified: Wed, 11 Mar 2026 18:36:57 GMT  
		Size: 34.9 MB (34903876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dd2426d524ab338bff3bad372d26933a9c7d3fa79207d61c798a657faac939e`  
		Last Modified: Wed, 11 Mar 2026 18:36:56 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-alpine` - unknown; unknown

```console
$ docker pull ruby@sha256:c91c848e6cde76fd6f14983383d21d232edf447d93675a033498e0af8dd9165a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.0 KB (22962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bb1b316fae2242273b07076810d462f112750f98c57387cb1e892cbd4b217d5`

```dockerfile
```

-	Layers:
	-	`sha256:c2821e9689ef45131461ef29711a9e2436eccefe5cb950fb91023c8e0c1ef0c6`  
		Last Modified: Wed, 11 Mar 2026 18:36:56 GMT  
		Size: 23.0 KB (22962 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-alpine` - linux; arm variant v7

```console
$ docker pull ruby@sha256:7c3c87419b3eb5a2d7786f051b223422612eaf653eb3fc57eb2c891c060d362b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.0 MB (38030671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14e0994c1f46af4dec9a4bdee7f69dab781b5dd2ab2a602f0d87c36ed59e55ae`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Wed, 11 Mar 2026 18:37:46 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 11 Mar 2026 18:40:19 GMT
ENV LANG=C.UTF-8
# Wed, 11 Mar 2026 18:40:19 GMT
ENV RUBY_VERSION=3.4.9
# Wed, 11 Mar 2026 18:40:19 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Wed, 11 Mar 2026 18:40:19 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Wed, 11 Mar 2026 18:40:19 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 11 Mar 2026 18:40:19 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 11 Mar 2026 18:40:19 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 11 Mar 2026 18:40:19 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Mar 2026 18:40:19 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 11 Mar 2026 18:40:19 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37fc4c2c10b0b0c9fbf81626aba073cb164564013b4d05b3e8f5abe152113879`  
		Last Modified: Wed, 11 Mar 2026 18:40:27 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68dcc4ee0547bc70a967b35d76c51151695bcb6b504633f6e0067de9ee949e9a`  
		Last Modified: Wed, 11 Mar 2026 18:40:28 GMT  
		Size: 34.7 MB (34748617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a234ca150649ad91ff9ff37762d933e0f4707fcb43b032243452b86e7b80cc7`  
		Last Modified: Wed, 11 Mar 2026 18:40:27 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-alpine` - unknown; unknown

```console
$ docker pull ruby@sha256:10c73bd35a8a2c9598fe831000535d1fa64a319b29ee6543c0899f276877495f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 KB (228711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52704afead06694675c950f18a4d05577ac0bd1e500ea732449694a506a25871`

```dockerfile
```

-	Layers:
	-	`sha256:3c108818b24392573344ca222a5d99b1e1d49b0d3b1984ec4d082338acd94133`  
		Last Modified: Wed, 11 Mar 2026 18:40:27 GMT  
		Size: 205.5 KB (205534 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91a9bd51c9e1ffd4ad4469ee397b537be8a845c407f8e231aff555e49ca780ce`  
		Last Modified: Wed, 11 Mar 2026 18:40:26 GMT  
		Size: 23.2 KB (23177 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-alpine` - linux; arm64 variant v8

```console
$ docker pull ruby@sha256:061641e0f18be97a9b9e5ae02f3c41381362fe736fb1f710c84e837397ec56fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.5 MB (43515265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e554400391378310f1768aaeb703a97dee092b34ca7ab65a448e50310b90e40`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 11 Mar 2026 18:37:26 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 11 Mar 2026 18:40:07 GMT
ENV LANG=C.UTF-8
# Wed, 11 Mar 2026 18:40:07 GMT
ENV RUBY_VERSION=3.4.9
# Wed, 11 Mar 2026 18:40:07 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Wed, 11 Mar 2026 18:40:07 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Wed, 11 Mar 2026 18:40:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 11 Mar 2026 18:40:07 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 11 Mar 2026 18:40:07 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 11 Mar 2026 18:40:07 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Mar 2026 18:40:07 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 11 Mar 2026 18:40:07 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:249f1516d696eb1de7765ae9640d2c427d1271007f9bb2c8b250a134bf5ec510`  
		Last Modified: Wed, 11 Mar 2026 18:40:14 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f34844a4cbccd3f9ad8e8c7b25f28bb7b065c0effff0744a52ce3eaac71ba60a`  
		Last Modified: Wed, 11 Mar 2026 18:40:16 GMT  
		Size: 39.3 MB (39317845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffe3b9994ed25b76dbb70c47a4881b43e2706f058e07918d7ef8b6536f9e1157`  
		Last Modified: Wed, 11 Mar 2026 18:40:14 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-alpine` - unknown; unknown

```console
$ docker pull ruby@sha256:829d08f611633df1a91c33207a3a3434c3f45e9782121c3e8c0e4e7dc595352a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.8 KB (228774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:766734e6ec8e888ea5fd5cae63ce74e48237293efd96f06e9b7ebccd78abfbb6`

```dockerfile
```

-	Layers:
	-	`sha256:87cb5f3100c9efe4e930d0acbc65346625c4bccadc72bb998f7a14f4923f899a`  
		Last Modified: Wed, 11 Mar 2026 18:40:15 GMT  
		Size: 205.6 KB (205562 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f756002c2f9e30099f2f964a89d49c5a3cb1c46d35663e43158eeb460e3f879`  
		Last Modified: Wed, 11 Mar 2026 18:40:14 GMT  
		Size: 23.2 KB (23212 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-alpine` - linux; 386

```console
$ docker pull ruby@sha256:98aed2a0b8b1fb68d34a1267b566b4693743b4b40f815c6f9497ccbb568eac44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.4 MB (38423648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19f9e6d71097852cba2346f5c04f1c6e75be7cb112e530406246d2efa86c3e6a`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:11 GMT
ADD alpine-minirootfs-3.23.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:11 GMT
CMD ["/bin/sh"]
# Wed, 11 Mar 2026 18:29:20 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 11 Mar 2026 18:31:40 GMT
ENV LANG=C.UTF-8
# Wed, 11 Mar 2026 18:31:40 GMT
ENV RUBY_VERSION=3.4.9
# Wed, 11 Mar 2026 18:31:40 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Wed, 11 Mar 2026 18:31:40 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Wed, 11 Mar 2026 18:31:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 11 Mar 2026 18:31:40 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 11 Mar 2026 18:31:40 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 11 Mar 2026 18:31:40 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Mar 2026 18:31:41 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 11 Mar 2026 18:31:41 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:18bdec7eea78464ecf9b88f4ec630eaeb694ea1c0101ecd9c20eda20c9065e23`  
		Last Modified: Wed, 28 Jan 2026 01:18:16 GMT  
		Size: 3.7 MB (3686998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14fcdb25db79baffaa40efce1171875422fc5d3ad632aefd3d931a8117197659`  
		Last Modified: Wed, 11 Mar 2026 18:31:48 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea4aec5e3317b2a1ef25fbcc15c01875f42c0399e49a07f14eb84ad8a620a6fe`  
		Last Modified: Wed, 11 Mar 2026 18:31:49 GMT  
		Size: 34.7 MB (34736322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24a7759d014de47a1a9b520de8d68e8b099deffd4b00faa599dbcf8a5a9c9408`  
		Last Modified: Wed, 11 Mar 2026 18:31:47 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-alpine` - unknown; unknown

```console
$ docker pull ruby@sha256:afafa9ad2ea1b692326f48daaa1b560e79345aa8decab2cbcf69ec68cc5329de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.1 KB (226116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0627eff7e9a3f70c6dc55a895d79f974bc0e596524afee356d8111fd806eb66`

```dockerfile
```

-	Layers:
	-	`sha256:edce9b3ed7c33a6fe4b9ee84eda23978db569b95f05956e395f4c906c73d9f5f`  
		Last Modified: Wed, 11 Mar 2026 18:31:48 GMT  
		Size: 203.1 KB (203107 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2fa7a4d2e56c6a73a1d8b70f03f9eee3a8df2a28235a4f536d2c0d9cc101284a`  
		Last Modified: Wed, 11 Mar 2026 18:31:48 GMT  
		Size: 23.0 KB (23009 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-alpine` - linux; ppc64le

```console
$ docker pull ruby@sha256:4ff5b594f7bf2a8e2c962897a5b80e18f8033594a3d41d1104457474f0ee3ae6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.5 MB (40463968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bc118ce1726932dcccb151f61bef09f7bff158e11b7b9ee6a80cf3351351cc6`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Wed, 11 Mar 2026 18:49:55 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 11 Mar 2026 18:53:48 GMT
ENV LANG=C.UTF-8
# Wed, 11 Mar 2026 18:53:48 GMT
ENV RUBY_VERSION=3.4.9
# Wed, 11 Mar 2026 18:53:48 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Wed, 11 Mar 2026 18:53:48 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Wed, 11 Mar 2026 18:53:48 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 11 Mar 2026 18:53:48 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 11 Mar 2026 18:53:48 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 11 Mar 2026 18:53:48 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Mar 2026 18:53:48 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 11 Mar 2026 18:53:48 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ab7fe7357b6730f3b873ecfed8a7c179fa639225342646a325d07b682bbddd6`  
		Last Modified: Wed, 11 Mar 2026 18:54:03 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8aa4bb19cf950c1bb5d08c0ff214190a930096b5129edd76074e57ed22ff1ac`  
		Last Modified: Wed, 11 Mar 2026 18:54:04 GMT  
		Size: 36.6 MB (36633997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40642b9144f21a51622c220cbdb7b896a92d48aa19ef6d2a39e8f6528511aa62`  
		Last Modified: Wed, 11 Mar 2026 18:54:03 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-alpine` - unknown; unknown

```console
$ docker pull ruby@sha256:2ba91073ba93db2d0217a45be07f099514a4e568334a34d6e94711e31b8bbe0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.7 KB (225652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:962c5364993438d6bb7b7f1b4f5ab19ac278251341c4b75439e85a57c1ef9099`

```dockerfile
```

-	Layers:
	-	`sha256:c2c21d5dba58bc389c08d5894d031b12be7100d5e104e86167acaf5b79588b70`  
		Last Modified: Wed, 11 Mar 2026 18:54:03 GMT  
		Size: 202.5 KB (202537 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc6048bbb586275f67ad6c164ce603161ccc52f926df7ebe0d70c12132c0ab93`  
		Last Modified: Wed, 11 Mar 2026 18:54:03 GMT  
		Size: 23.1 KB (23115 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-alpine` - linux; riscv64

```console
$ docker pull ruby@sha256:693c98e4930989fd02f276deafa51e23071de1336fc121d6df1775abb7f860ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.8 MB (41798913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:548178e94802fa093b9ca61e5f1cd64f717280f3e2481173c4bdb882bd2c2b33`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Thu, 12 Mar 2026 03:53:42 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 12 Mar 2026 06:19:29 GMT
ENV LANG=C.UTF-8
# Thu, 12 Mar 2026 06:19:29 GMT
ENV RUBY_VERSION=3.4.9
# Thu, 12 Mar 2026 06:19:29 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Thu, 12 Mar 2026 06:19:29 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Thu, 12 Mar 2026 06:19:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 12 Mar 2026 06:19:29 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 12 Mar 2026 06:19:29 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 12 Mar 2026 06:19:29 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 12 Mar 2026 06:19:29 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 12 Mar 2026 06:19:29 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b2658f8d6bc4f9ac98323dd6ad1121d228d3092dafe45381f4c664a14d322a9`  
		Last Modified: Thu, 12 Mar 2026 06:20:40 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2b272fc074605e5ad20064fad75960f150926a2e7d5fc47f58cff91b867c801`  
		Last Modified: Thu, 12 Mar 2026 06:20:46 GMT  
		Size: 38.2 MB (38213297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a96d03462057b01c72ce095d08d54d47df6add125841530b6252b239a6fc185`  
		Last Modified: Thu, 12 Mar 2026 06:20:40 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-alpine` - unknown; unknown

```console
$ docker pull ruby@sha256:ab5fb2cf6d87f010f8d06f6ecaea161b181a0d0708d921a31e22328587b80179
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.6 KB (225648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1703ff0bcacce9622c05df2579e1253105d7afd596f030dcd83cd0e72f99945`

```dockerfile
```

-	Layers:
	-	`sha256:94c9b9c2a89265ac04a27319498c872e60759ff83c12ae1856fd72b76a2bbf6e`  
		Last Modified: Thu, 12 Mar 2026 06:20:40 GMT  
		Size: 202.5 KB (202533 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:574c3840a24adcb140d7ab605c24ee2dd13d03600677f4fbc8053ef20103a589`  
		Last Modified: Thu, 12 Mar 2026 06:20:40 GMT  
		Size: 23.1 KB (23115 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-alpine` - linux; s390x

```console
$ docker pull ruby@sha256:51556c5e9b99449d621af36189d33e93501c259223fb9d9b44fe665900e59255
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.9 MB (39854875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f202819a6d7dcc0078b7661866dd96698ef390c590caacfe62b4ce69a9ec777`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Wed, 11 Mar 2026 18:33:48 GMT
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
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 11 Mar 2026 18:36:21 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 11 Mar 2026 18:36:21 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 11 Mar 2026 18:36:21 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Mar 2026 18:36:21 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 11 Mar 2026 18:36:21 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8479c5f80d00944144568614fcf718e573f9142b23aeccaab258f01d89fb36ad`  
		Last Modified: Wed, 11 Mar 2026 18:36:33 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:150c84be2a985a3634bc9e992eff806636cf7a0b7d092308f72c320e80294078`  
		Last Modified: Wed, 11 Mar 2026 18:36:34 GMT  
		Size: 36.1 MB (36129213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4732af5aab56632692bb7176b42612c2da0e682a1c4c2a00f711052420a05c1`  
		Last Modified: Wed, 11 Mar 2026 18:36:33 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-alpine` - unknown; unknown

```console
$ docker pull ruby@sha256:f2bceac3575a144efe044ccb8c63f692eede4d7492d6a9961ddd8ac36c9a5940
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.5 KB (225546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0f40bbc411c45a82fe807b23f0ba698b08df13103e668d7ae3d8fa2db22a050`

```dockerfile
```

-	Layers:
	-	`sha256:f106b2933a8b1f2ba7e89f1dd832b799cf09eba2136aac324bfbbe5a0c6f2d5e`  
		Last Modified: Wed, 11 Mar 2026 18:36:33 GMT  
		Size: 202.5 KB (202491 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb11ef95fbf746d982763565d7373faa9b587432e7eb3d8394253084b36e3133`  
		Last Modified: Wed, 11 Mar 2026 18:36:33 GMT  
		Size: 23.1 KB (23055 bytes)  
		MIME: application/vnd.in-toto+json
