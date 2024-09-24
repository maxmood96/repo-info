## `bash:5-alpine3.20`

```console
$ docker pull bash@sha256:ce062497c248eb1cf4d32927f8c1780cce158d3ed0658c586a5be7308d583cbb
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

### `bash:5-alpine3.20` - linux; amd64

```console
$ docker pull bash@sha256:5b36f2727af2f740b43b8591524f9335e8fa7fcff3bcb0ba8989588b237f6e00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6318704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91698992478c66011fc925293008447d42903e2eada741689c7d96f22a5d2a1b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Mon, 23 Sep 2024 22:17:43 GMT
ENV _BASH_VERSION=5.2.37
# Mon, 23 Sep 2024 22:17:43 GMT
ENV _BASH_BASELINE=5.2.37
# Mon, 23 Sep 2024 22:17:43 GMT
ENV _BASH_BASELINE_PATCH=37
# Mon, 23 Sep 2024 22:17:43 GMT
ENV _BASH_LATEST_PATCH=37
# Mon, 23 Sep 2024 22:17:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz"; 	wget -O bash.tar.gz.sig "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz.sig"; 		: "${_BASH_BASELINE_PATCH:=0}" "${_BASH_LATEST_PATCH:=0}"; 	if [ "$_BASH_LATEST_PATCH" -gt "$_BASH_BASELINE_PATCH" ]; then 		mkdir -p bash-patches; 		first="$(printf '%03d' "$(( _BASH_BASELINE_PATCH + 1 ))")"; 		last="$(printf '%03d' "$_BASH_LATEST_PATCH")"; 		majorMinor="${_BASH_VERSION%.*}"; 		for patch in $(seq -w "$first" "$last"); do 			url="https://ftp.gnu.org/gnu/bash/bash-$majorMinor-patches/bash${majorMinor//./}-$patch"; 			wget -O "bash-patches/$patch" "$url"; 			wget -O "bash-patches/$patch.sig" "$url.sig"; 		done; 	fi; 		apk add --no-cache --virtual .gpg-deps gnupg; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7C0135FB088AAF6C66C650B9BB5869F064EA74AB; 	gpg --batch --verify bash.tar.gz.sig bash.tar.gz; 	rm bash.tar.gz.sig; 	if [ -d bash-patches ]; then 		for sig in bash-patches/*.sig; do 			p="${sig%.sig}"; 			gpg --batch --verify "$sig" "$p"; 			rm "$sig"; 		done; 	fi; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apk del --no-network .gpg-deps; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	[ "$(bash -c 'echo "${BASH_VERSION%%[^0-9.]*}"')" = "$_BASH_VERSION" ]; 	bash -c 'help' > /dev/null # buildkit
# Mon, 23 Sep 2024 22:17:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Sep 2024 22:17:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Sep 2024 22:17:43 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:467989b961c339a26ad914f43d509746413029c70d9eeb7b81910d77c0137341`  
		Last Modified: Tue, 24 Sep 2024 01:00:45 GMT  
		Size: 2.7 MB (2694566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1517fbc9c0766586f9288794ffb0294029804ac39f95160b2bf98287dd918af`  
		Last Modified: Tue, 24 Sep 2024 01:00:45 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:5-alpine3.20` - unknown; unknown

```console
$ docker pull bash@sha256:19f7d6d288cbb27e3f10139043cb685b693ed743231054429ac7f077cc8e9fd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51378e9662e0c1a1332d59addfe0a59f00edfffabd05bd03ca5f3b19c011b86e`

```dockerfile
```

-	Layers:
	-	`sha256:886cb10c1b3603754a76b6db95ae11df079f86db675f2b52e30420d7acc21d67`  
		Last Modified: Tue, 24 Sep 2024 01:00:45 GMT  
		Size: 20.6 KB (20576 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:5-alpine3.20` - linux; arm variant v6

```console
$ docker pull bash@sha256:357c70e2b81ed7ca00b9802a01eb16f3d3f3314e2264eb2b8f23cfb5879f4051
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6004461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68551f0e785ba38973c7fe3fd53d4dfc31d2488089cbe931220a14e080faf9cb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
CMD ["/bin/sh"]
# Mon, 23 Sep 2024 22:17:43 GMT
ENV _BASH_VERSION=5.2.37
# Mon, 23 Sep 2024 22:17:43 GMT
ENV _BASH_BASELINE=5.2.37
# Mon, 23 Sep 2024 22:17:43 GMT
ENV _BASH_BASELINE_PATCH=37
# Mon, 23 Sep 2024 22:17:43 GMT
ENV _BASH_LATEST_PATCH=37
# Mon, 23 Sep 2024 22:17:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz"; 	wget -O bash.tar.gz.sig "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz.sig"; 		: "${_BASH_BASELINE_PATCH:=0}" "${_BASH_LATEST_PATCH:=0}"; 	if [ "$_BASH_LATEST_PATCH" -gt "$_BASH_BASELINE_PATCH" ]; then 		mkdir -p bash-patches; 		first="$(printf '%03d' "$(( _BASH_BASELINE_PATCH + 1 ))")"; 		last="$(printf '%03d' "$_BASH_LATEST_PATCH")"; 		majorMinor="${_BASH_VERSION%.*}"; 		for patch in $(seq -w "$first" "$last"); do 			url="https://ftp.gnu.org/gnu/bash/bash-$majorMinor-patches/bash${majorMinor//./}-$patch"; 			wget -O "bash-patches/$patch" "$url"; 			wget -O "bash-patches/$patch.sig" "$url.sig"; 		done; 	fi; 		apk add --no-cache --virtual .gpg-deps gnupg; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7C0135FB088AAF6C66C650B9BB5869F064EA74AB; 	gpg --batch --verify bash.tar.gz.sig bash.tar.gz; 	rm bash.tar.gz.sig; 	if [ -d bash-patches ]; then 		for sig in bash-patches/*.sig; do 			p="${sig%.sig}"; 			gpg --batch --verify "$sig" "$p"; 			rm "$sig"; 		done; 	fi; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apk del --no-network .gpg-deps; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	[ "$(bash -c 'echo "${BASH_VERSION%%[^0-9.]*}"')" = "$_BASH_VERSION" ]; 	bash -c 'help' > /dev/null # buildkit
# Mon, 23 Sep 2024 22:17:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Sep 2024 22:17:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Sep 2024 22:17:43 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a764666fca6874dabfff5ea1115cc56dceaf8cf53cf0e5f2e11444f9c5a7d80`  
		Last Modified: Tue, 24 Sep 2024 01:00:50 GMT  
		Size: 2.6 MB (2637624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c1c2e8011e53d560d803e6a65af2bd213a0a452d04df853d8a37b852bde7852`  
		Last Modified: Tue, 24 Sep 2024 01:00:50 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:5-alpine3.20` - unknown; unknown

```console
$ docker pull bash@sha256:5fc0bacda3b7a036c28f25052f56c512878e9be32cad40bcc89648f8f2dd97fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66896b34d4562d56ff29d345d7faa35711b1365df487883547c566bd32e0bfbf`

```dockerfile
```

-	Layers:
	-	`sha256:664034cfd7df373c070c150034d5c16cb0d498b76a9f124d4a1becc373fd6520`  
		Last Modified: Tue, 24 Sep 2024 01:00:50 GMT  
		Size: 20.7 KB (20678 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:5-alpine3.20` - linux; arm variant v7

```console
$ docker pull bash@sha256:363457f5e5effb4955936cc8155d715cbc8cd48e21971abe5ecf8444a73f4470
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5686810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08d6f33fc96e9719cc6557e25e50fa25546e6a9c208d406487ff0bf327f20bdd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:00 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Fri, 06 Sep 2024 22:08:01 GMT
CMD ["/bin/sh"]
# Mon, 23 Sep 2024 22:17:43 GMT
ENV _BASH_VERSION=5.2.37
# Mon, 23 Sep 2024 22:17:43 GMT
ENV _BASH_BASELINE=5.2.37
# Mon, 23 Sep 2024 22:17:43 GMT
ENV _BASH_BASELINE_PATCH=37
# Mon, 23 Sep 2024 22:17:43 GMT
ENV _BASH_LATEST_PATCH=37
# Mon, 23 Sep 2024 22:17:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz"; 	wget -O bash.tar.gz.sig "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz.sig"; 		: "${_BASH_BASELINE_PATCH:=0}" "${_BASH_LATEST_PATCH:=0}"; 	if [ "$_BASH_LATEST_PATCH" -gt "$_BASH_BASELINE_PATCH" ]; then 		mkdir -p bash-patches; 		first="$(printf '%03d' "$(( _BASH_BASELINE_PATCH + 1 ))")"; 		last="$(printf '%03d' "$_BASH_LATEST_PATCH")"; 		majorMinor="${_BASH_VERSION%.*}"; 		for patch in $(seq -w "$first" "$last"); do 			url="https://ftp.gnu.org/gnu/bash/bash-$majorMinor-patches/bash${majorMinor//./}-$patch"; 			wget -O "bash-patches/$patch" "$url"; 			wget -O "bash-patches/$patch.sig" "$url.sig"; 		done; 	fi; 		apk add --no-cache --virtual .gpg-deps gnupg; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7C0135FB088AAF6C66C650B9BB5869F064EA74AB; 	gpg --batch --verify bash.tar.gz.sig bash.tar.gz; 	rm bash.tar.gz.sig; 	if [ -d bash-patches ]; then 		for sig in bash-patches/*.sig; do 			p="${sig%.sig}"; 			gpg --batch --verify "$sig" "$p"; 			rm "$sig"; 		done; 	fi; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apk del --no-network .gpg-deps; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	[ "$(bash -c 'echo "${BASH_VERSION%%[^0-9.]*}"')" = "$_BASH_VERSION" ]; 	bash -c 'help' > /dev/null # buildkit
# Mon, 23 Sep 2024 22:17:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Sep 2024 22:17:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Sep 2024 22:17:43 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:190083d7a9340455a3ee0783477a39bdb60f282d65605aa0590a7cdfd1a20679`  
		Last Modified: Tue, 24 Sep 2024 01:00:34 GMT  
		Size: 2.6 MB (2590974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca1c307d994e92a18e847939c75014e6e6fe11c50c49b155621a90a68f37fd3f`  
		Last Modified: Tue, 24 Sep 2024 01:00:33 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:5-alpine3.20` - unknown; unknown

```console
$ docker pull bash@sha256:2047f33ce5154f61a3709e269fa4219653c1bda3994b565ac2f9f4b194aba6a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.0 KB (131996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea6e7fe7ba77095686e06bac3c569495d33cca2a1bf0d5bcbbc7583b68bb76b1`

```dockerfile
```

-	Layers:
	-	`sha256:7416d84f99cdeaeaa1ec33e1a3378a8270360195fce149e72ea66678deb50de4`  
		Last Modified: Tue, 24 Sep 2024 01:00:33 GMT  
		Size: 111.1 KB (111099 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8905499a6135493e11b3a63fd281336dcf5215c6b3986612d71d92c7fd34b821`  
		Last Modified: Tue, 24 Sep 2024 01:00:33 GMT  
		Size: 20.9 KB (20897 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:5-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull bash@sha256:7d770df6f5181e3f2f83eee5e6a0e9f0e755dfa87d2fa6c32fe7ed791879a25b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6869168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3c8b7dbb4fe2a403c6094191e4fb7d1677ed6094b87fa824a3a50022454551d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Mon, 23 Sep 2024 22:17:43 GMT
ENV _BASH_VERSION=5.2.37
# Mon, 23 Sep 2024 22:17:43 GMT
ENV _BASH_BASELINE=5.2.37
# Mon, 23 Sep 2024 22:17:43 GMT
ENV _BASH_BASELINE_PATCH=37
# Mon, 23 Sep 2024 22:17:43 GMT
ENV _BASH_LATEST_PATCH=37
# Mon, 23 Sep 2024 22:17:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz"; 	wget -O bash.tar.gz.sig "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz.sig"; 		: "${_BASH_BASELINE_PATCH:=0}" "${_BASH_LATEST_PATCH:=0}"; 	if [ "$_BASH_LATEST_PATCH" -gt "$_BASH_BASELINE_PATCH" ]; then 		mkdir -p bash-patches; 		first="$(printf '%03d' "$(( _BASH_BASELINE_PATCH + 1 ))")"; 		last="$(printf '%03d' "$_BASH_LATEST_PATCH")"; 		majorMinor="${_BASH_VERSION%.*}"; 		for patch in $(seq -w "$first" "$last"); do 			url="https://ftp.gnu.org/gnu/bash/bash-$majorMinor-patches/bash${majorMinor//./}-$patch"; 			wget -O "bash-patches/$patch" "$url"; 			wget -O "bash-patches/$patch.sig" "$url.sig"; 		done; 	fi; 		apk add --no-cache --virtual .gpg-deps gnupg; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7C0135FB088AAF6C66C650B9BB5869F064EA74AB; 	gpg --batch --verify bash.tar.gz.sig bash.tar.gz; 	rm bash.tar.gz.sig; 	if [ -d bash-patches ]; then 		for sig in bash-patches/*.sig; do 			p="${sig%.sig}"; 			gpg --batch --verify "$sig" "$p"; 			rm "$sig"; 		done; 	fi; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apk del --no-network .gpg-deps; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	[ "$(bash -c 'echo "${BASH_VERSION%%[^0-9.]*}"')" = "$_BASH_VERSION" ]; 	bash -c 'help' > /dev/null # buildkit
# Mon, 23 Sep 2024 22:17:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Sep 2024 22:17:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Sep 2024 22:17:43 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:078a9d80d4290b397164667d15a550b3eaa1091a1c82fa1b6c60f1aa17a026e5`  
		Last Modified: Tue, 24 Sep 2024 01:05:54 GMT  
		Size: 2.8 MB (2781187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f94c0dcbcefbd703752d20f28f543de4435ed76001efa91422953377d7e7be11`  
		Last Modified: Tue, 24 Sep 2024 01:05:53 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:5-alpine3.20` - unknown; unknown

```console
$ docker pull bash@sha256:1817c99eff048bdfb3a571ad95cbea0ad0ebd134a6c1cbc93b86b1ffd06aeec4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.3 KB (132278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8a45f12bfebb90feb437ecbfa0cba8d39a4c55ff24788ef256569fd040bb480`

```dockerfile
```

-	Layers:
	-	`sha256:8500c042663ba57503324df8fb5938939a28ce6bf28f8f3cc0c24f434acff284`  
		Last Modified: Tue, 24 Sep 2024 01:05:54 GMT  
		Size: 111.1 KB (111135 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c27b1c204e42797a9de049d772916335767dc3e9d2faafbb12ea390649ba6bd`  
		Last Modified: Tue, 24 Sep 2024 01:05:53 GMT  
		Size: 21.1 KB (21143 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:5-alpine3.20` - linux; 386

```console
$ docker pull bash@sha256:e90489de13e5f1d8d33b8074ba13b6e84ee2129b9a0f3bc6f45cab018ddc4e50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6113891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afdf08258b1f60ef7ceec90b0988d5c2b71e18c58cb26082e92f43ec3e4f973c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 06 Sep 2024 22:41:21 GMT
ADD file:00e6c22c1917031dd97c411814ae384c25a7f2bb91890494a73ea34f3c168453 in / 
# Fri, 06 Sep 2024 22:41:21 GMT
CMD ["/bin/sh"]
# Mon, 23 Sep 2024 22:17:43 GMT
ENV _BASH_VERSION=5.2.37
# Mon, 23 Sep 2024 22:17:43 GMT
ENV _BASH_BASELINE=5.2.37
# Mon, 23 Sep 2024 22:17:43 GMT
ENV _BASH_BASELINE_PATCH=37
# Mon, 23 Sep 2024 22:17:43 GMT
ENV _BASH_LATEST_PATCH=37
# Mon, 23 Sep 2024 22:17:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz"; 	wget -O bash.tar.gz.sig "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz.sig"; 		: "${_BASH_BASELINE_PATCH:=0}" "${_BASH_LATEST_PATCH:=0}"; 	if [ "$_BASH_LATEST_PATCH" -gt "$_BASH_BASELINE_PATCH" ]; then 		mkdir -p bash-patches; 		first="$(printf '%03d' "$(( _BASH_BASELINE_PATCH + 1 ))")"; 		last="$(printf '%03d' "$_BASH_LATEST_PATCH")"; 		majorMinor="${_BASH_VERSION%.*}"; 		for patch in $(seq -w "$first" "$last"); do 			url="https://ftp.gnu.org/gnu/bash/bash-$majorMinor-patches/bash${majorMinor//./}-$patch"; 			wget -O "bash-patches/$patch" "$url"; 			wget -O "bash-patches/$patch.sig" "$url.sig"; 		done; 	fi; 		apk add --no-cache --virtual .gpg-deps gnupg; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7C0135FB088AAF6C66C650B9BB5869F064EA74AB; 	gpg --batch --verify bash.tar.gz.sig bash.tar.gz; 	rm bash.tar.gz.sig; 	if [ -d bash-patches ]; then 		for sig in bash-patches/*.sig; do 			p="${sig%.sig}"; 			gpg --batch --verify "$sig" "$p"; 			rm "$sig"; 		done; 	fi; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apk del --no-network .gpg-deps; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	[ "$(bash -c 'echo "${BASH_VERSION%%[^0-9.]*}"')" = "$_BASH_VERSION" ]; 	bash -c 'help' > /dev/null # buildkit
# Mon, 23 Sep 2024 22:17:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Sep 2024 22:17:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Sep 2024 22:17:43 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:2689ac6c14fd48d5dbd1df1dd2d317f177e131f689c1a010922edcd778518efd`  
		Last Modified: Fri, 06 Sep 2024 22:41:47 GMT  
		Size: 3.5 MB (3469165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e344729503fe7e03c181f6860c105f99d3360277791b7bbd35fb11770fb12b96`  
		Last Modified: Tue, 24 Sep 2024 01:00:52 GMT  
		Size: 2.6 MB (2644394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4044b64b2038673ac17a65e8d67ddaa5789f5440055eb38e4049c57957dfb283`  
		Last Modified: Tue, 24 Sep 2024 01:00:51 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:5-alpine3.20` - unknown; unknown

```console
$ docker pull bash@sha256:d6a6028fe14f141f8d5c410658bc4f86980f10a9ab2c701123e1cbadaae349c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6bc14309a1532ca78066a23fbe24707b65b83188d3959e564de4a783c7dcdd7`

```dockerfile
```

-	Layers:
	-	`sha256:66d29ef1db07b36e5d03bb96f2fd859fac1fd150fc7dc92d8117126b07aa6f75`  
		Last Modified: Tue, 24 Sep 2024 01:00:51 GMT  
		Size: 20.5 KB (20527 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:5-alpine3.20` - linux; ppc64le

```console
$ docker pull bash@sha256:ee3860e3d95a3c8fc930df60b7770fd3e4aa94af1b6ce0fabb8595490807b8fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6518153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a293a79c37dc9357e7c8a1e355bd4dc65ebab7790fcb105649f84bab852d9a64`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 06 Sep 2024 22:26:06 GMT
ADD file:c1f14e23acaff59e2dc7a11f65f8fdfbed8be1350a135493a06b692ecefb26cc in / 
# Fri, 06 Sep 2024 22:26:07 GMT
CMD ["/bin/sh"]
# Mon, 23 Sep 2024 22:17:43 GMT
ENV _BASH_VERSION=5.2.37
# Mon, 23 Sep 2024 22:17:43 GMT
ENV _BASH_BASELINE=5.2.37
# Mon, 23 Sep 2024 22:17:43 GMT
ENV _BASH_BASELINE_PATCH=37
# Mon, 23 Sep 2024 22:17:43 GMT
ENV _BASH_LATEST_PATCH=37
# Mon, 23 Sep 2024 22:17:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz"; 	wget -O bash.tar.gz.sig "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz.sig"; 		: "${_BASH_BASELINE_PATCH:=0}" "${_BASH_LATEST_PATCH:=0}"; 	if [ "$_BASH_LATEST_PATCH" -gt "$_BASH_BASELINE_PATCH" ]; then 		mkdir -p bash-patches; 		first="$(printf '%03d' "$(( _BASH_BASELINE_PATCH + 1 ))")"; 		last="$(printf '%03d' "$_BASH_LATEST_PATCH")"; 		majorMinor="${_BASH_VERSION%.*}"; 		for patch in $(seq -w "$first" "$last"); do 			url="https://ftp.gnu.org/gnu/bash/bash-$majorMinor-patches/bash${majorMinor//./}-$patch"; 			wget -O "bash-patches/$patch" "$url"; 			wget -O "bash-patches/$patch.sig" "$url.sig"; 		done; 	fi; 		apk add --no-cache --virtual .gpg-deps gnupg; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7C0135FB088AAF6C66C650B9BB5869F064EA74AB; 	gpg --batch --verify bash.tar.gz.sig bash.tar.gz; 	rm bash.tar.gz.sig; 	if [ -d bash-patches ]; then 		for sig in bash-patches/*.sig; do 			p="${sig%.sig}"; 			gpg --batch --verify "$sig" "$p"; 			rm "$sig"; 		done; 	fi; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apk del --no-network .gpg-deps; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	[ "$(bash -c 'echo "${BASH_VERSION%%[^0-9.]*}"')" = "$_BASH_VERSION" ]; 	bash -c 'help' > /dev/null # buildkit
# Mon, 23 Sep 2024 22:17:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Sep 2024 22:17:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Sep 2024 22:17:43 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:b5caf700653f785a3409fb40484075ff91a3a7a84b79ad6a91b165589b35fbc0`  
		Last Modified: Fri, 06 Sep 2024 22:26:38 GMT  
		Size: 3.6 MB (3572419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a47e2e28fe115dc0606c9e3a608f3f30a713cdd71715c77a28142e422945ead5`  
		Last Modified: Tue, 24 Sep 2024 01:07:51 GMT  
		Size: 2.9 MB (2945395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:906c827c528d302ed16b2c36a0ae777f27de2480bd562785cb2a3562f0e5072d`  
		Last Modified: Tue, 24 Sep 2024 01:07:51 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:5-alpine3.20` - unknown; unknown

```console
$ docker pull bash@sha256:208d0314297ebf85103ec332ef6c041d4317e621da45e076726fc15828044028
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.0 KB (129992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9414c097e3d37dc107703424a77634ee1a45f227f3f4afce4a49ecc8a5718df`

```dockerfile
```

-	Layers:
	-	`sha256:1bedb6013f8f2d1dd4e2003bb95ec07fa151b3b1de852e0a5e8e5ec358d9956f`  
		Last Modified: Tue, 24 Sep 2024 01:07:51 GMT  
		Size: 109.1 KB (109135 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:666238fc025dde053ced93a1b77674fe41b06a3d6eaf25751da2cb91108cdac0`  
		Last Modified: Tue, 24 Sep 2024 01:07:50 GMT  
		Size: 20.9 KB (20857 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:5-alpine3.20` - linux; riscv64

```console
$ docker pull bash@sha256:b77ddcef8c3ac7702e0cee4528f9133afa32c316692a2afd3aa65866c99914a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6027399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f41335b5b922db135413042b7cf23a6088626f1371c33c2777e2338296ae8e9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 06 Sep 2024 22:26:03 GMT
ADD file:1f189f0db01ff094ebe1569a5caf278db6965725f4182176ff85dafa711ad524 in / 
# Fri, 06 Sep 2024 22:26:04 GMT
CMD ["/bin/sh"]
# Mon, 23 Sep 2024 22:17:43 GMT
ENV _BASH_VERSION=5.2.37
# Mon, 23 Sep 2024 22:17:43 GMT
ENV _BASH_BASELINE=5.2.37
# Mon, 23 Sep 2024 22:17:43 GMT
ENV _BASH_BASELINE_PATCH=37
# Mon, 23 Sep 2024 22:17:43 GMT
ENV _BASH_LATEST_PATCH=37
# Mon, 23 Sep 2024 22:17:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz"; 	wget -O bash.tar.gz.sig "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz.sig"; 		: "${_BASH_BASELINE_PATCH:=0}" "${_BASH_LATEST_PATCH:=0}"; 	if [ "$_BASH_LATEST_PATCH" -gt "$_BASH_BASELINE_PATCH" ]; then 		mkdir -p bash-patches; 		first="$(printf '%03d' "$(( _BASH_BASELINE_PATCH + 1 ))")"; 		last="$(printf '%03d' "$_BASH_LATEST_PATCH")"; 		majorMinor="${_BASH_VERSION%.*}"; 		for patch in $(seq -w "$first" "$last"); do 			url="https://ftp.gnu.org/gnu/bash/bash-$majorMinor-patches/bash${majorMinor//./}-$patch"; 			wget -O "bash-patches/$patch" "$url"; 			wget -O "bash-patches/$patch.sig" "$url.sig"; 		done; 	fi; 		apk add --no-cache --virtual .gpg-deps gnupg; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7C0135FB088AAF6C66C650B9BB5869F064EA74AB; 	gpg --batch --verify bash.tar.gz.sig bash.tar.gz; 	rm bash.tar.gz.sig; 	if [ -d bash-patches ]; then 		for sig in bash-patches/*.sig; do 			p="${sig%.sig}"; 			gpg --batch --verify "$sig" "$p"; 			rm "$sig"; 		done; 	fi; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apk del --no-network .gpg-deps; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	[ "$(bash -c 'echo "${BASH_VERSION%%[^0-9.]*}"')" = "$_BASH_VERSION" ]; 	bash -c 'help' > /dev/null # buildkit
# Mon, 23 Sep 2024 22:17:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Sep 2024 22:17:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Sep 2024 22:17:43 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:8c4a05189a5fd2cf629c25ab8d0831be7156d74b336f129a412933ee78af018c`  
		Last Modified: Fri, 06 Sep 2024 22:26:21 GMT  
		Size: 3.4 MB (3371452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc386824686b3655634753ca3087d8d92a064636332adb8873c1a1f458f75a4b`  
		Last Modified: Tue, 24 Sep 2024 01:07:13 GMT  
		Size: 2.7 MB (2655606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e20166278699847730691218ac894e301cecd0b8d6cdd717a2da7a51b87bae`  
		Last Modified: Tue, 24 Sep 2024 01:07:13 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:5-alpine3.20` - unknown; unknown

```console
$ docker pull bash@sha256:7cc4717edf1f9b987bb7dc391d3aa4bb6fc112deb088b397cef40b812adeb1fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.0 KB (129988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64fc71b2c8cb5bdfb7ab7eda66e0dc816bcd48ab8dfef381002cf46417309b68`

```dockerfile
```

-	Layers:
	-	`sha256:313041d6c4653c1cb93f87362a63fef8789195ebfdf21273aabff06670493699`  
		Last Modified: Tue, 24 Sep 2024 01:07:13 GMT  
		Size: 109.1 KB (109131 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7319139bc5cac14260669af2b2d41dbf979ac401ba4d98d2a63a3d6b89f719bc`  
		Last Modified: Tue, 24 Sep 2024 01:07:13 GMT  
		Size: 20.9 KB (20857 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:5-alpine3.20` - linux; s390x

```console
$ docker pull bash@sha256:d9ed92bde66fd5871b6cf90a5f84cc0d7430d2ea2960fffb2d980bd89080e01d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6244243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74dd6650e95363945065cb7d9004917b540f0c6d23262460ee3dec50a8e62f04`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 06 Sep 2024 22:48:17 GMT
ADD file:ba2637314e600db5a647501cf1ab287c5f51de1627c13bc1d82aa48925a3dd78 in / 
# Fri, 06 Sep 2024 22:48:17 GMT
CMD ["/bin/sh"]
# Mon, 23 Sep 2024 22:17:43 GMT
ENV _BASH_VERSION=5.2.37
# Mon, 23 Sep 2024 22:17:43 GMT
ENV _BASH_BASELINE=5.2.37
# Mon, 23 Sep 2024 22:17:43 GMT
ENV _BASH_BASELINE_PATCH=37
# Mon, 23 Sep 2024 22:17:43 GMT
ENV _BASH_LATEST_PATCH=37
# Mon, 23 Sep 2024 22:17:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz"; 	wget -O bash.tar.gz.sig "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz.sig"; 		: "${_BASH_BASELINE_PATCH:=0}" "${_BASH_LATEST_PATCH:=0}"; 	if [ "$_BASH_LATEST_PATCH" -gt "$_BASH_BASELINE_PATCH" ]; then 		mkdir -p bash-patches; 		first="$(printf '%03d' "$(( _BASH_BASELINE_PATCH + 1 ))")"; 		last="$(printf '%03d' "$_BASH_LATEST_PATCH")"; 		majorMinor="${_BASH_VERSION%.*}"; 		for patch in $(seq -w "$first" "$last"); do 			url="https://ftp.gnu.org/gnu/bash/bash-$majorMinor-patches/bash${majorMinor//./}-$patch"; 			wget -O "bash-patches/$patch" "$url"; 			wget -O "bash-patches/$patch.sig" "$url.sig"; 		done; 	fi; 		apk add --no-cache --virtual .gpg-deps gnupg; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7C0135FB088AAF6C66C650B9BB5869F064EA74AB; 	gpg --batch --verify bash.tar.gz.sig bash.tar.gz; 	rm bash.tar.gz.sig; 	if [ -d bash-patches ]; then 		for sig in bash-patches/*.sig; do 			p="${sig%.sig}"; 			gpg --batch --verify "$sig" "$p"; 			rm "$sig"; 		done; 	fi; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apk del --no-network .gpg-deps; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	[ "$(bash -c 'echo "${BASH_VERSION%%[^0-9.]*}"')" = "$_BASH_VERSION" ]; 	bash -c 'help' > /dev/null # buildkit
# Mon, 23 Sep 2024 22:17:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Sep 2024 22:17:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Sep 2024 22:17:43 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:df110db6acd600b9ee5ebd7b510779652f96424d3f80321a4e0dcb8a09aa0526`  
		Last Modified: Fri, 06 Sep 2024 22:48:57 GMT  
		Size: 3.5 MB (3461598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1fc95cd71502ee428afef78fd522b6f1578d4a1424915959a2f29e1149fa713`  
		Last Modified: Tue, 24 Sep 2024 01:14:25 GMT  
		Size: 2.8 MB (2782312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93d068642614f26fda07ebd4369ffb5138cdf9e9c2287c2f7fd0f784191ce883`  
		Last Modified: Tue, 24 Sep 2024 01:14:25 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:5-alpine3.20` - unknown; unknown

```console
$ docker pull bash@sha256:3311c15e2f66ebed0f3998418ca3c7c0ee2ba731ef8b947dde2517c04098a22a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.9 KB (129871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27df58ae07d8187c5c72dc9a9276ec13bad3c1eb74e5c8a4bbf43932a9255453`

```dockerfile
```

-	Layers:
	-	`sha256:21a22c78b12ffbbb71b85ee1bdc13cb3cfc525252d5fafce3a2f29c8c40de051`  
		Last Modified: Tue, 24 Sep 2024 01:14:25 GMT  
		Size: 109.1 KB (109077 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a18f78ae3ac0b420e0e11a39bc661db8d4997049e58c14b7531d0d65e1f311a7`  
		Last Modified: Tue, 24 Sep 2024 01:14:25 GMT  
		Size: 20.8 KB (20794 bytes)  
		MIME: application/vnd.in-toto+json
