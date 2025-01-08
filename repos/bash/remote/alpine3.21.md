## `bash:alpine3.21`

```console
$ docker pull bash@sha256:92f26366328a7169e663be0d85e249c820ba5d438910b8f7c8fce7f12055cda7
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

### `bash:alpine3.21` - linux; amd64

```console
$ docker pull bash@sha256:70a51767233c4d0bc3bdc927c94b948b1ba1e62a9ffa5b03dca6e75b63b09aff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6353773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dbe0988136abc10523ec8f49b16a74696ff64210ceaa2d38e7adbdc76198318`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Dec 2024 18:52:02 GMT
ADD alpine-minirootfs-3.21.1-x86_64.tar.gz / # buildkit
# Tue, 10 Dec 2024 18:52:02 GMT
CMD ["/bin/sh"]
# Tue, 10 Dec 2024 18:52:02 GMT
ENV _BASH_VERSION=5.2.37
# Tue, 10 Dec 2024 18:52:02 GMT
ENV _BASH_BASELINE=5.2.37
# Tue, 10 Dec 2024 18:52:02 GMT
ENV _BASH_BASELINE_PATCH=37
# Tue, 10 Dec 2024 18:52:02 GMT
ENV _BASH_LATEST_PATCH=37
# Tue, 10 Dec 2024 18:52:02 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz"; 	wget -O bash.tar.gz.sig "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz.sig"; 		: "${_BASH_BASELINE_PATCH:=0}" "${_BASH_LATEST_PATCH:=0}"; 	if [ "$_BASH_LATEST_PATCH" -gt "$_BASH_BASELINE_PATCH" ]; then 		mkdir -p bash-patches; 		first="$(printf '%03d' "$(( _BASH_BASELINE_PATCH + 1 ))")"; 		last="$(printf '%03d' "$_BASH_LATEST_PATCH")"; 		majorMinor="${_BASH_VERSION%.*}"; 		for patch in $(seq -w "$first" "$last"); do 			url="https://ftp.gnu.org/gnu/bash/bash-$majorMinor-patches/bash${majorMinor//./}-$patch"; 			wget -O "bash-patches/$patch" "$url"; 			wget -O "bash-patches/$patch.sig" "$url.sig"; 		done; 	fi; 		apk add --no-cache --virtual .gpg-deps gnupg; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7C0135FB088AAF6C66C650B9BB5869F064EA74AB; 	gpg --batch --verify bash.tar.gz.sig bash.tar.gz; 	rm bash.tar.gz.sig; 	if [ -d bash-patches ]; then 		for sig in bash-patches/*.sig; do 			p="${sig%.sig}"; 			gpg --batch --verify "$sig" "$p"; 			rm "$sig"; 		done; 	fi; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apk del --no-network .gpg-deps; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	[ "$(bash -c 'echo "${BASH_VERSION%%[^0-9.]*}"')" = "$_BASH_VERSION" ]; 	bash -c 'help' > /dev/null # buildkit
# Tue, 10 Dec 2024 18:52:02 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 10 Dec 2024 18:52:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Dec 2024 18:52:02 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:245043d9199c263f869fc0558f43f7cb98bbc92acdd5def1b4f690adc0ac7807`  
		Last Modified: Mon, 06 Jan 2025 21:44:42 GMT  
		Size: 3.6 MB (3636222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:817695395e501a798e5e91a8d0c88e212bec1215bcda313cb7a3435664b0698b`  
		Last Modified: Tue, 07 Jan 2025 03:14:45 GMT  
		Size: 2.7 MB (2717214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:040b85d53ca02a3ca5c294e4fd910ed4a742a4f7687439420504a5fe998dc84c`  
		Last Modified: Tue, 07 Jan 2025 03:14:45 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:alpine3.21` - unknown; unknown

```console
$ docker pull bash@sha256:e385d73380499e8656339c634d92b93911755abbbfb505396224f4156e0d4613
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.2 KB (137173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3b54088006edbf28c8c83f964677a519fe01e297b3bdb0c8fd06ac56666168a`

```dockerfile
```

-	Layers:
	-	`sha256:15f56dba0cb6d8c3462b0b36ffcb78bc4b07afb72a76c86f596fe3b9b7b7cf3b`  
		Last Modified: Tue, 07 Jan 2025 03:14:45 GMT  
		Size: 116.1 KB (116070 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d825a2019eef11432beb4b4edcbb86f0dd9638399f1d1bb8e3d0bda26fe1ffb`  
		Last Modified: Tue, 07 Jan 2025 03:14:45 GMT  
		Size: 21.1 KB (21103 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:alpine3.21` - linux; arm variant v6

```console
$ docker pull bash@sha256:e7d326f5f582cd2299d4c537d00de0dc4cb8f65c4363961691c8b10b347067da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6022296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:689756b0a8d8222af8ddedcb9a993637bffa622144b4105772dab70cadb33d26`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Dec 2024 18:52:02 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
# Tue, 10 Dec 2024 18:52:02 GMT
CMD ["/bin/sh"]
# Tue, 10 Dec 2024 18:52:02 GMT
ENV _BASH_VERSION=5.2.37
# Tue, 10 Dec 2024 18:52:02 GMT
ENV _BASH_BASELINE=5.2.37
# Tue, 10 Dec 2024 18:52:02 GMT
ENV _BASH_BASELINE_PATCH=37
# Tue, 10 Dec 2024 18:52:02 GMT
ENV _BASH_LATEST_PATCH=37
# Tue, 10 Dec 2024 18:52:02 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz"; 	wget -O bash.tar.gz.sig "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz.sig"; 		: "${_BASH_BASELINE_PATCH:=0}" "${_BASH_LATEST_PATCH:=0}"; 	if [ "$_BASH_LATEST_PATCH" -gt "$_BASH_BASELINE_PATCH" ]; then 		mkdir -p bash-patches; 		first="$(printf '%03d' "$(( _BASH_BASELINE_PATCH + 1 ))")"; 		last="$(printf '%03d' "$_BASH_LATEST_PATCH")"; 		majorMinor="${_BASH_VERSION%.*}"; 		for patch in $(seq -w "$first" "$last"); do 			url="https://ftp.gnu.org/gnu/bash/bash-$majorMinor-patches/bash${majorMinor//./}-$patch"; 			wget -O "bash-patches/$patch" "$url"; 			wget -O "bash-patches/$patch.sig" "$url.sig"; 		done; 	fi; 		apk add --no-cache --virtual .gpg-deps gnupg; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7C0135FB088AAF6C66C650B9BB5869F064EA74AB; 	gpg --batch --verify bash.tar.gz.sig bash.tar.gz; 	rm bash.tar.gz.sig; 	if [ -d bash-patches ]; then 		for sig in bash-patches/*.sig; do 			p="${sig%.sig}"; 			gpg --batch --verify "$sig" "$p"; 			rm "$sig"; 		done; 	fi; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apk del --no-network .gpg-deps; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	[ "$(bash -c 'echo "${BASH_VERSION%%[^0-9.]*}"')" = "$_BASH_VERSION" ]; 	bash -c 'help' > /dev/null # buildkit
# Tue, 10 Dec 2024 18:52:02 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 10 Dec 2024 18:52:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Dec 2024 18:52:02 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:d3e229a4bb72770bd404e0f6590519a8e566146523e984834c6a3d82836f0069`  
		Last Modified: Wed, 08 Jan 2025 17:23:44 GMT  
		Size: 3.4 MB (3363879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cde701765f0a46657f3f8331e37b630d778512b191a948e989a4c26fac28480b`  
		Last Modified: Wed, 08 Jan 2025 18:09:16 GMT  
		Size: 2.7 MB (2658081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8aa03129a2195c0f5bffa0b028ef6a7b5a4982f36879b2723ece02f412fec82`  
		Last Modified: Wed, 08 Jan 2025 18:09:16 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:alpine3.21` - unknown; unknown

```console
$ docker pull bash@sha256:b3255ce780af2e2fdc0d7fef6032286597aebd82770160c1300a244d56f50727
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.0 KB (20997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99d7f860f608341ea52f7f2bf2f87c038f816ddaf7a9a35ac96eb6d4dcf83ae1`

```dockerfile
```

-	Layers:
	-	`sha256:32b12c2ac95be253e84869fb12bf4c0dc57005d57828ca315fa1d7ff7a0bfa4f`  
		Last Modified: Wed, 08 Jan 2025 18:09:16 GMT  
		Size: 21.0 KB (20997 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:alpine3.21` - linux; arm variant v7

```console
$ docker pull bash@sha256:a5d5cdd58fcee038e9ec0bd6b7df9d7db62aac8b125209c96189518b00319ea5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5703270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ee31c78f43b16c853e8ec660089b328f8049fa6ac524d0840473a932c7c52fd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Dec 2024 18:52:02 GMT
ADD alpine-minirootfs-3.21.1-armv7.tar.gz / # buildkit
# Tue, 10 Dec 2024 18:52:02 GMT
CMD ["/bin/sh"]
# Tue, 10 Dec 2024 18:52:02 GMT
ENV _BASH_VERSION=5.2.37
# Tue, 10 Dec 2024 18:52:02 GMT
ENV _BASH_BASELINE=5.2.37
# Tue, 10 Dec 2024 18:52:02 GMT
ENV _BASH_BASELINE_PATCH=37
# Tue, 10 Dec 2024 18:52:02 GMT
ENV _BASH_LATEST_PATCH=37
# Tue, 10 Dec 2024 18:52:02 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz"; 	wget -O bash.tar.gz.sig "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz.sig"; 		: "${_BASH_BASELINE_PATCH:=0}" "${_BASH_LATEST_PATCH:=0}"; 	if [ "$_BASH_LATEST_PATCH" -gt "$_BASH_BASELINE_PATCH" ]; then 		mkdir -p bash-patches; 		first="$(printf '%03d' "$(( _BASH_BASELINE_PATCH + 1 ))")"; 		last="$(printf '%03d' "$_BASH_LATEST_PATCH")"; 		majorMinor="${_BASH_VERSION%.*}"; 		for patch in $(seq -w "$first" "$last"); do 			url="https://ftp.gnu.org/gnu/bash/bash-$majorMinor-patches/bash${majorMinor//./}-$patch"; 			wget -O "bash-patches/$patch" "$url"; 			wget -O "bash-patches/$patch.sig" "$url.sig"; 		done; 	fi; 		apk add --no-cache --virtual .gpg-deps gnupg; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7C0135FB088AAF6C66C650B9BB5869F064EA74AB; 	gpg --batch --verify bash.tar.gz.sig bash.tar.gz; 	rm bash.tar.gz.sig; 	if [ -d bash-patches ]; then 		for sig in bash-patches/*.sig; do 			p="${sig%.sig}"; 			gpg --batch --verify "$sig" "$p"; 			rm "$sig"; 		done; 	fi; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apk del --no-network .gpg-deps; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	[ "$(bash -c 'echo "${BASH_VERSION%%[^0-9.]*}"')" = "$_BASH_VERSION" ]; 	bash -c 'help' > /dev/null # buildkit
# Tue, 10 Dec 2024 18:52:02 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 10 Dec 2024 18:52:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Dec 2024 18:52:02 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:fa398bd1707194d783a6221bb60ba630f074222cdc0f4b6a05d9167d6e9c4a9f`  
		Last Modified: Tue, 07 Jan 2025 02:55:27 GMT  
		Size: 3.1 MB (3093241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac2890d58fd279eb7b4ef9f9852ada87a2991b0d6946c8699e0da00f371e5098`  
		Last Modified: Tue, 07 Jan 2025 03:23:27 GMT  
		Size: 2.6 MB (2609697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9098cbc7983cb1ed20ec2e6e2e633c4fd8a7fb3b37a00443f880688a459901e5`  
		Last Modified: Tue, 07 Jan 2025 03:23:27 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:alpine3.21` - unknown; unknown

```console
$ docker pull bash@sha256:174ea42fb3a1d702a39f48809a76dbd5a0cff5c1171ec57264612629459e76e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.3 KB (137349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cff176f0cdc1eca9aeff2cd41478e7c5f322510cbbba1cab65cefadff7333eb3`

```dockerfile
```

-	Layers:
	-	`sha256:ac4be591a752e7bd87fcd4b4b8f12be0ab5969a428c57efcbf649464c9dbc6fb`  
		Last Modified: Tue, 07 Jan 2025 03:23:27 GMT  
		Size: 116.1 KB (116138 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d20f1a22eb39b1309c98112f0d8206a5d7b501f3af8ee0726b4092cb49eb99d`  
		Last Modified: Tue, 07 Jan 2025 03:23:26 GMT  
		Size: 21.2 KB (21211 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:alpine3.21` - linux; arm64 variant v8

```console
$ docker pull bash@sha256:960255df660deadd963830492cdbee1eceb2f1bb1728a01a935d218042d4d38a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6777134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:698a8eea55510f3604ba4b18432c34c050d609a0ee67477a315331910b0c9549`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Dec 2024 18:52:02 GMT
ADD alpine-minirootfs-3.21.1-aarch64.tar.gz / # buildkit
# Tue, 10 Dec 2024 18:52:02 GMT
CMD ["/bin/sh"]
# Tue, 10 Dec 2024 18:52:02 GMT
ENV _BASH_VERSION=5.2.37
# Tue, 10 Dec 2024 18:52:02 GMT
ENV _BASH_BASELINE=5.2.37
# Tue, 10 Dec 2024 18:52:02 GMT
ENV _BASH_BASELINE_PATCH=37
# Tue, 10 Dec 2024 18:52:02 GMT
ENV _BASH_LATEST_PATCH=37
# Tue, 10 Dec 2024 18:52:02 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz"; 	wget -O bash.tar.gz.sig "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz.sig"; 		: "${_BASH_BASELINE_PATCH:=0}" "${_BASH_LATEST_PATCH:=0}"; 	if [ "$_BASH_LATEST_PATCH" -gt "$_BASH_BASELINE_PATCH" ]; then 		mkdir -p bash-patches; 		first="$(printf '%03d' "$(( _BASH_BASELINE_PATCH + 1 ))")"; 		last="$(printf '%03d' "$_BASH_LATEST_PATCH")"; 		majorMinor="${_BASH_VERSION%.*}"; 		for patch in $(seq -w "$first" "$last"); do 			url="https://ftp.gnu.org/gnu/bash/bash-$majorMinor-patches/bash${majorMinor//./}-$patch"; 			wget -O "bash-patches/$patch" "$url"; 			wget -O "bash-patches/$patch.sig" "$url.sig"; 		done; 	fi; 		apk add --no-cache --virtual .gpg-deps gnupg; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7C0135FB088AAF6C66C650B9BB5869F064EA74AB; 	gpg --batch --verify bash.tar.gz.sig bash.tar.gz; 	rm bash.tar.gz.sig; 	if [ -d bash-patches ]; then 		for sig in bash-patches/*.sig; do 			p="${sig%.sig}"; 			gpg --batch --verify "$sig" "$p"; 			rm "$sig"; 		done; 	fi; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apk del --no-network .gpg-deps; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	[ "$(bash -c 'echo "${BASH_VERSION%%[^0-9.]*}"')" = "$_BASH_VERSION" ]; 	bash -c 'help' > /dev/null # buildkit
# Tue, 10 Dec 2024 18:52:02 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 10 Dec 2024 18:52:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Dec 2024 18:52:02 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:707c94c90c597447ce10a36c9b56355c1cc67d0cf593a592daeb419d99a30d85`  
		Last Modified: Tue, 07 Jan 2025 03:02:50 GMT  
		Size: 4.0 MB (3983007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5c230e726cb923e770c0bd0451ba2411d1c477ed8fffd0377ede41a36517e40`  
		Last Modified: Tue, 07 Jan 2025 03:47:17 GMT  
		Size: 2.8 MB (2793794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4503cecc056f0714933c22bed0f0d936e34b0c4c0bdd99c960bc10be48476a03`  
		Last Modified: Tue, 07 Jan 2025 03:47:16 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:alpine3.21` - unknown; unknown

```console
$ docker pull bash@sha256:c1c5b6f56360402af4d4bcadbdd1a17e19ccd8048b58d4f2ff2b43c6429377f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.4 KB (137430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49b6289e8d871fb1f0c8f597c5c0160f9721fbff69e5fe0d8ccf48f4bbbb02b3`

```dockerfile
```

-	Layers:
	-	`sha256:2142833f1d95cd8b1da453ef41b5b96703d39a29bbb193f3f79a525b8731b775`  
		Last Modified: Tue, 07 Jan 2025 03:47:17 GMT  
		Size: 116.2 KB (116174 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b16160a12a4449f587dd618c15253dd1696e6ba5cd4b0fbf06b4ab818b36b70`  
		Last Modified: Tue, 07 Jan 2025 03:47:16 GMT  
		Size: 21.3 KB (21256 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:alpine3.21` - linux; 386

```console
$ docker pull bash@sha256:9677489bed84a83729b368b5968d669e2ad10b9048e5c0c1099873ebf520df50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6122579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f05f119fa2a74da62e1a48bf1c48fc737c638453aa647948808f284de60d1c6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Dec 2024 18:52:02 GMT
ADD alpine-minirootfs-3.21.2-x86.tar.gz / # buildkit
# Tue, 10 Dec 2024 18:52:02 GMT
CMD ["/bin/sh"]
# Tue, 10 Dec 2024 18:52:02 GMT
ENV _BASH_VERSION=5.2.37
# Tue, 10 Dec 2024 18:52:02 GMT
ENV _BASH_BASELINE=5.2.37
# Tue, 10 Dec 2024 18:52:02 GMT
ENV _BASH_BASELINE_PATCH=37
# Tue, 10 Dec 2024 18:52:02 GMT
ENV _BASH_LATEST_PATCH=37
# Tue, 10 Dec 2024 18:52:02 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz"; 	wget -O bash.tar.gz.sig "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz.sig"; 		: "${_BASH_BASELINE_PATCH:=0}" "${_BASH_LATEST_PATCH:=0}"; 	if [ "$_BASH_LATEST_PATCH" -gt "$_BASH_BASELINE_PATCH" ]; then 		mkdir -p bash-patches; 		first="$(printf '%03d' "$(( _BASH_BASELINE_PATCH + 1 ))")"; 		last="$(printf '%03d' "$_BASH_LATEST_PATCH")"; 		majorMinor="${_BASH_VERSION%.*}"; 		for patch in $(seq -w "$first" "$last"); do 			url="https://ftp.gnu.org/gnu/bash/bash-$majorMinor-patches/bash${majorMinor//./}-$patch"; 			wget -O "bash-patches/$patch" "$url"; 			wget -O "bash-patches/$patch.sig" "$url.sig"; 		done; 	fi; 		apk add --no-cache --virtual .gpg-deps gnupg; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7C0135FB088AAF6C66C650B9BB5869F064EA74AB; 	gpg --batch --verify bash.tar.gz.sig bash.tar.gz; 	rm bash.tar.gz.sig; 	if [ -d bash-patches ]; then 		for sig in bash-patches/*.sig; do 			p="${sig%.sig}"; 			gpg --batch --verify "$sig" "$p"; 			rm "$sig"; 		done; 	fi; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apk del --no-network .gpg-deps; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	[ "$(bash -c 'echo "${BASH_VERSION%%[^0-9.]*}"')" = "$_BASH_VERSION" ]; 	bash -c 'help' > /dev/null # buildkit
# Tue, 10 Dec 2024 18:52:02 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 10 Dec 2024 18:52:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Dec 2024 18:52:02 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:dbaac2331104495e5df0818a1db05c402cfc13af140c75beccf51922d5f37ad5`  
		Last Modified: Wed, 08 Jan 2025 17:23:36 GMT  
		Size: 3.5 MB (3463126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02dab8b0401c2207c95437630a62e553832f36e86545adca44e906cce97a84a8`  
		Last Modified: Wed, 08 Jan 2025 17:58:36 GMT  
		Size: 2.7 MB (2659119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8031c7daac3958359624062cd953693943ecca5edf96efd573364083a734c96`  
		Last Modified: Wed, 08 Jan 2025 17:58:35 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:alpine3.21` - unknown; unknown

```console
$ docker pull bash@sha256:b7e2b1555c4df561e342f0ce4412eac7415541303607cf0d83d73302bba97987
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.1 KB (137077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a554f0b8a2d1fdc8bf66c7bea733f07d917d2d8963d2638f5f281e53688f644e`

```dockerfile
```

-	Layers:
	-	`sha256:72ccc740a0b288ebe1e4889dfc28e3541492e34f0b15b3f0a3c0969d9477020d`  
		Last Modified: Wed, 08 Jan 2025 17:58:35 GMT  
		Size: 116.0 KB (116025 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7897253ebd1c584f36582d3e758224bf72a76e8cf43357ca0b4147354de47a4`  
		Last Modified: Wed, 08 Jan 2025 17:58:35 GMT  
		Size: 21.1 KB (21052 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:alpine3.21` - linux; ppc64le

```console
$ docker pull bash@sha256:22a8505099760d26934b5fe6e8af6889d97984e6e18719a41bea020818b44543
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6539115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bf8e3790545920f33acb412ed28a17b942819874883984536bcc7d26c9f0aac`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Dec 2024 18:52:02 GMT
ADD alpine-minirootfs-3.21.2-ppc64le.tar.gz / # buildkit
# Tue, 10 Dec 2024 18:52:02 GMT
CMD ["/bin/sh"]
# Tue, 10 Dec 2024 18:52:02 GMT
ENV _BASH_VERSION=5.2.37
# Tue, 10 Dec 2024 18:52:02 GMT
ENV _BASH_BASELINE=5.2.37
# Tue, 10 Dec 2024 18:52:02 GMT
ENV _BASH_BASELINE_PATCH=37
# Tue, 10 Dec 2024 18:52:02 GMT
ENV _BASH_LATEST_PATCH=37
# Tue, 10 Dec 2024 18:52:02 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz"; 	wget -O bash.tar.gz.sig "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz.sig"; 		: "${_BASH_BASELINE_PATCH:=0}" "${_BASH_LATEST_PATCH:=0}"; 	if [ "$_BASH_LATEST_PATCH" -gt "$_BASH_BASELINE_PATCH" ]; then 		mkdir -p bash-patches; 		first="$(printf '%03d' "$(( _BASH_BASELINE_PATCH + 1 ))")"; 		last="$(printf '%03d' "$_BASH_LATEST_PATCH")"; 		majorMinor="${_BASH_VERSION%.*}"; 		for patch in $(seq -w "$first" "$last"); do 			url="https://ftp.gnu.org/gnu/bash/bash-$majorMinor-patches/bash${majorMinor//./}-$patch"; 			wget -O "bash-patches/$patch" "$url"; 			wget -O "bash-patches/$patch.sig" "$url.sig"; 		done; 	fi; 		apk add --no-cache --virtual .gpg-deps gnupg; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7C0135FB088AAF6C66C650B9BB5869F064EA74AB; 	gpg --batch --verify bash.tar.gz.sig bash.tar.gz; 	rm bash.tar.gz.sig; 	if [ -d bash-patches ]; then 		for sig in bash-patches/*.sig; do 			p="${sig%.sig}"; 			gpg --batch --verify "$sig" "$p"; 			rm "$sig"; 		done; 	fi; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apk del --no-network .gpg-deps; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	[ "$(bash -c 'echo "${BASH_VERSION%%[^0-9.]*}"')" = "$_BASH_VERSION" ]; 	bash -c 'help' > /dev/null # buildkit
# Tue, 10 Dec 2024 18:52:02 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 10 Dec 2024 18:52:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Dec 2024 18:52:02 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:244ac55e5ecd413dee99efe3ace7cb84420bfc9a727ec2327dae7805045d7470`  
		Last Modified: Wed, 08 Jan 2025 17:24:16 GMT  
		Size: 3.6 MB (3573601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9f854a6c210153f6ec500a80031ef60f3117c9a13465995f1f78b303500ac31`  
		Last Modified: Wed, 08 Jan 2025 18:01:19 GMT  
		Size: 3.0 MB (2965177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb555bd3832f084d57b802c83c1db31a3544e3f49eb0a53174a4d7f95bb357d8`  
		Last Modified: Wed, 08 Jan 2025 18:01:19 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:alpine3.21` - unknown; unknown

```console
$ docker pull bash@sha256:2db87fe4ff384a31c431d3893e92b69c4beb8274594892e456763d4a5ff24a83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.3 KB (135349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51e078c875019324b3516d05c0a37bff1df1d58eeaf427085978985b839243d7`

```dockerfile
```

-	Layers:
	-	`sha256:508e1ea9fcfd68dd1aa289f9adaf21c55daec1ba39fac8f162a1ee9a743e0fc3`  
		Last Modified: Wed, 08 Jan 2025 18:01:19 GMT  
		Size: 114.2 KB (114177 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67a891b5dba430ccd79387cee96f46706a0c3b7a0e45525026286a78d7e13d91`  
		Last Modified: Wed, 08 Jan 2025 18:01:19 GMT  
		Size: 21.2 KB (21172 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:alpine3.21` - linux; riscv64

```console
$ docker pull bash@sha256:cc34d20e699180e3e82ed4fe3e1279b398922ff9f5b215b79210ed6750706fa5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6019026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bc9e70636b9bed67f90174ae152155f8c4098b5c4cb9b450ccb7c7cd53bf668`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Dec 2024 18:52:02 GMT
ADD alpine-minirootfs-3.21.1-riscv64.tar.gz / # buildkit
# Tue, 10 Dec 2024 18:52:02 GMT
CMD ["/bin/sh"]
# Tue, 10 Dec 2024 18:52:02 GMT
ENV _BASH_VERSION=5.2.37
# Tue, 10 Dec 2024 18:52:02 GMT
ENV _BASH_BASELINE=5.2.37
# Tue, 10 Dec 2024 18:52:02 GMT
ENV _BASH_BASELINE_PATCH=37
# Tue, 10 Dec 2024 18:52:02 GMT
ENV _BASH_LATEST_PATCH=37
# Tue, 10 Dec 2024 18:52:02 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz"; 	wget -O bash.tar.gz.sig "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz.sig"; 		: "${_BASH_BASELINE_PATCH:=0}" "${_BASH_LATEST_PATCH:=0}"; 	if [ "$_BASH_LATEST_PATCH" -gt "$_BASH_BASELINE_PATCH" ]; then 		mkdir -p bash-patches; 		first="$(printf '%03d' "$(( _BASH_BASELINE_PATCH + 1 ))")"; 		last="$(printf '%03d' "$_BASH_LATEST_PATCH")"; 		majorMinor="${_BASH_VERSION%.*}"; 		for patch in $(seq -w "$first" "$last"); do 			url="https://ftp.gnu.org/gnu/bash/bash-$majorMinor-patches/bash${majorMinor//./}-$patch"; 			wget -O "bash-patches/$patch" "$url"; 			wget -O "bash-patches/$patch.sig" "$url.sig"; 		done; 	fi; 		apk add --no-cache --virtual .gpg-deps gnupg; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7C0135FB088AAF6C66C650B9BB5869F064EA74AB; 	gpg --batch --verify bash.tar.gz.sig bash.tar.gz; 	rm bash.tar.gz.sig; 	if [ -d bash-patches ]; then 		for sig in bash-patches/*.sig; do 			p="${sig%.sig}"; 			gpg --batch --verify "$sig" "$p"; 			rm "$sig"; 		done; 	fi; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apk del --no-network .gpg-deps; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	[ "$(bash -c 'echo "${BASH_VERSION%%[^0-9.]*}"')" = "$_BASH_VERSION" ]; 	bash -c 'help' > /dev/null # buildkit
# Tue, 10 Dec 2024 18:52:02 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 10 Dec 2024 18:52:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Dec 2024 18:52:02 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:7ac47ecf3caf977bc5a9f6efe0249994a504165670ebb9b6fe2c478617c5482f`  
		Last Modified: Tue, 07 Jan 2025 02:32:47 GMT  
		Size: 3.3 MB (3345140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22d808c748614bdadbac5ab53c73cf7d9da447004b7c198d49ad6e593e85fbcd`  
		Last Modified: Tue, 07 Jan 2025 03:40:12 GMT  
		Size: 2.7 MB (2673548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca90933ace6be135c21d2b251d9868d80b9ddb3279a6b472e27778fd1f24205`  
		Last Modified: Tue, 07 Jan 2025 03:40:11 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:alpine3.21` - unknown; unknown

```console
$ docker pull bash@sha256:06a7df20e89529796fb49a200bba5f971d143911dc648f7991a311b19dc4d47b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.3 KB (135345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a1661e69868b31ea76296be1725889c37ca440bea67f0f6460b57aa4d0aa546`

```dockerfile
```

-	Layers:
	-	`sha256:8d8f8aad3f39cd0cacb0fcdc287fc26860f5a5ca3136c61dde59d6073a4779e3`  
		Last Modified: Tue, 07 Jan 2025 03:40:11 GMT  
		Size: 114.2 KB (114173 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bbf3e5aef37476b47280ccb455b9380aa08955ed11cc8c94aebdac53e5cc3d42`  
		Last Modified: Tue, 07 Jan 2025 03:40:11 GMT  
		Size: 21.2 KB (21172 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:alpine3.21` - linux; s390x

```console
$ docker pull bash@sha256:f70bb0dba1e74df2fbbc70f5b0737bda079ffd4f0ac754f81c2836971eec3b1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6269765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8b1ee01e15d7c52e21f2846f69c9eeaca4d2a051cabd3a900737fd1e3889cb4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Dec 2024 18:52:02 GMT
ADD alpine-minirootfs-3.21.2-s390x.tar.gz / # buildkit
# Tue, 10 Dec 2024 18:52:02 GMT
CMD ["/bin/sh"]
# Tue, 10 Dec 2024 18:52:02 GMT
ENV _BASH_VERSION=5.2.37
# Tue, 10 Dec 2024 18:52:02 GMT
ENV _BASH_BASELINE=5.2.37
# Tue, 10 Dec 2024 18:52:02 GMT
ENV _BASH_BASELINE_PATCH=37
# Tue, 10 Dec 2024 18:52:02 GMT
ENV _BASH_LATEST_PATCH=37
# Tue, 10 Dec 2024 18:52:02 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz"; 	wget -O bash.tar.gz.sig "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz.sig"; 		: "${_BASH_BASELINE_PATCH:=0}" "${_BASH_LATEST_PATCH:=0}"; 	if [ "$_BASH_LATEST_PATCH" -gt "$_BASH_BASELINE_PATCH" ]; then 		mkdir -p bash-patches; 		first="$(printf '%03d' "$(( _BASH_BASELINE_PATCH + 1 ))")"; 		last="$(printf '%03d' "$_BASH_LATEST_PATCH")"; 		majorMinor="${_BASH_VERSION%.*}"; 		for patch in $(seq -w "$first" "$last"); do 			url="https://ftp.gnu.org/gnu/bash/bash-$majorMinor-patches/bash${majorMinor//./}-$patch"; 			wget -O "bash-patches/$patch" "$url"; 			wget -O "bash-patches/$patch.sig" "$url.sig"; 		done; 	fi; 		apk add --no-cache --virtual .gpg-deps gnupg; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7C0135FB088AAF6C66C650B9BB5869F064EA74AB; 	gpg --batch --verify bash.tar.gz.sig bash.tar.gz; 	rm bash.tar.gz.sig; 	if [ -d bash-patches ]; then 		for sig in bash-patches/*.sig; do 			p="${sig%.sig}"; 			gpg --batch --verify "$sig" "$p"; 			rm "$sig"; 		done; 	fi; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apk del --no-network .gpg-deps; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	[ "$(bash -c 'echo "${BASH_VERSION%%[^0-9.]*}"')" = "$_BASH_VERSION" ]; 	bash -c 'help' > /dev/null # buildkit
# Tue, 10 Dec 2024 18:52:02 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 10 Dec 2024 18:52:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Dec 2024 18:52:02 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:b2af93686f9384c40cfe861d7173877bb2ee1675c3ee70181799693c34c8722f`  
		Last Modified: Wed, 08 Jan 2025 17:25:12 GMT  
		Size: 3.5 MB (3466867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:684639c8eef1c46f332047c32df3d007bb5e481d8022fbcdb00347f01cccb379`  
		Last Modified: Wed, 08 Jan 2025 18:00:30 GMT  
		Size: 2.8 MB (2802566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0451949a9988eed80cadd70dc5358384d22de34152f61e5e4112a45d7ce47cb9`  
		Last Modified: Wed, 08 Jan 2025 18:00:30 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:alpine3.21` - unknown; unknown

```console
$ docker pull bash@sha256:a049141b42ff16e6f834cddd678f87203ed4d549aaf7788379e72f038eec7feb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.2 KB (135222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c705958952b826e54ec69254df6c5573a0b85598cc9d9ddca47f1d6484f8945`

```dockerfile
```

-	Layers:
	-	`sha256:7de45f9e2548c0384db6d07b8ef15d55df29dab722b0a267b63377ccb36c3db2`  
		Last Modified: Wed, 08 Jan 2025 18:00:30 GMT  
		Size: 114.1 KB (114119 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1affc07fac33af84686c8062e740c3eada62cfce6c69857f16ae85bd44776c98`  
		Last Modified: Wed, 08 Jan 2025 18:00:30 GMT  
		Size: 21.1 KB (21103 bytes)  
		MIME: application/vnd.in-toto+json
