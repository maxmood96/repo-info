## `bash:4-alpine3.22`

```console
$ docker pull bash@sha256:98e3e261543129cb58ae11723d39b9866c15034bea0d2fb5655da7f502b75051
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

### `bash:4-alpine3.22` - linux; amd64

```console
$ docker pull bash@sha256:12e3da2d13a37aadfe7a28cc0e7ceabe95e96c067ae12ae7aa08eacd1a55b35b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4875069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac538afdaee77d5c575a5626861042d2dfb7c152cb2c2e8760518c1016a8ee1b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 18:45:01 GMT
ENV _BASH_VERSION=4.4.23
# Fri, 30 May 2025 18:45:01 GMT
ENV _BASH_BASELINE=4.4.18
# Fri, 30 May 2025 18:45:01 GMT
ENV _BASH_BASELINE_PATCH=18
# Fri, 30 May 2025 18:45:01 GMT
ENV _BASH_LATEST_PATCH=23
# Fri, 30 May 2025 18:45:01 GMT
COPY alpine3.21.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Fri, 30 May 2025 18:45:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz"; 	wget -O bash.tar.gz.sig "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz.sig"; 		: "${_BASH_BASELINE_PATCH:=0}" "${_BASH_LATEST_PATCH:=0}"; 	if [ "$_BASH_LATEST_PATCH" -gt "$_BASH_BASELINE_PATCH" ]; then 		mkdir -p bash-patches; 		first="$(printf '%03d' "$(( _BASH_BASELINE_PATCH + 1 ))")"; 		last="$(printf '%03d' "$_BASH_LATEST_PATCH")"; 		majorMinor="${_BASH_VERSION%.*}"; 		for patch in $(seq -w "$first" "$last"); do 			url="https://ftp.gnu.org/gnu/bash/bash-$majorMinor-patches/bash${majorMinor//./}-$patch"; 			wget -O "bash-patches/$patch" "$url"; 			wget -O "bash-patches/$patch.sig" "$url.sig"; 		done; 	fi; 		apk add --no-cache --virtual .gpg-deps gnupg; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7C0135FB088AAF6C66C650B9BB5869F064EA74AB; 	gpg --batch --verify bash.tar.gz.sig bash.tar.gz; 	rm bash.tar.gz.sig; 	if [ -d bash-patches ]; then 		for sig in bash-patches/*.sig; do 			p="${sig%.sig}"; 			gpg --batch --verify "$sig" "$p"; 			rm "$sig"; 		done; 	fi; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apk del --no-network .gpg-deps; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	for f in config.guess config.sub; do 		wget -O "support/$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 	done; 	export CFLAGS='-Wno-error=implicit-int -Wno-error=implicit-function-declaration'; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	[ "$(bash -c 'echo "${BASH_VERSION%%[^0-9.]*}"')" = "$_BASH_VERSION" ]; 	bash -c 'help' > /dev/null # buildkit
# Fri, 30 May 2025 18:45:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 30 May 2025 18:45:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 30 May 2025 18:45:01 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cca7947b045046ae688c811401f56d768614bd200e041163906d7c900a26a56a`  
		Last Modified: Tue, 03 Jun 2025 13:30:50 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e1f9ab8520fa557307d941b0fa150b0676d0b4940f6ffba29fa12d3b0043900`  
		Last Modified: Tue, 03 Jun 2025 13:30:50 GMT  
		Size: 1.1 MB (1077291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc6a9154c1ca8b52a7ad943858a1e759d48ad598a85650b48c99f493bd5357b7`  
		Last Modified: Tue, 03 Jun 2025 13:30:52 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:4-alpine3.22` - unknown; unknown

```console
$ docker pull bash@sha256:837e9618509edd1c3c781d98df49915bf045d3215986c552533b494c54d1518e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.5 KB (142477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b67b96dd2b7d8c5ff025d3ed422a7601aa00d97518ca382debdfc5eda1c74f5`

```dockerfile
```

-	Layers:
	-	`sha256:17a5c9ea52f1ff0a35943bbaf0e43b577194714dbab8517573c8a30324bf347d`  
		Last Modified: Fri, 06 Jun 2025 08:42:33 GMT  
		Size: 119.0 KB (118981 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:999380a8673956665a770b30166e22b22620abb6b20b50e939d52b1f82b94b1c`  
		Last Modified: Fri, 06 Jun 2025 08:42:35 GMT  
		Size: 23.5 KB (23496 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:4-alpine3.22` - linux; arm variant v6

```console
$ docker pull bash@sha256:331ad94a5f0263efef20a44981642d25f979f95d5a18dfb221ef55dd559e7265
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4580345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df1f3b1bd8091fed8ebc08e118e999c6788c7a3433ba9a8f024ece7906ede1e1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 18:45:01 GMT
ENV _BASH_VERSION=4.4.23
# Fri, 30 May 2025 18:45:01 GMT
ENV _BASH_BASELINE=4.4.18
# Fri, 30 May 2025 18:45:01 GMT
ENV _BASH_BASELINE_PATCH=18
# Fri, 30 May 2025 18:45:01 GMT
ENV _BASH_LATEST_PATCH=23
# Fri, 30 May 2025 18:45:01 GMT
COPY alpine3.21.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Fri, 30 May 2025 18:45:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz"; 	wget -O bash.tar.gz.sig "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz.sig"; 		: "${_BASH_BASELINE_PATCH:=0}" "${_BASH_LATEST_PATCH:=0}"; 	if [ "$_BASH_LATEST_PATCH" -gt "$_BASH_BASELINE_PATCH" ]; then 		mkdir -p bash-patches; 		first="$(printf '%03d' "$(( _BASH_BASELINE_PATCH + 1 ))")"; 		last="$(printf '%03d' "$_BASH_LATEST_PATCH")"; 		majorMinor="${_BASH_VERSION%.*}"; 		for patch in $(seq -w "$first" "$last"); do 			url="https://ftp.gnu.org/gnu/bash/bash-$majorMinor-patches/bash${majorMinor//./}-$patch"; 			wget -O "bash-patches/$patch" "$url"; 			wget -O "bash-patches/$patch.sig" "$url.sig"; 		done; 	fi; 		apk add --no-cache --virtual .gpg-deps gnupg; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7C0135FB088AAF6C66C650B9BB5869F064EA74AB; 	gpg --batch --verify bash.tar.gz.sig bash.tar.gz; 	rm bash.tar.gz.sig; 	if [ -d bash-patches ]; then 		for sig in bash-patches/*.sig; do 			p="${sig%.sig}"; 			gpg --batch --verify "$sig" "$p"; 			rm "$sig"; 		done; 	fi; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apk del --no-network .gpg-deps; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	for f in config.guess config.sub; do 		wget -O "support/$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 	done; 	export CFLAGS='-Wno-error=implicit-int -Wno-error=implicit-function-declaration'; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	[ "$(bash -c 'echo "${BASH_VERSION%%[^0-9.]*}"')" = "$_BASH_VERSION" ]; 	bash -c 'help' > /dev/null # buildkit
# Fri, 30 May 2025 18:45:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 30 May 2025 18:45:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 30 May 2025 18:45:01 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e50a5d6e348e8c276cf343aabe47356b43d0c25d14456a9ef4a994d74161906`  
		Last Modified: Fri, 06 Jun 2025 08:42:39 GMT  
		Size: 592.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:867e3bfd52c3603194afb2562122a5bb7c9e9ab66ac3a224070a39f3e7252a79`  
		Last Modified: Fri, 06 Jun 2025 08:42:41 GMT  
		Size: 1.1 MB (1078492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e42f04c87df24102cd7c6907fa660edf214d6046e89010634fdf08de6035ac4`  
		Last Modified: Fri, 06 Jun 2025 08:42:42 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:4-alpine3.22` - unknown; unknown

```console
$ docker pull bash@sha256:855a5a56e330c4023282125e4bddff6999e98c720465e095047895ad473761bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.4 KB (23373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2b56af99adcd48abef6f17cc8313cfa79f7e8ca4310d2d6a8082de4c81c6905`

```dockerfile
```

-	Layers:
	-	`sha256:d95cfd74a1c66759fc31ea92333fc015a2d676d5504ca45e0809c063775aa1c4`  
		Last Modified: Fri, 06 Jun 2025 08:42:46 GMT  
		Size: 23.4 KB (23373 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:4-alpine3.22` - linux; arm variant v7

```console
$ docker pull bash@sha256:2349a33f123874f745adfc144d99404e47afc1f5075dc37fd05dc9cc71f9bd71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4253233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe3882b6556c76d7ea8742cef86577d1859e299c9bee77230f126a163500ecb2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 18:45:01 GMT
ENV _BASH_VERSION=4.4.23
# Fri, 30 May 2025 18:45:01 GMT
ENV _BASH_BASELINE=4.4.18
# Fri, 30 May 2025 18:45:01 GMT
ENV _BASH_BASELINE_PATCH=18
# Fri, 30 May 2025 18:45:01 GMT
ENV _BASH_LATEST_PATCH=23
# Fri, 30 May 2025 18:45:01 GMT
COPY alpine3.21.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Fri, 30 May 2025 18:45:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz"; 	wget -O bash.tar.gz.sig "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz.sig"; 		: "${_BASH_BASELINE_PATCH:=0}" "${_BASH_LATEST_PATCH:=0}"; 	if [ "$_BASH_LATEST_PATCH" -gt "$_BASH_BASELINE_PATCH" ]; then 		mkdir -p bash-patches; 		first="$(printf '%03d' "$(( _BASH_BASELINE_PATCH + 1 ))")"; 		last="$(printf '%03d' "$_BASH_LATEST_PATCH")"; 		majorMinor="${_BASH_VERSION%.*}"; 		for patch in $(seq -w "$first" "$last"); do 			url="https://ftp.gnu.org/gnu/bash/bash-$majorMinor-patches/bash${majorMinor//./}-$patch"; 			wget -O "bash-patches/$patch" "$url"; 			wget -O "bash-patches/$patch.sig" "$url.sig"; 		done; 	fi; 		apk add --no-cache --virtual .gpg-deps gnupg; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7C0135FB088AAF6C66C650B9BB5869F064EA74AB; 	gpg --batch --verify bash.tar.gz.sig bash.tar.gz; 	rm bash.tar.gz.sig; 	if [ -d bash-patches ]; then 		for sig in bash-patches/*.sig; do 			p="${sig%.sig}"; 			gpg --batch --verify "$sig" "$p"; 			rm "$sig"; 		done; 	fi; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apk del --no-network .gpg-deps; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	for f in config.guess config.sub; do 		wget -O "support/$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 	done; 	export CFLAGS='-Wno-error=implicit-int -Wno-error=implicit-function-declaration'; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	[ "$(bash -c 'echo "${BASH_VERSION%%[^0-9.]*}"')" = "$_BASH_VERSION" ]; 	bash -c 'help' > /dev/null # buildkit
# Fri, 30 May 2025 18:45:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 30 May 2025 18:45:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 30 May 2025 18:45:01 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffe02f6f6774a1d41ce78a73c7b2b98dc34b74114c9fe9ff4bed2eaeddfaad62`  
		Last Modified: Fri, 06 Jun 2025 08:42:50 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39ebf867bdd7177cb8290b80dff45f22dbbf8da5e4e5b49add251db3a5396922`  
		Last Modified: Fri, 06 Jun 2025 08:42:52 GMT  
		Size: 1.0 MB (1033122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2833a879d93454094ddc4b7ccccac043ad911ad2993c8e8b62ebb4bd1352f56`  
		Last Modified: Fri, 06 Jun 2025 08:42:54 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:4-alpine3.22` - unknown; unknown

```console
$ docker pull bash@sha256:32b7da368255a0a045dab29c9b0869c6fc39b26a1bf1b237e32203d888d96e30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.6 KB (142621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f8ef78dc40a660a2859e5767a2a9613e32d7ad9494ff38eb4ed11947f809f70`

```dockerfile
```

-	Layers:
	-	`sha256:01e7186102539b0302dd0622c0ed23e2fb18d71a9bf045a954a9f11e12356d82`  
		Last Modified: Fri, 06 Jun 2025 08:42:57 GMT  
		Size: 119.0 KB (119033 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9295c447ab6b6f1d7e0199e8e87f70a30a7727cc86bcb8df4e372c85af0142ae`  
		Last Modified: Fri, 06 Jun 2025 08:42:59 GMT  
		Size: 23.6 KB (23588 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:4-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull bash@sha256:8fbd7c0c8445d6acdc47ae5149581ce9bdc849717e212b4c9eb5edfe6761b3f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5233395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4e80d199878e87da18575d5b1aa6e6e09612e7faedbc5d66243164b0da48c98`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 18:45:01 GMT
ENV _BASH_VERSION=4.4.23
# Fri, 30 May 2025 18:45:01 GMT
ENV _BASH_BASELINE=4.4.18
# Fri, 30 May 2025 18:45:01 GMT
ENV _BASH_BASELINE_PATCH=18
# Fri, 30 May 2025 18:45:01 GMT
ENV _BASH_LATEST_PATCH=23
# Fri, 30 May 2025 18:45:01 GMT
COPY alpine3.21.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Fri, 30 May 2025 18:45:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz"; 	wget -O bash.tar.gz.sig "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz.sig"; 		: "${_BASH_BASELINE_PATCH:=0}" "${_BASH_LATEST_PATCH:=0}"; 	if [ "$_BASH_LATEST_PATCH" -gt "$_BASH_BASELINE_PATCH" ]; then 		mkdir -p bash-patches; 		first="$(printf '%03d' "$(( _BASH_BASELINE_PATCH + 1 ))")"; 		last="$(printf '%03d' "$_BASH_LATEST_PATCH")"; 		majorMinor="${_BASH_VERSION%.*}"; 		for patch in $(seq -w "$first" "$last"); do 			url="https://ftp.gnu.org/gnu/bash/bash-$majorMinor-patches/bash${majorMinor//./}-$patch"; 			wget -O "bash-patches/$patch" "$url"; 			wget -O "bash-patches/$patch.sig" "$url.sig"; 		done; 	fi; 		apk add --no-cache --virtual .gpg-deps gnupg; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7C0135FB088AAF6C66C650B9BB5869F064EA74AB; 	gpg --batch --verify bash.tar.gz.sig bash.tar.gz; 	rm bash.tar.gz.sig; 	if [ -d bash-patches ]; then 		for sig in bash-patches/*.sig; do 			p="${sig%.sig}"; 			gpg --batch --verify "$sig" "$p"; 			rm "$sig"; 		done; 	fi; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apk del --no-network .gpg-deps; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	for f in config.guess config.sub; do 		wget -O "support/$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 	done; 	export CFLAGS='-Wno-error=implicit-int -Wno-error=implicit-function-declaration'; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	[ "$(bash -c 'echo "${BASH_VERSION%%[^0-9.]*}"')" = "$_BASH_VERSION" ]; 	bash -c 'help' > /dev/null # buildkit
# Fri, 30 May 2025 18:45:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 30 May 2025 18:45:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 30 May 2025 18:45:01 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57ff2aea0a10d76dd36056b9037efcf5c884cf3fcbfe16cce635c3147f31b890`  
		Last Modified: Tue, 03 Jun 2025 14:06:32 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80d2ab9b084cd9482b1104ce7c31f1db0a30af6e6bc39b9416f717552410fb63`  
		Last Modified: Tue, 03 Jun 2025 14:06:38 GMT  
		Size: 1.1 MB (1096520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:badb5343307a69787126044e2a5036db28e3afb56e2cb94a5373c78b98d57a4a`  
		Last Modified: Tue, 03 Jun 2025 14:06:36 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:4-alpine3.22` - unknown; unknown

```console
$ docker pull bash@sha256:cbd2761417cf5dad5879fa55e319a38f1f99792927efc7e74f9478aed54df349
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.7 KB (142685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a421d80e269a69c62ac29ddcabb9393433e029f70986168f48da696a7b8e8114`

```dockerfile
```

-	Layers:
	-	`sha256:4e7658616700be4fce887eed31ea52c8115b5e534313db39475c73aa1ba8044a`  
		Last Modified: Fri, 06 Jun 2025 08:43:10 GMT  
		Size: 119.1 KB (119061 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6cfda988f1a678162b9ad90e610625517688b9e55fd23b3a7540083c3e64cce`  
		Last Modified: Fri, 06 Jun 2025 08:43:11 GMT  
		Size: 23.6 KB (23624 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:4-alpine3.22` - linux; 386

```console
$ docker pull bash@sha256:f0098046a1f2fbafed7724861e660fa7b272f6b30156617642436f5271ab7f78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4671028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0d80a941501375a696b851444ca07b1f743876eae5f438db559f8206d20c7ed`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 18:45:01 GMT
ENV _BASH_VERSION=4.4.23
# Fri, 30 May 2025 18:45:01 GMT
ENV _BASH_BASELINE=4.4.18
# Fri, 30 May 2025 18:45:01 GMT
ENV _BASH_BASELINE_PATCH=18
# Fri, 30 May 2025 18:45:01 GMT
ENV _BASH_LATEST_PATCH=23
# Fri, 30 May 2025 18:45:01 GMT
COPY alpine3.21.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Fri, 30 May 2025 18:45:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz"; 	wget -O bash.tar.gz.sig "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz.sig"; 		: "${_BASH_BASELINE_PATCH:=0}" "${_BASH_LATEST_PATCH:=0}"; 	if [ "$_BASH_LATEST_PATCH" -gt "$_BASH_BASELINE_PATCH" ]; then 		mkdir -p bash-patches; 		first="$(printf '%03d' "$(( _BASH_BASELINE_PATCH + 1 ))")"; 		last="$(printf '%03d' "$_BASH_LATEST_PATCH")"; 		majorMinor="${_BASH_VERSION%.*}"; 		for patch in $(seq -w "$first" "$last"); do 			url="https://ftp.gnu.org/gnu/bash/bash-$majorMinor-patches/bash${majorMinor//./}-$patch"; 			wget -O "bash-patches/$patch" "$url"; 			wget -O "bash-patches/$patch.sig" "$url.sig"; 		done; 	fi; 		apk add --no-cache --virtual .gpg-deps gnupg; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7C0135FB088AAF6C66C650B9BB5869F064EA74AB; 	gpg --batch --verify bash.tar.gz.sig bash.tar.gz; 	rm bash.tar.gz.sig; 	if [ -d bash-patches ]; then 		for sig in bash-patches/*.sig; do 			p="${sig%.sig}"; 			gpg --batch --verify "$sig" "$p"; 			rm "$sig"; 		done; 	fi; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apk del --no-network .gpg-deps; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	for f in config.guess config.sub; do 		wget -O "support/$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 	done; 	export CFLAGS='-Wno-error=implicit-int -Wno-error=implicit-function-declaration'; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	[ "$(bash -c 'echo "${BASH_VERSION%%[^0-9.]*}"')" = "$_BASH_VERSION" ]; 	bash -c 'help' > /dev/null # buildkit
# Fri, 30 May 2025 18:45:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 30 May 2025 18:45:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 30 May 2025 18:45:01 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:c787620501b746b3aa9ec021f3ddb0b707572b5c68e33d73be392b9c078a4993`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 3.6 MB (3616029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8a805e00e4bacc440abd6490a521e8725b5ec2a55f15b04a1f78963cbc47665`  
		Last Modified: Fri, 06 Jun 2025 08:43:15 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d04615467d20e1338b4e40d4eabc9220b50e2033e29deb2766c541150ae9f402`  
		Last Modified: Fri, 06 Jun 2025 08:43:17 GMT  
		Size: 1.1 MB (1054068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7cb3a05d73cff31c29854d11dca5a9a371d8b4b04ff978469987953c589ec90`  
		Last Modified: Fri, 06 Jun 2025 08:43:18 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:4-alpine3.22` - unknown; unknown

```console
$ docker pull bash@sha256:617da95b7fe47e52bc5d432bbd94264e63c0b87f6b3f61ed8ebca8595bf25df7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.4 KB (142399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29c82ce4700ee3c92456070fdf2566455af4264c6539b60fee87772d9f09a059`

```dockerfile
```

-	Layers:
	-	`sha256:03effde44077c37cc9e3c53e8dd13dd52064db6f3cc3980adafcd7329dec3648`  
		Last Modified: Fri, 06 Jun 2025 08:43:22 GMT  
		Size: 118.9 KB (118946 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:343c4f02dd593c988918e849145c92e43dc65e7efc9cc7d974c25d7c87cdc94d`  
		Last Modified: Fri, 06 Jun 2025 08:43:23 GMT  
		Size: 23.5 KB (23453 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:4-alpine3.22` - linux; ppc64le

```console
$ docker pull bash@sha256:d7acd4b676f55b95506cdf27879eb6184a530e018f5e36bc3b79d7b2f2918f9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4866490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c37ca88e0c881796d7bfd7f2dd43d1538de410b6b40a4c57af05df5dc0edc1c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-ppc64le.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 18:45:01 GMT
ENV _BASH_VERSION=4.4.23
# Fri, 30 May 2025 18:45:01 GMT
ENV _BASH_BASELINE=4.4.18
# Fri, 30 May 2025 18:45:01 GMT
ENV _BASH_BASELINE_PATCH=18
# Fri, 30 May 2025 18:45:01 GMT
ENV _BASH_LATEST_PATCH=23
# Fri, 30 May 2025 18:45:01 GMT
COPY alpine3.21.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Fri, 30 May 2025 18:45:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz"; 	wget -O bash.tar.gz.sig "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz.sig"; 		: "${_BASH_BASELINE_PATCH:=0}" "${_BASH_LATEST_PATCH:=0}"; 	if [ "$_BASH_LATEST_PATCH" -gt "$_BASH_BASELINE_PATCH" ]; then 		mkdir -p bash-patches; 		first="$(printf '%03d' "$(( _BASH_BASELINE_PATCH + 1 ))")"; 		last="$(printf '%03d' "$_BASH_LATEST_PATCH")"; 		majorMinor="${_BASH_VERSION%.*}"; 		for patch in $(seq -w "$first" "$last"); do 			url="https://ftp.gnu.org/gnu/bash/bash-$majorMinor-patches/bash${majorMinor//./}-$patch"; 			wget -O "bash-patches/$patch" "$url"; 			wget -O "bash-patches/$patch.sig" "$url.sig"; 		done; 	fi; 		apk add --no-cache --virtual .gpg-deps gnupg; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7C0135FB088AAF6C66C650B9BB5869F064EA74AB; 	gpg --batch --verify bash.tar.gz.sig bash.tar.gz; 	rm bash.tar.gz.sig; 	if [ -d bash-patches ]; then 		for sig in bash-patches/*.sig; do 			p="${sig%.sig}"; 			gpg --batch --verify "$sig" "$p"; 			rm "$sig"; 		done; 	fi; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apk del --no-network .gpg-deps; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	for f in config.guess config.sub; do 		wget -O "support/$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 	done; 	export CFLAGS='-Wno-error=implicit-int -Wno-error=implicit-function-declaration'; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	[ "$(bash -c 'echo "${BASH_VERSION%%[^0-9.]*}"')" = "$_BASH_VERSION" ]; 	bash -c 'help' > /dev/null # buildkit
# Fri, 30 May 2025 18:45:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 30 May 2025 18:45:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 30 May 2025 18:45:01 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:33a2433d89df7e794d1655fce70d7031d8065c9798bdc2931f7c98fcc8d310d0`  
		Last Modified: Tue, 03 Jun 2025 13:30:33 GMT  
		Size: 3.7 MB (3730187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6053f07ee34f8243fe4730b026bda16f0fe106674241e927ee003d668d05fac2`  
		Last Modified: Fri, 06 Jun 2025 08:43:27 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:088e88a8a767277f3dc37187af0672797614f6f9d22f42450d5925a3cf96f313`  
		Last Modified: Fri, 06 Jun 2025 08:43:29 GMT  
		Size: 1.1 MB (1135367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e4b9dd8ce20350eec885fff350349b7190071621ee7d133b787e6131712417e`  
		Last Modified: Fri, 06 Jun 2025 08:43:30 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:4-alpine3.22` - unknown; unknown

```console
$ docker pull bash@sha256:19b1d4132038ae1edf390a9bd7b6bf7149471def33384405c4081dba29375e06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.6 KB (140628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88184c1864d4bff1d22b33587edcfef977b61b88437806b0536e5ca49279cd15`

```dockerfile
```

-	Layers:
	-	`sha256:5a6b6f17a3f6d570ac836e45cc245b64a9fdf8bed12f973d6d42fed2f5709503`  
		Last Modified: Fri, 06 Jun 2025 08:43:34 GMT  
		Size: 117.1 KB (117076 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1282dbbd4fc48a9acf6258fb0b2bfb5e29cb483c2d9e8f61742dc286fc48a258`  
		Last Modified: Fri, 06 Jun 2025 08:43:35 GMT  
		Size: 23.6 KB (23552 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:4-alpine3.22` - linux; riscv64

```console
$ docker pull bash@sha256:c0fff9b2b97ab5cf43e0d46b4298db059ae3892a32e97b41c40088a420fd222b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4608421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b22fed89d44483ec3f132a1699cde7d75b9c0443ca2c7d7ee2143ea120218e37`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-riscv64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 18:45:01 GMT
ENV _BASH_VERSION=4.4.23
# Fri, 30 May 2025 18:45:01 GMT
ENV _BASH_BASELINE=4.4.18
# Fri, 30 May 2025 18:45:01 GMT
ENV _BASH_BASELINE_PATCH=18
# Fri, 30 May 2025 18:45:01 GMT
ENV _BASH_LATEST_PATCH=23
# Fri, 30 May 2025 18:45:01 GMT
COPY alpine3.21.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Fri, 30 May 2025 18:45:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz"; 	wget -O bash.tar.gz.sig "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz.sig"; 		: "${_BASH_BASELINE_PATCH:=0}" "${_BASH_LATEST_PATCH:=0}"; 	if [ "$_BASH_LATEST_PATCH" -gt "$_BASH_BASELINE_PATCH" ]; then 		mkdir -p bash-patches; 		first="$(printf '%03d' "$(( _BASH_BASELINE_PATCH + 1 ))")"; 		last="$(printf '%03d' "$_BASH_LATEST_PATCH")"; 		majorMinor="${_BASH_VERSION%.*}"; 		for patch in $(seq -w "$first" "$last"); do 			url="https://ftp.gnu.org/gnu/bash/bash-$majorMinor-patches/bash${majorMinor//./}-$patch"; 			wget -O "bash-patches/$patch" "$url"; 			wget -O "bash-patches/$patch.sig" "$url.sig"; 		done; 	fi; 		apk add --no-cache --virtual .gpg-deps gnupg; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7C0135FB088AAF6C66C650B9BB5869F064EA74AB; 	gpg --batch --verify bash.tar.gz.sig bash.tar.gz; 	rm bash.tar.gz.sig; 	if [ -d bash-patches ]; then 		for sig in bash-patches/*.sig; do 			p="${sig%.sig}"; 			gpg --batch --verify "$sig" "$p"; 			rm "$sig"; 		done; 	fi; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apk del --no-network .gpg-deps; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	for f in config.guess config.sub; do 		wget -O "support/$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 	done; 	export CFLAGS='-Wno-error=implicit-int -Wno-error=implicit-function-declaration'; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	[ "$(bash -c 'echo "${BASH_VERSION%%[^0-9.]*}"')" = "$_BASH_VERSION" ]; 	bash -c 'help' > /dev/null # buildkit
# Fri, 30 May 2025 18:45:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 30 May 2025 18:45:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 30 May 2025 18:45:01 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:a0a4beaa1960bba353066d674aa0e3378b856b09e6d3f704d1755daa5d6c1d39`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.5 MB (3513811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b81da3cc124a68f972e1dccdd763aa477cacbe790fbcb5c2374a536d05ab09b4`  
		Last Modified: Fri, 06 Jun 2025 08:43:39 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f88f86af2c3d140f542bc22155a78d994e09348d2ed903a89f5c529094d5346`  
		Last Modified: Fri, 06 Jun 2025 08:43:41 GMT  
		Size: 1.1 MB (1093673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbd78bfb40a8e09f34e9533852b3291dc24e56c5c69079791f6659738dc87d0a`  
		Last Modified: Fri, 06 Jun 2025 08:43:42 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:4-alpine3.22` - unknown; unknown

```console
$ docker pull bash@sha256:d624c9c5454d1fb1dc32db577015bec18660b2266f4129808549d81cdc8efa20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.6 KB (140624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22ed9d92381a4d598e82c8a18b70a846ac8eb76ee41c7d485fb3fcab0f7745e3`

```dockerfile
```

-	Layers:
	-	`sha256:2499598820d814ae3efd05ecdecfae6035bcc6e5210a05e46592512407108833`  
		Last Modified: Fri, 06 Jun 2025 08:43:46 GMT  
		Size: 117.1 KB (117072 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a757e52c7f59839ab391fdd8c10fc423bf88d09f8f518d8cfd902f3a12abe516`  
		Last Modified: Fri, 06 Jun 2025 08:43:47 GMT  
		Size: 23.6 KB (23552 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:4-alpine3.22` - linux; s390x

```console
$ docker pull bash@sha256:b641f21a3f231057bfef334dc43dcdc3b393c766dfd31c28f791c806506bf4eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4765017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fc55d999f0e045c0e2520bb24239649ce93a32c3f1b4586bbf8706b0df79471`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-s390x.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 18:45:01 GMT
ENV _BASH_VERSION=4.4.23
# Fri, 30 May 2025 18:45:01 GMT
ENV _BASH_BASELINE=4.4.18
# Fri, 30 May 2025 18:45:01 GMT
ENV _BASH_BASELINE_PATCH=18
# Fri, 30 May 2025 18:45:01 GMT
ENV _BASH_LATEST_PATCH=23
# Fri, 30 May 2025 18:45:01 GMT
COPY alpine3.21.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Fri, 30 May 2025 18:45:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz"; 	wget -O bash.tar.gz.sig "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz.sig"; 		: "${_BASH_BASELINE_PATCH:=0}" "${_BASH_LATEST_PATCH:=0}"; 	if [ "$_BASH_LATEST_PATCH" -gt "$_BASH_BASELINE_PATCH" ]; then 		mkdir -p bash-patches; 		first="$(printf '%03d' "$(( _BASH_BASELINE_PATCH + 1 ))")"; 		last="$(printf '%03d' "$_BASH_LATEST_PATCH")"; 		majorMinor="${_BASH_VERSION%.*}"; 		for patch in $(seq -w "$first" "$last"); do 			url="https://ftp.gnu.org/gnu/bash/bash-$majorMinor-patches/bash${majorMinor//./}-$patch"; 			wget -O "bash-patches/$patch" "$url"; 			wget -O "bash-patches/$patch.sig" "$url.sig"; 		done; 	fi; 		apk add --no-cache --virtual .gpg-deps gnupg; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7C0135FB088AAF6C66C650B9BB5869F064EA74AB; 	gpg --batch --verify bash.tar.gz.sig bash.tar.gz; 	rm bash.tar.gz.sig; 	if [ -d bash-patches ]; then 		for sig in bash-patches/*.sig; do 			p="${sig%.sig}"; 			gpg --batch --verify "$sig" "$p"; 			rm "$sig"; 		done; 	fi; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apk del --no-network .gpg-deps; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	for f in config.guess config.sub; do 		wget -O "support/$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 	done; 	export CFLAGS='-Wno-error=implicit-int -Wno-error=implicit-function-declaration'; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	[ "$(bash -c 'echo "${BASH_VERSION%%[^0-9.]*}"')" = "$_BASH_VERSION" ]; 	bash -c 'help' > /dev/null # buildkit
# Fri, 30 May 2025 18:45:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 30 May 2025 18:45:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 30 May 2025 18:45:01 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:47a70fdc8ac4c1273de626dc7710d3e19cfd5b9f3e10cfc4b14602bdfffbffe1`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.6 MB (3647529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e4a9e4a96bee0e859e6251070538f67d5d58cecabfc2aaa3da00214f6aea2d4`  
		Last Modified: Fri, 06 Jun 2025 08:43:51 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e094400ac566e9454bb993d17f7cc72e03351d5be4e7cf097df025cba80e75ed`  
		Last Modified: Fri, 06 Jun 2025 08:43:54 GMT  
		Size: 1.1 MB (1116553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d9114a8d38cacc3d2f28eeef5b5e777ecaab6676922cab27b9ee427b0be1d11`  
		Last Modified: Fri, 06 Jun 2025 08:43:54 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:4-alpine3.22` - unknown; unknown

```console
$ docker pull bash@sha256:2391bfd68ac2c489983d9328629a4e3747948f1969fb7b825689ee3c26c7cc79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.5 KB (140526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c26377d7eff17d238ec70e7f439d9bcc02ae2ecfec5722f1c7682572630500c`

```dockerfile
```

-	Layers:
	-	`sha256:c0dd1132fcf5b1b90e6c4ac78f3c2fb6f48705e72d5919fd7169d6fb5ea4b2ea`  
		Last Modified: Fri, 06 Jun 2025 08:43:58 GMT  
		Size: 117.0 KB (117030 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02f25947e4343fb4cb43d34bb854463cb6743a7808b8f4c4dd031b4d2a84d0db`  
		Last Modified: Fri, 06 Jun 2025 08:44:00 GMT  
		Size: 23.5 KB (23496 bytes)  
		MIME: application/vnd.in-toto+json
