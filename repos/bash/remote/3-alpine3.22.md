## `bash:3-alpine3.22`

```console
$ docker pull bash@sha256:09e5a7aefe37d28729ea57c59819e88cc5ffa9c1ab052ad90b19ba8c43ce6d02
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

### `bash:3-alpine3.22` - linux; amd64

```console
$ docker pull bash@sha256:0a7844ce48bc41a81b460defc102450460a7bd8d6baff96cc133e1af3e8667dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4454302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65a89f9522fdf0732f3b8c086f9c65555ba80a4d6d732ce586e0e315abb1e200`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 07 Jul 2025 22:42:46 GMT
ENV _BASH_VERSION=3.2.57
# Mon, 07 Jul 2025 22:42:46 GMT
ENV _BASH_BASELINE=3.2.57
# Mon, 07 Jul 2025 22:42:46 GMT
ENV _BASH_BASELINE_PATCH=57
# Mon, 07 Jul 2025 22:42:46 GMT
ENV _BASH_LATEST_PATCH=57
# Mon, 07 Jul 2025 22:42:46 GMT
COPY alpine3.21.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Mon, 07 Jul 2025 22:42:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz"; 	wget -O bash.tar.gz.sig "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz.sig"; 		: "${_BASH_BASELINE_PATCH:=0}" "${_BASH_LATEST_PATCH:=0}"; 	if [ "$_BASH_LATEST_PATCH" -gt "$_BASH_BASELINE_PATCH" ]; then 		mkdir -p bash-patches; 		first="$(printf '%03d' "$(( _BASH_BASELINE_PATCH + 1 ))")"; 		last="$(printf '%03d' "$_BASH_LATEST_PATCH")"; 		majorMinor="${_BASH_VERSION%.*}"; 		for patch in $(seq -w "$first" "$last"); do 			url="https://ftp.gnu.org/gnu/bash/bash-$majorMinor-patches/bash${majorMinor//./}-$patch"; 			wget -O "bash-patches/$patch" "$url"; 			wget -O "bash-patches/$patch.sig" "$url.sig"; 		done; 	fi; 		apk add --no-cache --virtual .gpg-deps gnupg; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7C0135FB088AAF6C66C650B9BB5869F064EA74AB; 	gpg --batch --verify bash.tar.gz.sig bash.tar.gz; 	rm bash.tar.gz.sig; 	if [ -d bash-patches ]; then 		for sig in bash-patches/*.sig; do 			p="${sig%.sig}"; 			gpg --batch --verify "$sig" "$p"; 			rm "$sig"; 		done; 	fi; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apk del --no-network .gpg-deps; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	for f in config.guess config.sub; do 		wget -T2 -O "support/$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb" || 			wget -O "support/$f" "https://github.com/tianon/mirror-gnu-config/raw/7d3d27baf8107b630586c962c057e22149653deb/$f"; 	done; 	export CFLAGS='-Wno-error=implicit-int -Wno-error=implicit-function-declaration'; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make y.tab.c; make builtins/libbuiltins.a; 	make -j 1; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	[ "$(bash -c 'echo "${BASH_VERSION%%[^0-9.]*}"')" = "$_BASH_VERSION" ]; 	bash -c 'help' > /dev/null # buildkit
# Mon, 07 Jul 2025 22:42:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 07 Jul 2025 22:42:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 07 Jul 2025 22:42:46 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46a95b8f86852773adfed7ab4fdf314e63c56ad7fc0320b92f4ff3cc1a85b2e1`  
		Last Modified: Mon, 07 Jul 2025 22:56:46 GMT  
		Size: 1.6 KB (1630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20edb512ec8dddbf250d2a4ab4ced76c07bf300c4e9a3a6b1b2ef9d15867e262`  
		Last Modified: Mon, 07 Jul 2025 22:56:48 GMT  
		Size: 655.5 KB (655491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19c0f5730bc41bb291f80e4618699a2808022564d54029a656a46480c25db904`  
		Last Modified: Mon, 07 Jul 2025 22:56:47 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:3-alpine3.22` - unknown; unknown

```console
$ docker pull bash@sha256:29f947c580ce7432aed85a688c21bee417a3992b3ddc8f008cb4a692d06ffd7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.1 KB (143054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca4bfc85100edd361b0b9bb83b810c83689ce4b1aeb8ea8fe69a5604ce287b72`

```dockerfile
```

-	Layers:
	-	`sha256:f4da86790551efeaf28df8d964d84e6439bde74be617132db5e6fad9807954f1`  
		Last Modified: Tue, 08 Jul 2025 00:01:32 GMT  
		Size: 119.0 KB (118981 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7287a58af17e07f652a5bd195e1d64a17609fe8fb32a2125c06b133e4e586850`  
		Last Modified: Tue, 08 Jul 2025 00:01:33 GMT  
		Size: 24.1 KB (24073 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:3-alpine3.22` - linux; arm variant v6

```console
$ docker pull bash@sha256:29fd33120c468a24fe376501f269b2201af2895d632a30dfde94c29d6629c297
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4157602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2c0d9a0443f5ca1f29a4a06bfc9925a3f427c381700340d2a8235470346f6c7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 07 Jul 2025 22:42:46 GMT
ENV _BASH_VERSION=3.2.57
# Mon, 07 Jul 2025 22:42:46 GMT
ENV _BASH_BASELINE=3.2.57
# Mon, 07 Jul 2025 22:42:46 GMT
ENV _BASH_BASELINE_PATCH=57
# Mon, 07 Jul 2025 22:42:46 GMT
ENV _BASH_LATEST_PATCH=57
# Mon, 07 Jul 2025 22:42:46 GMT
COPY alpine3.21.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Mon, 07 Jul 2025 22:42:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz"; 	wget -O bash.tar.gz.sig "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz.sig"; 		: "${_BASH_BASELINE_PATCH:=0}" "${_BASH_LATEST_PATCH:=0}"; 	if [ "$_BASH_LATEST_PATCH" -gt "$_BASH_BASELINE_PATCH" ]; then 		mkdir -p bash-patches; 		first="$(printf '%03d' "$(( _BASH_BASELINE_PATCH + 1 ))")"; 		last="$(printf '%03d' "$_BASH_LATEST_PATCH")"; 		majorMinor="${_BASH_VERSION%.*}"; 		for patch in $(seq -w "$first" "$last"); do 			url="https://ftp.gnu.org/gnu/bash/bash-$majorMinor-patches/bash${majorMinor//./}-$patch"; 			wget -O "bash-patches/$patch" "$url"; 			wget -O "bash-patches/$patch.sig" "$url.sig"; 		done; 	fi; 		apk add --no-cache --virtual .gpg-deps gnupg; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7C0135FB088AAF6C66C650B9BB5869F064EA74AB; 	gpg --batch --verify bash.tar.gz.sig bash.tar.gz; 	rm bash.tar.gz.sig; 	if [ -d bash-patches ]; then 		for sig in bash-patches/*.sig; do 			p="${sig%.sig}"; 			gpg --batch --verify "$sig" "$p"; 			rm "$sig"; 		done; 	fi; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apk del --no-network .gpg-deps; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	for f in config.guess config.sub; do 		wget -T2 -O "support/$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb" || 			wget -O "support/$f" "https://github.com/tianon/mirror-gnu-config/raw/7d3d27baf8107b630586c962c057e22149653deb/$f"; 	done; 	export CFLAGS='-Wno-error=implicit-int -Wno-error=implicit-function-declaration'; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make y.tab.c; make builtins/libbuiltins.a; 	make -j 1; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	[ "$(bash -c 'echo "${BASH_VERSION%%[^0-9.]*}"')" = "$_BASH_VERSION" ]; 	bash -c 'help' > /dev/null # buildkit
# Mon, 07 Jul 2025 22:42:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 07 Jul 2025 22:42:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 07 Jul 2025 22:42:46 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:240a38f2fd18ea0f49beed4ae70efac263ceba425aa8ae1f5a6e6edcb330f238`  
		Last Modified: Tue, 08 Jul 2025 01:11:25 GMT  
		Size: 1.6 KB (1629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eece965bd4c32b0e1e918e484db8f4e7e5611bf16bf65598be81af841929b122`  
		Last Modified: Tue, 08 Jul 2025 01:11:26 GMT  
		Size: 654.7 KB (654713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c0a7d5a02e6a770299c9501cc9f9db9e8739e6c22b42010f4246cf39aea108f`  
		Last Modified: Tue, 08 Jul 2025 01:11:25 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:3-alpine3.22` - unknown; unknown

```console
$ docker pull bash@sha256:db21a3d3115ef509eee9ceb84e11b121f4fda38dccc53646da3f14cb9a284a5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 KB (23950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e707109d7e867ce07c7731fb8c6f8f9ae86316cce093e6e3105edf94926ad565`

```dockerfile
```

-	Layers:
	-	`sha256:5bd90f66ef9cac306480ee43d0568132947a58f5fafa285b42f5aa8886ea4519`  
		Last Modified: Tue, 08 Jul 2025 03:01:47 GMT  
		Size: 23.9 KB (23950 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:3-alpine3.22` - linux; arm variant v7

```console
$ docker pull bash@sha256:4487e0219bd848e4b57f8118a4646e442065f19737139debfee130b9576235bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3839316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:640377bff60508e5424a01c3fcbeae58e0f94fbbed925c02ad70b373e9c4986f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 18:33:23 GMT
ENV _BASH_VERSION=3.2.57
# Fri, 30 May 2025 18:33:23 GMT
ENV _BASH_BASELINE=3.2.57
# Fri, 30 May 2025 18:33:23 GMT
ENV _BASH_BASELINE_PATCH=57
# Fri, 30 May 2025 18:33:23 GMT
ENV _BASH_LATEST_PATCH=57
# Fri, 30 May 2025 18:33:23 GMT
COPY alpine3.21.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Fri, 30 May 2025 18:33:23 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz"; 	wget -O bash.tar.gz.sig "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz.sig"; 		: "${_BASH_BASELINE_PATCH:=0}" "${_BASH_LATEST_PATCH:=0}"; 	if [ "$_BASH_LATEST_PATCH" -gt "$_BASH_BASELINE_PATCH" ]; then 		mkdir -p bash-patches; 		first="$(printf '%03d' "$(( _BASH_BASELINE_PATCH + 1 ))")"; 		last="$(printf '%03d' "$_BASH_LATEST_PATCH")"; 		majorMinor="${_BASH_VERSION%.*}"; 		for patch in $(seq -w "$first" "$last"); do 			url="https://ftp.gnu.org/gnu/bash/bash-$majorMinor-patches/bash${majorMinor//./}-$patch"; 			wget -O "bash-patches/$patch" "$url"; 			wget -O "bash-patches/$patch.sig" "$url.sig"; 		done; 	fi; 		apk add --no-cache --virtual .gpg-deps gnupg; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7C0135FB088AAF6C66C650B9BB5869F064EA74AB; 	gpg --batch --verify bash.tar.gz.sig bash.tar.gz; 	rm bash.tar.gz.sig; 	if [ -d bash-patches ]; then 		for sig in bash-patches/*.sig; do 			p="${sig%.sig}"; 			gpg --batch --verify "$sig" "$p"; 			rm "$sig"; 		done; 	fi; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apk del --no-network .gpg-deps; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	for f in config.guess config.sub; do 		wget -O "support/$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 	done; 	export CFLAGS='-Wno-error=implicit-int -Wno-error=implicit-function-declaration'; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make y.tab.c; make builtins/libbuiltins.a; 	make -j 1; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	[ "$(bash -c 'echo "${BASH_VERSION%%[^0-9.]*}"')" = "$_BASH_VERSION" ]; 	bash -c 'help' > /dev/null # buildkit
# Fri, 30 May 2025 18:33:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 30 May 2025 18:33:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 30 May 2025 18:33:23 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a34dac3a1fe5bcb39fdf21835f2890296ed658742dabbb34b23161bc76dc664d`  
		Last Modified: Fri, 06 Jun 2025 08:50:55 GMT  
		Size: 1.6 KB (1629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:271a65cce1f4c52c0a2805157bd6ac65d4e325d5268338318c73a06111c15518`  
		Last Modified: Fri, 06 Jun 2025 08:50:57 GMT  
		Size: 618.2 KB (618174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feb1cb3120d9d52e838517288cbd4bae6d68c68053cacd23de7eedb345c35b40`  
		Last Modified: Fri, 06 Jun 2025 08:50:58 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:3-alpine3.22` - unknown; unknown

```console
$ docker pull bash@sha256:93578ba77d5c581960d16e0f3e6765cc2dd15f4a7c07b201fa8c0ac4eca2057d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.9 KB (142856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:665763fd335e7506c419d984349ebdb4e2b822b9657e0d8b6f115eec8df6bdda`

```dockerfile
```

-	Layers:
	-	`sha256:92c5b2b49c2b661dcb4ffa687bfe4c9b7968f3c4f70d12d87464555e58f75245`  
		Last Modified: Fri, 06 Jun 2025 08:51:01 GMT  
		Size: 119.0 KB (119033 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6d74ae2010bfe4366ad94ef11a2ff7b827520bb5954de737311337aaf386f32`  
		Last Modified: Fri, 06 Jun 2025 08:51:03 GMT  
		Size: 23.8 KB (23823 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:3-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull bash@sha256:3cc8ea76e8d93060131aa55e3281a91b198ee53de8d6ff584f3a6fc8d342970a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4778440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb39d5e4f68bacd95c25eebe0f5affff4584a6c8c6446ed5cfe28a07b16705d1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 18:33:23 GMT
ENV _BASH_VERSION=3.2.57
# Fri, 30 May 2025 18:33:23 GMT
ENV _BASH_BASELINE=3.2.57
# Fri, 30 May 2025 18:33:23 GMT
ENV _BASH_BASELINE_PATCH=57
# Fri, 30 May 2025 18:33:23 GMT
ENV _BASH_LATEST_PATCH=57
# Fri, 30 May 2025 18:33:23 GMT
COPY alpine3.21.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Fri, 30 May 2025 18:33:23 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz"; 	wget -O bash.tar.gz.sig "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz.sig"; 		: "${_BASH_BASELINE_PATCH:=0}" "${_BASH_LATEST_PATCH:=0}"; 	if [ "$_BASH_LATEST_PATCH" -gt "$_BASH_BASELINE_PATCH" ]; then 		mkdir -p bash-patches; 		first="$(printf '%03d' "$(( _BASH_BASELINE_PATCH + 1 ))")"; 		last="$(printf '%03d' "$_BASH_LATEST_PATCH")"; 		majorMinor="${_BASH_VERSION%.*}"; 		for patch in $(seq -w "$first" "$last"); do 			url="https://ftp.gnu.org/gnu/bash/bash-$majorMinor-patches/bash${majorMinor//./}-$patch"; 			wget -O "bash-patches/$patch" "$url"; 			wget -O "bash-patches/$patch.sig" "$url.sig"; 		done; 	fi; 		apk add --no-cache --virtual .gpg-deps gnupg; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7C0135FB088AAF6C66C650B9BB5869F064EA74AB; 	gpg --batch --verify bash.tar.gz.sig bash.tar.gz; 	rm bash.tar.gz.sig; 	if [ -d bash-patches ]; then 		for sig in bash-patches/*.sig; do 			p="${sig%.sig}"; 			gpg --batch --verify "$sig" "$p"; 			rm "$sig"; 		done; 	fi; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apk del --no-network .gpg-deps; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	for f in config.guess config.sub; do 		wget -O "support/$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 	done; 	export CFLAGS='-Wno-error=implicit-int -Wno-error=implicit-function-declaration'; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make y.tab.c; make builtins/libbuiltins.a; 	make -j 1; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	[ "$(bash -c 'echo "${BASH_VERSION%%[^0-9.]*}"')" = "$_BASH_VERSION" ]; 	bash -c 'help' > /dev/null # buildkit
# Fri, 30 May 2025 18:33:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 30 May 2025 18:33:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 30 May 2025 18:33:23 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd89abcabac34468fb2bed5bf7ac1f57bd05fbdf2be16ee6b32d008ac1f3c793`  
		Last Modified: Wed, 04 Jun 2025 08:07:46 GMT  
		Size: 1.6 KB (1630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe0014e7c22df537d4e10acd70b14f7a560eab74d80fbc67d1bb25fb68575caf`  
		Last Modified: Wed, 04 Jun 2025 08:07:47 GMT  
		Size: 640.5 KB (640536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3cf35627df55490640c5de7ce6af245215a4016ca16240007d20431f7d25c0a`  
		Last Modified: Wed, 04 Jun 2025 08:07:46 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:3-alpine3.22` - unknown; unknown

```console
$ docker pull bash@sha256:6fe3496e4b08e188f3c895eeb4acb45a51c6a089baf33f534cf9f21b2349b304
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.9 KB (142920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c788bd5bf70f768e24b2b0fbb3c4d5fcddf7fb446de3e73375aaeeaefb130794`

```dockerfile
```

-	Layers:
	-	`sha256:333dfc57bfe4d1994955a4f3ff0368db3588538d70302d939c11c4f620152491`  
		Last Modified: Fri, 06 Jun 2025 08:51:14 GMT  
		Size: 119.1 KB (119061 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:667b05fa8fba1160ad2f15c6e82760d557acc0c3366503861748d3409e4a21e9`  
		Last Modified: Fri, 06 Jun 2025 08:51:15 GMT  
		Size: 23.9 KB (23859 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:3-alpine3.22` - linux; 386

```console
$ docker pull bash@sha256:420bf0bccc81683692153e206af5efdaa854ce3eab64edbfb50b340c62855f33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4256865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e1d3cd1352b1eebd737eae5ff141b410914cc1d045b71ad33705a439c0503f9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 07 Jul 2025 22:42:46 GMT
ENV _BASH_VERSION=3.2.57
# Mon, 07 Jul 2025 22:42:46 GMT
ENV _BASH_BASELINE=3.2.57
# Mon, 07 Jul 2025 22:42:46 GMT
ENV _BASH_BASELINE_PATCH=57
# Mon, 07 Jul 2025 22:42:46 GMT
ENV _BASH_LATEST_PATCH=57
# Mon, 07 Jul 2025 22:42:46 GMT
COPY alpine3.21.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Mon, 07 Jul 2025 22:42:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz"; 	wget -O bash.tar.gz.sig "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz.sig"; 		: "${_BASH_BASELINE_PATCH:=0}" "${_BASH_LATEST_PATCH:=0}"; 	if [ "$_BASH_LATEST_PATCH" -gt "$_BASH_BASELINE_PATCH" ]; then 		mkdir -p bash-patches; 		first="$(printf '%03d' "$(( _BASH_BASELINE_PATCH + 1 ))")"; 		last="$(printf '%03d' "$_BASH_LATEST_PATCH")"; 		majorMinor="${_BASH_VERSION%.*}"; 		for patch in $(seq -w "$first" "$last"); do 			url="https://ftp.gnu.org/gnu/bash/bash-$majorMinor-patches/bash${majorMinor//./}-$patch"; 			wget -O "bash-patches/$patch" "$url"; 			wget -O "bash-patches/$patch.sig" "$url.sig"; 		done; 	fi; 		apk add --no-cache --virtual .gpg-deps gnupg; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7C0135FB088AAF6C66C650B9BB5869F064EA74AB; 	gpg --batch --verify bash.tar.gz.sig bash.tar.gz; 	rm bash.tar.gz.sig; 	if [ -d bash-patches ]; then 		for sig in bash-patches/*.sig; do 			p="${sig%.sig}"; 			gpg --batch --verify "$sig" "$p"; 			rm "$sig"; 		done; 	fi; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apk del --no-network .gpg-deps; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	for f in config.guess config.sub; do 		wget -T2 -O "support/$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb" || 			wget -O "support/$f" "https://github.com/tianon/mirror-gnu-config/raw/7d3d27baf8107b630586c962c057e22149653deb/$f"; 	done; 	export CFLAGS='-Wno-error=implicit-int -Wno-error=implicit-function-declaration'; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make y.tab.c; make builtins/libbuiltins.a; 	make -j 1; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	[ "$(bash -c 'echo "${BASH_VERSION%%[^0-9.]*}"')" = "$_BASH_VERSION" ]; 	bash -c 'help' > /dev/null # buildkit
# Mon, 07 Jul 2025 22:42:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 07 Jul 2025 22:42:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 07 Jul 2025 22:42:46 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:c787620501b746b3aa9ec021f3ddb0b707572b5c68e33d73be392b9c078a4993`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 3.6 MB (3616029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b05dc73badbc3db2e65df9e97e84193491b93bec4854ad068787437612af9635`  
		Last Modified: Mon, 07 Jul 2025 22:56:41 GMT  
		Size: 1.6 KB (1630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:536d9fcc976a1740a60e7d921a976f4d9d23f85a030f1c26d8fb310f3720e89f`  
		Last Modified: Mon, 07 Jul 2025 22:56:42 GMT  
		Size: 638.9 KB (638875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:630745c729f1755d79f483f751b91c1c3da1d1955cca1f99c17eccbe5671cbac`  
		Last Modified: Mon, 07 Jul 2025 22:56:41 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:3-alpine3.22` - unknown; unknown

```console
$ docker pull bash@sha256:faa6749a343bbc9c460ef137bb1b542fbb3feacdd528948ce44a53375f031dce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.0 KB (142977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51bdcb67d24f08af55a8318960b0682062e63ca1a80dc71f85e8bfd8d26e8c70`

```dockerfile
```

-	Layers:
	-	`sha256:f1e3d67218406b5329ea9cbb5fac38bef177b78881a49fcddb8a829e8ea2704d`  
		Last Modified: Tue, 08 Jul 2025 00:01:50 GMT  
		Size: 118.9 KB (118946 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1b2a41c9954fab4692ec745b2694cd99a7b5386473d540876ef5eed3d394cba`  
		Last Modified: Tue, 08 Jul 2025 00:01:50 GMT  
		Size: 24.0 KB (24031 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:3-alpine3.22` - linux; ppc64le

```console
$ docker pull bash@sha256:bc3093177a4f4ca8406cc5b8783709dcf81c5c83e56f4961c25cdb7c878a2203
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4399333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8072ceb0bec3185ea9742c8a0bcc8f0f95d6ee4419f90c39e6cecc3d0e72bb1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-ppc64le.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 07 Jul 2025 22:42:46 GMT
ENV _BASH_VERSION=3.2.57
# Mon, 07 Jul 2025 22:42:46 GMT
ENV _BASH_BASELINE=3.2.57
# Mon, 07 Jul 2025 22:42:46 GMT
ENV _BASH_BASELINE_PATCH=57
# Mon, 07 Jul 2025 22:42:46 GMT
ENV _BASH_LATEST_PATCH=57
# Mon, 07 Jul 2025 22:42:46 GMT
COPY alpine3.21.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Mon, 07 Jul 2025 22:42:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz"; 	wget -O bash.tar.gz.sig "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz.sig"; 		: "${_BASH_BASELINE_PATCH:=0}" "${_BASH_LATEST_PATCH:=0}"; 	if [ "$_BASH_LATEST_PATCH" -gt "$_BASH_BASELINE_PATCH" ]; then 		mkdir -p bash-patches; 		first="$(printf '%03d' "$(( _BASH_BASELINE_PATCH + 1 ))")"; 		last="$(printf '%03d' "$_BASH_LATEST_PATCH")"; 		majorMinor="${_BASH_VERSION%.*}"; 		for patch in $(seq -w "$first" "$last"); do 			url="https://ftp.gnu.org/gnu/bash/bash-$majorMinor-patches/bash${majorMinor//./}-$patch"; 			wget -O "bash-patches/$patch" "$url"; 			wget -O "bash-patches/$patch.sig" "$url.sig"; 		done; 	fi; 		apk add --no-cache --virtual .gpg-deps gnupg; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7C0135FB088AAF6C66C650B9BB5869F064EA74AB; 	gpg --batch --verify bash.tar.gz.sig bash.tar.gz; 	rm bash.tar.gz.sig; 	if [ -d bash-patches ]; then 		for sig in bash-patches/*.sig; do 			p="${sig%.sig}"; 			gpg --batch --verify "$sig" "$p"; 			rm "$sig"; 		done; 	fi; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apk del --no-network .gpg-deps; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	for f in config.guess config.sub; do 		wget -T2 -O "support/$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb" || 			wget -O "support/$f" "https://github.com/tianon/mirror-gnu-config/raw/7d3d27baf8107b630586c962c057e22149653deb/$f"; 	done; 	export CFLAGS='-Wno-error=implicit-int -Wno-error=implicit-function-declaration'; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make y.tab.c; make builtins/libbuiltins.a; 	make -j 1; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	[ "$(bash -c 'echo "${BASH_VERSION%%[^0-9.]*}"')" = "$_BASH_VERSION" ]; 	bash -c 'help' > /dev/null # buildkit
# Mon, 07 Jul 2025 22:42:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 07 Jul 2025 22:42:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 07 Jul 2025 22:42:46 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:33a2433d89df7e794d1655fce70d7031d8065c9798bdc2931f7c98fcc8d310d0`  
		Last Modified: Tue, 03 Jun 2025 13:30:33 GMT  
		Size: 3.7 MB (3730187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bef457fadb369ed81499b11492b6cd5f3d0df713c37a5bcbe8dd86d5c062e72c`  
		Last Modified: Mon, 07 Jul 2025 23:28:23 GMT  
		Size: 1.6 KB (1631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4780ea2905869233b9e12bd2ade282d2f242e1da32c1580485bb04770e5bbabb`  
		Last Modified: Mon, 07 Jul 2025 23:28:23 GMT  
		Size: 667.2 KB (667184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56bfe5b5e7603fd1446308cb10cda5ead85036bbada25de4fce58dda86193359`  
		Last Modified: Mon, 07 Jul 2025 23:28:23 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:3-alpine3.22` - unknown; unknown

```console
$ docker pull bash@sha256:6dc6b3ae425451da51591d0375dd207c3f48e0267921ab1a7dce0242520a8eb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.2 KB (141205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfd2cf8e110917b1b4f3f929870a12b9c91eb1243c614d890fed4ede7f46ebe5`

```dockerfile
```

-	Layers:
	-	`sha256:04bb036f0f3bf4f1efa9ab44733321f623b96f4e19901cd7af1933ada92e7b64`  
		Last Modified: Tue, 08 Jul 2025 03:01:57 GMT  
		Size: 117.1 KB (117076 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45d1e72084c505e143f2a75a62049df3970bfc5708b6ae36b11b2b678d9a89b1`  
		Last Modified: Tue, 08 Jul 2025 03:01:58 GMT  
		Size: 24.1 KB (24129 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:3-alpine3.22` - linux; riscv64

```console
$ docker pull bash@sha256:b6fd0fb9d1bfa8f45638c36f26151e53e5b870091968d183cc255a5ed72837ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4188533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ba6a9f5a0ed3bbb7e02eb06492bc2821ae72a2b30467d04e2753edb8c32b805`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-riscv64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 07 Jul 2025 22:42:46 GMT
ENV _BASH_VERSION=3.2.57
# Mon, 07 Jul 2025 22:42:46 GMT
ENV _BASH_BASELINE=3.2.57
# Mon, 07 Jul 2025 22:42:46 GMT
ENV _BASH_BASELINE_PATCH=57
# Mon, 07 Jul 2025 22:42:46 GMT
ENV _BASH_LATEST_PATCH=57
# Mon, 07 Jul 2025 22:42:46 GMT
COPY alpine3.21.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Mon, 07 Jul 2025 22:42:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz"; 	wget -O bash.tar.gz.sig "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz.sig"; 		: "${_BASH_BASELINE_PATCH:=0}" "${_BASH_LATEST_PATCH:=0}"; 	if [ "$_BASH_LATEST_PATCH" -gt "$_BASH_BASELINE_PATCH" ]; then 		mkdir -p bash-patches; 		first="$(printf '%03d' "$(( _BASH_BASELINE_PATCH + 1 ))")"; 		last="$(printf '%03d' "$_BASH_LATEST_PATCH")"; 		majorMinor="${_BASH_VERSION%.*}"; 		for patch in $(seq -w "$first" "$last"); do 			url="https://ftp.gnu.org/gnu/bash/bash-$majorMinor-patches/bash${majorMinor//./}-$patch"; 			wget -O "bash-patches/$patch" "$url"; 			wget -O "bash-patches/$patch.sig" "$url.sig"; 		done; 	fi; 		apk add --no-cache --virtual .gpg-deps gnupg; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7C0135FB088AAF6C66C650B9BB5869F064EA74AB; 	gpg --batch --verify bash.tar.gz.sig bash.tar.gz; 	rm bash.tar.gz.sig; 	if [ -d bash-patches ]; then 		for sig in bash-patches/*.sig; do 			p="${sig%.sig}"; 			gpg --batch --verify "$sig" "$p"; 			rm "$sig"; 		done; 	fi; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apk del --no-network .gpg-deps; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	for f in config.guess config.sub; do 		wget -T2 -O "support/$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb" || 			wget -O "support/$f" "https://github.com/tianon/mirror-gnu-config/raw/7d3d27baf8107b630586c962c057e22149653deb/$f"; 	done; 	export CFLAGS='-Wno-error=implicit-int -Wno-error=implicit-function-declaration'; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make y.tab.c; make builtins/libbuiltins.a; 	make -j 1; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	[ "$(bash -c 'echo "${BASH_VERSION%%[^0-9.]*}"')" = "$_BASH_VERSION" ]; 	bash -c 'help' > /dev/null # buildkit
# Mon, 07 Jul 2025 22:42:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 07 Jul 2025 22:42:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 07 Jul 2025 22:42:46 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:a0a4beaa1960bba353066d674aa0e3378b856b09e6d3f704d1755daa5d6c1d39`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.5 MB (3513811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99fe377165a2da23958e638a8d442c8d25e96d22abaaa8f1cdc5c6e2f68168ab`  
		Last Modified: Tue, 08 Jul 2025 00:07:15 GMT  
		Size: 1.6 KB (1630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57724f0e717343ccf4cea761c1e6e7669a6eecd099c1bc9e28bdb9fd2bf4f412`  
		Last Modified: Tue, 08 Jul 2025 00:07:18 GMT  
		Size: 672.8 KB (672755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9638df15febcb33d4eddf05dc4ed5d9974f3dc051f3844c0421416b3f4a223a5`  
		Last Modified: Tue, 08 Jul 2025 00:07:16 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:3-alpine3.22` - unknown; unknown

```console
$ docker pull bash@sha256:e1fbfb3b0350859b11149b3c36d0271eb5f7f066e73f4e6ef0ba7899779d57c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.2 KB (141201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0a0942a304d80a2b54e142b4f8d19f630276bd7e4b67499c47d0c99e3a73d71`

```dockerfile
```

-	Layers:
	-	`sha256:37c57d9e087c1479b42d18c209e063dee018ff9202f03c5adfef33b5cf2a0b8c`  
		Last Modified: Tue, 08 Jul 2025 03:02:01 GMT  
		Size: 117.1 KB (117072 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad3b6be9a1b18aef1e1adc8de4c18c134d35cefe76329ff7ab20874a70369011`  
		Last Modified: Tue, 08 Jul 2025 03:02:02 GMT  
		Size: 24.1 KB (24129 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:3-alpine3.22` - linux; s390x

```console
$ docker pull bash@sha256:a588b05eda0c71a72dd3c1e87b6660df5925f943a5ee0e731c49956b9aea951f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4339035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ae00de28a367c99ec5f7a5344536ed76ede20da08b45f556c4ff44ceccbf338`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-s390x.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 18:33:23 GMT
ENV _BASH_VERSION=3.2.57
# Fri, 30 May 2025 18:33:23 GMT
ENV _BASH_BASELINE=3.2.57
# Fri, 30 May 2025 18:33:23 GMT
ENV _BASH_BASELINE_PATCH=57
# Fri, 30 May 2025 18:33:23 GMT
ENV _BASH_LATEST_PATCH=57
# Fri, 30 May 2025 18:33:23 GMT
COPY alpine3.21.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Fri, 30 May 2025 18:33:23 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz"; 	wget -O bash.tar.gz.sig "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz.sig"; 		: "${_BASH_BASELINE_PATCH:=0}" "${_BASH_LATEST_PATCH:=0}"; 	if [ "$_BASH_LATEST_PATCH" -gt "$_BASH_BASELINE_PATCH" ]; then 		mkdir -p bash-patches; 		first="$(printf '%03d' "$(( _BASH_BASELINE_PATCH + 1 ))")"; 		last="$(printf '%03d' "$_BASH_LATEST_PATCH")"; 		majorMinor="${_BASH_VERSION%.*}"; 		for patch in $(seq -w "$first" "$last"); do 			url="https://ftp.gnu.org/gnu/bash/bash-$majorMinor-patches/bash${majorMinor//./}-$patch"; 			wget -O "bash-patches/$patch" "$url"; 			wget -O "bash-patches/$patch.sig" "$url.sig"; 		done; 	fi; 		apk add --no-cache --virtual .gpg-deps gnupg; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7C0135FB088AAF6C66C650B9BB5869F064EA74AB; 	gpg --batch --verify bash.tar.gz.sig bash.tar.gz; 	rm bash.tar.gz.sig; 	if [ -d bash-patches ]; then 		for sig in bash-patches/*.sig; do 			p="${sig%.sig}"; 			gpg --batch --verify "$sig" "$p"; 			rm "$sig"; 		done; 	fi; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apk del --no-network .gpg-deps; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	for f in config.guess config.sub; do 		wget -O "support/$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 	done; 	export CFLAGS='-Wno-error=implicit-int -Wno-error=implicit-function-declaration'; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make y.tab.c; make builtins/libbuiltins.a; 	make -j 1; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	[ "$(bash -c 'echo "${BASH_VERSION%%[^0-9.]*}"')" = "$_BASH_VERSION" ]; 	bash -c 'help' > /dev/null # buildkit
# Fri, 30 May 2025 18:33:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 30 May 2025 18:33:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 30 May 2025 18:33:23 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:47a70fdc8ac4c1273de626dc7710d3e19cfd5b9f3e10cfc4b14602bdfffbffe1`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.6 MB (3647529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:824b661d575d1e67daf2a43fe369b18d0bc9206959e8a78b756295506f282c94`  
		Last Modified: Fri, 06 Jun 2025 08:51:57 GMT  
		Size: 1.6 KB (1627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43f35d008b6834790d30154b63b5406b2bb781bfd0133b477401bf928de1d078`  
		Last Modified: Fri, 06 Jun 2025 08:52:00 GMT  
		Size: 689.5 KB (689542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eddefbed925ac58756701e79c8a85ca5e364a3a0011fd804afa8b03b36f71c7`  
		Last Modified: Fri, 06 Jun 2025 08:52:01 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:3-alpine3.22` - unknown; unknown

```console
$ docker pull bash@sha256:66a98257a1bb598c3f0efe0af95b0d5a88a1e87d39ced4c17aecb9be0c7ddd8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.8 KB (140761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afa03f7301fb409c2a837e780f0ae3f44eb4ffb723baa2484442775e75198ae9`

```dockerfile
```

-	Layers:
	-	`sha256:a5c32d94367e000c94e53bc40daaa7e054a0a9516bf1ee9ae008c0ce794ca870`  
		Last Modified: Fri, 06 Jun 2025 08:52:05 GMT  
		Size: 117.0 KB (117030 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45707cfc3470c605d20c96a6aff5405bbb812f08eeef68065edefb42f8b374d5`  
		Last Modified: Fri, 06 Jun 2025 08:52:06 GMT  
		Size: 23.7 KB (23731 bytes)  
		MIME: application/vnd.in-toto+json
