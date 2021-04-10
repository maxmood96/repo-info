## `ruby:buster`

```console
$ docker pull ruby@sha256:06f49974bf8ac940945199553c04712f8552d6658e3d552f5572038fb2b87a84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `ruby:buster` - linux; amd64

```console
$ docker pull ruby@sha256:07af18490b04bf48d8934fe13eb892f229b1f220502bca66fbcc69679904633d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.9 MB (340888950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f0597af290165462708d4404e003ab0ee7f135e2abde4cf344b318541eb1ff7`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 30 Mar 2021 21:49:16 GMT
ADD file:c254898ceb4172f05cd40460f8d0b1ca2d39d5178bdddd4e794c7d3fc5a60a03 in / 
# Tue, 30 Mar 2021 21:49:16 GMT
CMD ["bash"]
# Tue, 30 Mar 2021 23:03:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 30 Mar 2021 23:03:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 30 Mar 2021 23:03:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 30 Mar 2021 23:05:08 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 14:54:24 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 31 Mar 2021 14:54:24 GMT
ENV LANG=C.UTF-8
# Wed, 31 Mar 2021 14:54:24 GMT
ENV RUBY_MAJOR=3.0
# Mon, 05 Apr 2021 18:48:32 GMT
ENV RUBY_VERSION=3.0.1
# Mon, 05 Apr 2021 18:48:32 GMT
ENV RUBY_DOWNLOAD_SHA256=d06bccd382d03724b69f674bc46cd6957ba08ed07522694ce44b9e8ffc9c48e2
# Mon, 05 Apr 2021 18:52:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Mon, 05 Apr 2021 18:52:41 GMT
ENV GEM_HOME=/usr/local/bundle
# Mon, 05 Apr 2021 18:52:41 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Mon, 05 Apr 2021 18:52:41 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 05 Apr 2021 18:52:43 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Mon, 05 Apr 2021 18:52:43 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:004f1eed87df3f75f5e2a1a649fa7edd7f713d1300532fd0909bb39cd48437d7`  
		Last Modified: Tue, 30 Mar 2021 21:53:41 GMT  
		Size: 50.4 MB (50432842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d6f1e8117dbb1c6a57603cb4f321a861a08105a81bcc6b01b0ec2b78c8523a5`  
		Last Modified: Tue, 30 Mar 2021 23:14:05 GMT  
		Size: 7.8 MB (7832608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48c2faf66abec3dce9f54d6722ff592fce6dd4fb58a0d0b72282936c6598a3b3`  
		Last Modified: Tue, 30 Mar 2021 23:14:05 GMT  
		Size: 10.0 MB (9997208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:234b70d0479d7f16d7ee8d04e4ffdacc57d7d14313faf59d332f18b2e9418743`  
		Last Modified: Tue, 30 Mar 2021 23:14:37 GMT  
		Size: 51.8 MB (51840782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fa07a00e2f029c4b2c7f177a2b696f1b3510040cde4f5bb06ddbca98e7fbf76`  
		Last Modified: Tue, 30 Mar 2021 23:15:30 GMT  
		Size: 192.4 MB (192350814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaa60f1cb67e2445bd02786d2511bc7b95d242b8a0f5d98fe3370c010765938c`  
		Last Modified: Wed, 31 Mar 2021 15:31:40 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f90b4d2abce5d1141e50c154a2f1f679582f443370e4e4c9f5c689b78f1a813`  
		Last Modified: Mon, 05 Apr 2021 20:12:28 GMT  
		Size: 28.4 MB (28434321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62b5828fc036189daf4471f1cf416047105e5c82e8120ebf2cbfdf2e04d6731c`  
		Last Modified: Mon, 05 Apr 2021 20:12:25 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:buster` - linux; arm variant v5

```console
$ docker pull ruby@sha256:4e9d3421bed211a6d2c0cc4746f2db3fd269af16b5c6ad495a94edfd317f3cb8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.6 MB (313622033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c753ae740c7a1719b4888f61906e26d33f29ab1bfa704399a470407c737bafbf`
-	Default Command: `["irb"]`

```dockerfile
# Sat, 10 Apr 2021 00:51:03 GMT
ADD file:1b971030610d93168a72e3a82bac2d23dfaf0519be9b0cd24596e21761ce3837 in / 
# Sat, 10 Apr 2021 00:51:07 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 02:02:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 02:03:04 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 10 Apr 2021 02:04:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 02:07:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 07:22:41 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Sat, 10 Apr 2021 07:22:41 GMT
ENV LANG=C.UTF-8
# Sat, 10 Apr 2021 07:22:43 GMT
ENV RUBY_MAJOR=3.0
# Sat, 10 Apr 2021 07:22:43 GMT
ENV RUBY_VERSION=3.0.1
# Sat, 10 Apr 2021 07:22:45 GMT
ENV RUBY_DOWNLOAD_SHA256=d06bccd382d03724b69f674bc46cd6957ba08ed07522694ce44b9e8ffc9c48e2
# Sat, 10 Apr 2021 07:26:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Sat, 10 Apr 2021 07:26:21 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 10 Apr 2021 07:26:22 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 10 Apr 2021 07:26:23 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 10 Apr 2021 07:26:26 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sat, 10 Apr 2021 07:26:27 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:3c06faee41008db891ee3639eb45f5703ab8b865e7ed637997d6f9f9549ac0ef`  
		Last Modified: Sat, 10 Apr 2021 00:58:59 GMT  
		Size: 48.1 MB (48149130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b3cbc9c29f2277dd77644c394d167227ced2c7f34300a31a383eaecd0bce22f`  
		Last Modified: Sat, 10 Apr 2021 02:19:00 GMT  
		Size: 7.4 MB (7376533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66d381d109c0d0c28597405dae6e0dad96a189bb700571bea48863c242c56f59`  
		Last Modified: Sat, 10 Apr 2021 02:19:01 GMT  
		Size: 9.7 MB (9687553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7310d88e88f65f721330cf40b3f791383dc06d5855e03f2cf9a9b31d226b4521`  
		Last Modified: Sat, 10 Apr 2021 02:19:29 GMT  
		Size: 49.6 MB (49574896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:765ad24266a5e63808ae793eef8a22ab667abc5beb02022a35202c9e0422a320`  
		Last Modified: Sat, 10 Apr 2021 02:20:25 GMT  
		Size: 171.3 MB (171299713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c40c89738dd37f9774fd8aeca65c8b7a1958995b909d97988923f6fcbb0f45b1`  
		Last Modified: Sat, 10 Apr 2021 08:11:04 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28b55fc1240d16d8a2777e17d0b6acb405b0a882c1963fa377c648463ffd3f4a`  
		Last Modified: Sat, 10 Apr 2021 08:11:10 GMT  
		Size: 27.5 MB (27533833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d238c6dc2f43404f9790ba148253de607cc014006ea77eac6edfa8e9236f7f7`  
		Last Modified: Sat, 10 Apr 2021 08:11:04 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:buster` - linux; arm variant v7

```console
$ docker pull ruby@sha256:4bec4f6c4d3b09beb6db6b1f866205b163d6e509a32d138fdd4d0bf25b336f8a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.7 MB (305733583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa2687340807a4c80c575958c5f5000bd58655a4373ce0f3f00fa31eafb978e4`
-	Default Command: `["irb"]`

```dockerfile
# Sat, 10 Apr 2021 00:59:18 GMT
ADD file:bd2081229497eea2b33310cb1582b965581ca78b00b87cc8e42bdc8b9f350678 in / 
# Sat, 10 Apr 2021 00:59:20 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 06:05:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 06:05:42 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 10 Apr 2021 06:06:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 06:08:19 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 16:16:45 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Sat, 10 Apr 2021 16:16:48 GMT
ENV LANG=C.UTF-8
# Sat, 10 Apr 2021 16:16:49 GMT
ENV RUBY_MAJOR=3.0
# Sat, 10 Apr 2021 16:16:50 GMT
ENV RUBY_VERSION=3.0.1
# Sat, 10 Apr 2021 16:16:52 GMT
ENV RUBY_DOWNLOAD_SHA256=d06bccd382d03724b69f674bc46cd6957ba08ed07522694ce44b9e8ffc9c48e2
# Sat, 10 Apr 2021 16:20:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Sat, 10 Apr 2021 16:20:15 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 10 Apr 2021 16:20:20 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 10 Apr 2021 16:20:22 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 10 Apr 2021 16:20:32 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sat, 10 Apr 2021 16:20:35 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:de0ca59eb81518ffd92fbcd386251018f950dc16b1bd8ad2e642184db76be2a1`  
		Last Modified: Sat, 10 Apr 2021 01:07:26 GMT  
		Size: 45.9 MB (45915598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed23bfa8aaeab64a1ca00d3bead680f790be28326d14305705b2ee5227b4f2b7`  
		Last Modified: Sat, 10 Apr 2021 06:19:54 GMT  
		Size: 7.1 MB (7124181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20a12824e68a5072613049fad15fc8f0d209526ddd9d85787cc60d1b0d5073c0`  
		Last Modified: Sat, 10 Apr 2021 06:19:55 GMT  
		Size: 9.3 MB (9343784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da73a12ad465a34e484807c20e78927bd0dbd29a487e06024dbf3a1e21ba8a39`  
		Last Modified: Sat, 10 Apr 2021 06:20:19 GMT  
		Size: 47.4 MB (47356313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c237e38e8aae72f55dd563d8cf0e1a0f246537f88b9d91d6ccf514be502e31af`  
		Last Modified: Sat, 10 Apr 2021 06:21:08 GMT  
		Size: 168.6 MB (168558098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84366156ab90731176c0ee5a51aa9e3e8598ebc158ff11c7a3e36461ab8a8cc7`  
		Last Modified: Sat, 10 Apr 2021 17:18:09 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:123f606c44eb54d49b9ffa7ec4690c8dabc8f13b0184ebd0994995ad432c9163`  
		Last Modified: Sat, 10 Apr 2021 17:18:13 GMT  
		Size: 27.4 MB (27435235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:292759c03e58b30fde5fc939700b58a2a59c5bd92f2f97017795a8d1a612b2a7`  
		Last Modified: Sat, 10 Apr 2021 16:49:44 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:buster` - linux; arm64 variant v8

```console
$ docker pull ruby@sha256:705a718f0eeb941bef41b8d1507634944180e02ffb03069656fe891240a2670f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.2 MB (331154587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:137352ffe9a22552a53a21987b0d2588a9cf26144f2c7804144bcc67c51ac3cb`
-	Default Command: `["irb"]`

```dockerfile
# Sat, 10 Apr 2021 00:40:59 GMT
ADD file:320ad0e2a3d6c676ddb8ce5646b5a94d18d82a8868955da3a9379a261dfe1ffe in / 
# Sat, 10 Apr 2021 00:41:01 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 01:46:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 01:46:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 10 Apr 2021 01:47:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 01:49:15 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 16:01:24 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Sat, 10 Apr 2021 16:01:24 GMT
ENV LANG=C.UTF-8
# Sat, 10 Apr 2021 16:01:25 GMT
ENV RUBY_MAJOR=3.0
# Sat, 10 Apr 2021 16:01:26 GMT
ENV RUBY_VERSION=3.0.1
# Sat, 10 Apr 2021 16:01:28 GMT
ENV RUBY_DOWNLOAD_SHA256=d06bccd382d03724b69f674bc46cd6957ba08ed07522694ce44b9e8ffc9c48e2
# Sat, 10 Apr 2021 16:04:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Sat, 10 Apr 2021 16:04:28 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 10 Apr 2021 16:04:29 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 10 Apr 2021 16:04:31 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 10 Apr 2021 16:04:35 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sat, 10 Apr 2021 16:04:36 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:01cf0f0da10ede0eec0fc1c5fbfdeb63a447dfcc0a3c4419c0a4c3f0a2826636`  
		Last Modified: Sat, 10 Apr 2021 00:47:28 GMT  
		Size: 49.2 MB (49225782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c667eb56cd05909001c1c50e81cbc75e290fd8e353f974bab4246a0d4fc484ca`  
		Last Modified: Sat, 10 Apr 2021 02:01:00 GMT  
		Size: 7.7 MB (7695101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27ca15a4cef673e0e1a7bc3e659f4653df9bce82b945e367475e436852cc7880`  
		Last Modified: Sat, 10 Apr 2021 02:00:59 GMT  
		Size: 10.0 MB (9984406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b7f1cf823a7fca9771e278355d8924fac8d9cef1f8e3ecbc87332c4859d1d4f`  
		Last Modified: Sat, 10 Apr 2021 02:01:23 GMT  
		Size: 52.2 MB (52167974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afc82e36e8c811c7e1f7adf3207add9dd5c7150fe7cd8e429d49f47b71057f7b`  
		Last Modified: Sat, 10 Apr 2021 02:02:13 GMT  
		Size: 183.9 MB (183903910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74d3220f5df665fc2ae0fe82c2eac66e22d5f0b79cd183712f26b2aee608e719`  
		Last Modified: Sat, 10 Apr 2021 16:48:08 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:343b7cfeb72fee40a869ea30c613bfbfa2b18c523a3c07b26d56b07baf300d13`  
		Last Modified: Sat, 10 Apr 2021 16:48:15 GMT  
		Size: 28.2 MB (28177039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d71ea9c896489d7cddfab5194badd6601f92635eca67d5cf614a11bdbc7f267`  
		Last Modified: Sat, 10 Apr 2021 16:48:08 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:buster` - linux; 386

```console
$ docker pull ruby@sha256:100d3eaee4ce6f695e9e936bb04c8789bbf628c417f602ded8f7d0a75aebdc31
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.6 MB (349587369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ebabe7d77a2cf21e051fba1e31b6c3b509e976db5bf107af0f5eb419a4fb281`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 30 Mar 2021 21:39:30 GMT
ADD file:a2981af3d3aa369b11e802f23b175abfdb0f7636cdeec3aed67488d7a1f28a19 in / 
# Tue, 30 Mar 2021 21:39:30 GMT
CMD ["bash"]
# Tue, 30 Mar 2021 23:56:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 30 Mar 2021 23:56:50 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 30 Mar 2021 23:57:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 30 Mar 2021 23:58:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 11:25:16 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 31 Mar 2021 11:25:16 GMT
ENV LANG=C.UTF-8
# Wed, 31 Mar 2021 11:25:16 GMT
ENV RUBY_MAJOR=3.0
# Mon, 05 Apr 2021 18:34:48 GMT
ENV RUBY_VERSION=3.0.1
# Mon, 05 Apr 2021 18:34:49 GMT
ENV RUBY_DOWNLOAD_SHA256=d06bccd382d03724b69f674bc46cd6957ba08ed07522694ce44b9e8ffc9c48e2
# Mon, 05 Apr 2021 18:39:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Mon, 05 Apr 2021 18:39:34 GMT
ENV GEM_HOME=/usr/local/bundle
# Mon, 05 Apr 2021 18:39:35 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Mon, 05 Apr 2021 18:39:35 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 05 Apr 2021 18:39:36 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Mon, 05 Apr 2021 18:39:36 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:a3a3dbaddd2d56d7418508211551c461f826d1cae349d39a355a1c22fe140b36`  
		Last Modified: Tue, 30 Mar 2021 21:46:05 GMT  
		Size: 51.2 MB (51198756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de970e2d41035ffe1a656cc3d1f8e17bc7b8539b23745405b8fccf25d10fd312`  
		Last Modified: Wed, 31 Mar 2021 00:08:00 GMT  
		Size: 8.0 MB (7997659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c27a2cf0e2e609cc89ee5b623626f822424bdc818ac5eab541a7a7b158ef0c01`  
		Last Modified: Wed, 31 Mar 2021 00:08:00 GMT  
		Size: 10.3 MB (10340050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b7a5ef36d45f69154fe2b83a8e658d4f08c45428493e8e1cc74a8b03b3c4799`  
		Last Modified: Wed, 31 Mar 2021 00:08:31 GMT  
		Size: 53.4 MB (53438017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98e4b62cf2ad846ba0bec17add38106ebdfbe771009574c1a033f9698ba80e36`  
		Last Modified: Wed, 31 Mar 2021 00:09:26 GMT  
		Size: 198.9 MB (198898090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb8dc3e0c865387be62882f043ea642d4ce3950eb8403f4e1a19e9f0284403f0`  
		Last Modified: Wed, 31 Mar 2021 12:11:08 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb02f22a037c1ee1ae94419ff52af43d251786d4a1bf7804a924d6584ee18492`  
		Last Modified: Mon, 05 Apr 2021 20:10:19 GMT  
		Size: 27.7 MB (27714422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb6791dfc15463d73bf87085163a42c9f3b9cdd3c9665d747b8bf94b3e1324d4`  
		Last Modified: Mon, 05 Apr 2021 20:10:12 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:buster` - linux; mips64le

```console
$ docker pull ruby@sha256:441a810c776c3ccdc2a4e1d62b157cdbfe0a112af94eb3209b74e8a921f10964
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.7 MB (325700716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afedc6ddf9cef54921927f7dbd24034ee2f42875ddede5774732d86367094e60`
-	Default Command: `["irb"]`

```dockerfile
# Sat, 10 Apr 2021 01:09:16 GMT
ADD file:76d04de63b0abd4b467c1af49e65bf93f854f7a99965790bf5ae8a5d5d4eff52 in / 
# Sat, 10 Apr 2021 01:09:17 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 02:07:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 02:07:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 10 Apr 2021 02:08:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 02:11:02 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 14:38:15 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Sat, 10 Apr 2021 14:38:16 GMT
ENV LANG=C.UTF-8
# Sat, 10 Apr 2021 14:38:16 GMT
ENV RUBY_MAJOR=3.0
# Sat, 10 Apr 2021 14:38:16 GMT
ENV RUBY_VERSION=3.0.1
# Sat, 10 Apr 2021 14:38:17 GMT
ENV RUBY_DOWNLOAD_SHA256=d06bccd382d03724b69f674bc46cd6957ba08ed07522694ce44b9e8ffc9c48e2
# Sat, 10 Apr 2021 14:47:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Sat, 10 Apr 2021 14:47:26 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 10 Apr 2021 14:47:27 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 10 Apr 2021 14:47:27 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 10 Apr 2021 14:47:29 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sat, 10 Apr 2021 14:47:29 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:437194c1aac057ffc15e81662666c0514263f66844c3fb685f8eb711c9b1d5b3`  
		Last Modified: Sat, 10 Apr 2021 01:15:20 GMT  
		Size: 49.1 MB (49081824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfb75a7e91e7c3217150c14a2e864c3194b8d8fa134057032352db7e33215141`  
		Last Modified: Sat, 10 Apr 2021 02:18:48 GMT  
		Size: 7.3 MB (7252482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a0a522cec664fdadd94fceaaa3083e5793143f1d6402669712f09e5c634a3be`  
		Last Modified: Sat, 10 Apr 2021 02:18:48 GMT  
		Size: 10.0 MB (10016374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f883e819b37d86e804f6ee7839bd1b05fdbd362fbc25fa493e45714b68135398`  
		Last Modified: Sat, 10 Apr 2021 02:19:40 GMT  
		Size: 50.8 MB (50845406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a89d961f9bb62172a5fca020c082f25f14646a36827a57de99f497e63a6d317f`  
		Last Modified: Sat, 10 Apr 2021 02:21:52 GMT  
		Size: 179.9 MB (179856176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:604db71f14b7ed44afca3c27cf13d368e038c04dbe9bfaaf851d1ac2103fc22a`  
		Last Modified: Sat, 10 Apr 2021 15:50:24 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f7bde1638bcd10f4a0b372f0e307fc0a1cf58fe31ccbc72c20d8cf527e49234`  
		Last Modified: Sat, 10 Apr 2021 15:50:34 GMT  
		Size: 28.6 MB (28648113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f800f00a3b8cef5e7e30aa2c60e3e77cb8f9b6c1371871e546cd409bec1ad799`  
		Last Modified: Sat, 10 Apr 2021 15:50:22 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:buster` - linux; ppc64le

```console
$ docker pull ruby@sha256:10c5a8b2a85e3343c973b615cfa504f61393d2ac6926f60b1c8683af13f70170
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **362.7 MB (362681337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83900f60a1ba829c2d3fb2bde429cb7b98ff800f75f5f70dad72d55c509537c6`
-	Default Command: `["irb"]`

```dockerfile
# Sat, 10 Apr 2021 01:26:11 GMT
ADD file:0671a70f02e705f591888f40e87a43122cd95a6ead3df61becbc4a7fb1c7ec43 in / 
# Sat, 10 Apr 2021 01:26:21 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 02:24:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 02:25:23 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 10 Apr 2021 02:28:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 02:46:24 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 14:48:38 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Sat, 10 Apr 2021 14:48:46 GMT
ENV LANG=C.UTF-8
# Sat, 10 Apr 2021 14:48:55 GMT
ENV RUBY_MAJOR=3.0
# Sat, 10 Apr 2021 14:49:07 GMT
ENV RUBY_VERSION=3.0.1
# Sat, 10 Apr 2021 14:49:17 GMT
ENV RUBY_DOWNLOAD_SHA256=d06bccd382d03724b69f674bc46cd6957ba08ed07522694ce44b9e8ffc9c48e2
# Sat, 10 Apr 2021 14:53:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Sat, 10 Apr 2021 14:54:01 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 10 Apr 2021 14:54:13 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 10 Apr 2021 14:54:25 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 10 Apr 2021 14:54:35 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sat, 10 Apr 2021 14:54:56 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:d018a28ea8249b332e6bce3cb93862d5b05dba493dbaf3531505ce3a3701001b`  
		Last Modified: Sat, 10 Apr 2021 01:33:24 GMT  
		Size: 54.2 MB (54179922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa1d690a663e373c9e09abb435ea1b9002ad11e9118b98f27767951ec963437e`  
		Last Modified: Sat, 10 Apr 2021 03:04:29 GMT  
		Size: 8.3 MB (8271815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de29ad508d11980c81b06641138821d118c6de9064228c4ee33bfedd156acf15`  
		Last Modified: Sat, 10 Apr 2021 03:04:29 GMT  
		Size: 10.7 MB (10727718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b93e64fc4b56829740f482d15d41f6be2348195960f65820b5565f1a7e81b7df`  
		Last Modified: Sat, 10 Apr 2021 03:04:56 GMT  
		Size: 57.5 MB (57457359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe1ce5bcac35bc5be092a46fb837cbe55211e2fa50c72e73fa34f3f056a9c9c6`  
		Last Modified: Sat, 10 Apr 2021 03:05:45 GMT  
		Size: 203.2 MB (203192237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a09a698f8c9e9c424a6a3cd41363b51a975178739298fde2c6548d01cc25bf4b`  
		Last Modified: Sat, 10 Apr 2021 15:54:13 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76872b4cf65a6464eb97d9e7c98ff9ac43683a979cef2071d199525a94115a61`  
		Last Modified: Sat, 10 Apr 2021 15:54:19 GMT  
		Size: 28.9 MB (28851911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c50183811d6da6cb2bfd76d5cda9b958b0018ed4b3457a6a7fc58c54333d3a6`  
		Last Modified: Sat, 10 Apr 2021 15:54:13 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:buster` - linux; s390x

```console
$ docker pull ruby@sha256:bab6d6d5644931255915f70ea589afd57c18829c45e096ca6a13b3291b06aef4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.2 MB (323156015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abe5e4981888f2503af901b05ce99012c27cddcd4793435e5ffc3d14fe6b343d`
-	Default Command: `["irb"]`

```dockerfile
# Sat, 10 Apr 2021 00:42:07 GMT
ADD file:4df1e9998bf12ac6b068948127db30e29fdc3196e27d72adf972c6c1cc6ce2a0 in / 
# Sat, 10 Apr 2021 00:42:10 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 01:27:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 01:28:04 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 10 Apr 2021 01:28:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 01:29:13 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 01:49:33 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Sat, 10 Apr 2021 01:49:33 GMT
ENV LANG=C.UTF-8
# Sat, 10 Apr 2021 01:49:34 GMT
ENV RUBY_MAJOR=3.0
# Sat, 10 Apr 2021 01:49:34 GMT
ENV RUBY_VERSION=3.0.1
# Sat, 10 Apr 2021 01:49:34 GMT
ENV RUBY_DOWNLOAD_SHA256=d06bccd382d03724b69f674bc46cd6957ba08ed07522694ce44b9e8ffc9c48e2
# Sat, 10 Apr 2021 01:51:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Sat, 10 Apr 2021 01:51:20 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 10 Apr 2021 01:51:20 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 10 Apr 2021 01:51:20 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 10 Apr 2021 01:51:21 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sat, 10 Apr 2021 01:51:21 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:03bd9fa68773b62afcbde0348c41cadd08d602d2731d955581cc322351e8be39`  
		Last Modified: Sat, 10 Apr 2021 00:45:31 GMT  
		Size: 49.0 MB (49000527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:462b0816104d88c29adf6ff712d656e5b8ac57f3dfb17fdcb1cb5d2090b85fad`  
		Last Modified: Sat, 10 Apr 2021 01:33:41 GMT  
		Size: 7.4 MB (7400505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e318693fbecdee6c86a20d06396ea273a6f98a120b3e5a91f973416800bcaac2`  
		Last Modified: Sat, 10 Apr 2021 01:33:41 GMT  
		Size: 9.9 MB (9883023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ee83389c8b4e83fa875720df895d5659e47a3d1a138254412dd52760e56be38`  
		Last Modified: Sat, 10 Apr 2021 01:33:54 GMT  
		Size: 51.4 MB (51380124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:043051c2cc4d79d1554d756d71d9de5d55a6ec6cc6608e569a849a5e54c0d630`  
		Last Modified: Sat, 10 Apr 2021 01:34:21 GMT  
		Size: 176.9 MB (176868356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73ad59ded229821811904eeb32943484d31750d09bd19d6217fb7fb41e0987c4`  
		Last Modified: Sat, 10 Apr 2021 02:21:56 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64d7975c6a29d018c0d83d0ebe3aff1ffb8c57fea4999c87b5f6d4604042ff68`  
		Last Modified: Sat, 10 Apr 2021 02:21:58 GMT  
		Size: 28.6 MB (28623107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e73730d4a3770fea4ff3e5c7b5ebe98ad68c83d7c10fa1849019f6ce9036ec1`  
		Last Modified: Sat, 10 Apr 2021 02:21:56 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
