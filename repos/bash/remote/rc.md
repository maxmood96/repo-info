## `bash:rc`

```console
$ docker pull bash@sha256:78a6f92d33496fdda4c4e1d8aeb6ca9a0818e2de0d9b404e4b35c8c8f8b59070
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

### `bash:rc` - linux; amd64

```console
$ docker pull bash@sha256:905b4b5db42fce69f4fbc63145a1656ad4747d53eb424aa1a505784ae80637cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6590964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae785417af3b15ca61d746f1e07e5b5731ce00fb1c550886b2fd928abaab11ad`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Dec 2024 17:18:53 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Tue, 17 Dec 2024 17:18:53 GMT
CMD ["/bin/sh"]
# Tue, 17 Dec 2024 17:18:53 GMT
ENV _BASH_VERSION=5.3-beta
# Tue, 17 Dec 2024 17:18:53 GMT
ENV _BASH_BASELINE=5.3-beta
# Tue, 17 Dec 2024 17:18:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz"; 	wget -O bash.tar.gz.sig "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz.sig"; 		: "${_BASH_BASELINE_PATCH:=0}" "${_BASH_LATEST_PATCH:=0}"; 	if [ "$_BASH_LATEST_PATCH" -gt "$_BASH_BASELINE_PATCH" ]; then 		mkdir -p bash-patches; 		first="$(printf '%03d' "$(( _BASH_BASELINE_PATCH + 1 ))")"; 		last="$(printf '%03d' "$_BASH_LATEST_PATCH")"; 		majorMinor="${_BASH_VERSION%.*}"; 		for patch in $(seq -w "$first" "$last"); do 			url="https://ftp.gnu.org/gnu/bash/bash-$majorMinor-patches/bash${majorMinor//./}-$patch"; 			wget -O "bash-patches/$patch" "$url"; 			wget -O "bash-patches/$patch.sig" "$url.sig"; 		done; 	fi; 		apk add --no-cache --virtual .gpg-deps gnupg; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7C0135FB088AAF6C66C650B9BB5869F064EA74AB; 	gpg --batch --verify bash.tar.gz.sig bash.tar.gz; 	rm bash.tar.gz.sig; 	if [ -d bash-patches ]; then 		for sig in bash-patches/*.sig; do 			p="${sig%.sig}"; 			gpg --batch --verify "$sig" "$p"; 			rm "$sig"; 		done; 	fi; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apk del --no-network .gpg-deps; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	[ "$(bash -c 'echo "${BASH_VERSION%%[^0-9.]*}"')" = "${_BASH_VERSION%%-*}.0" ]; 	bash -c 'help' > /dev/null # buildkit
# Tue, 17 Dec 2024 17:18:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Dec 2024 17:18:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Dec 2024 17:18:53 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94b916e39404a6059c6d6e14602c8cd63ce6a1aed18810323ec49fb83040e431`  
		Last Modified: Fri, 14 Feb 2025 19:11:41 GMT  
		Size: 2.9 MB (2948379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e35bf4d9c5957edbfd545b864bf872bcdae76136b82be6e0901cb39d1a001dc`  
		Last Modified: Fri, 14 Feb 2025 19:11:40 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:rc` - unknown; unknown

```console
$ docker pull bash@sha256:19af037413c836b55a719e119970a570f569f3a847120de2e555338411bfc06a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.9 KB (135867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:034cb293bfd3e2254ec197d75d9dd2cef270384b95454f5a017379bbd493fc58`

```dockerfile
```

-	Layers:
	-	`sha256:02df4cf3b38f90dafaa142ab85cb0838028ab413159cbd42d8a2d308bad912b3`  
		Last Modified: Fri, 14 Feb 2025 22:06:01 GMT  
		Size: 115.5 KB (115502 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d8f993516d2ad13d42e7cdab3bc6cb2b38c17bb24e35fb6d44e67db19c13d8e`  
		Last Modified: Fri, 14 Feb 2025 22:06:01 GMT  
		Size: 20.4 KB (20365 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:rc` - linux; arm variant v6

```console
$ docker pull bash@sha256:dc3bfc060b005a78a22de7c5f4333daae9a74595bcdc08f6d062c1c1925e07c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6250893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa276ee8cbc2bc93d38326c53da6138911b453a598ad4b9e8b0ff4325e1e341e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Dec 2024 17:18:53 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Tue, 17 Dec 2024 17:18:53 GMT
CMD ["/bin/sh"]
# Tue, 17 Dec 2024 17:18:53 GMT
ENV _BASH_VERSION=5.3-beta
# Tue, 17 Dec 2024 17:18:53 GMT
ENV _BASH_BASELINE=5.3-beta
# Tue, 17 Dec 2024 17:18:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz"; 	wget -O bash.tar.gz.sig "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz.sig"; 		: "${_BASH_BASELINE_PATCH:=0}" "${_BASH_LATEST_PATCH:=0}"; 	if [ "$_BASH_LATEST_PATCH" -gt "$_BASH_BASELINE_PATCH" ]; then 		mkdir -p bash-patches; 		first="$(printf '%03d' "$(( _BASH_BASELINE_PATCH + 1 ))")"; 		last="$(printf '%03d' "$_BASH_LATEST_PATCH")"; 		majorMinor="${_BASH_VERSION%.*}"; 		for patch in $(seq -w "$first" "$last"); do 			url="https://ftp.gnu.org/gnu/bash/bash-$majorMinor-patches/bash${majorMinor//./}-$patch"; 			wget -O "bash-patches/$patch" "$url"; 			wget -O "bash-patches/$patch.sig" "$url.sig"; 		done; 	fi; 		apk add --no-cache --virtual .gpg-deps gnupg; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7C0135FB088AAF6C66C650B9BB5869F064EA74AB; 	gpg --batch --verify bash.tar.gz.sig bash.tar.gz; 	rm bash.tar.gz.sig; 	if [ -d bash-patches ]; then 		for sig in bash-patches/*.sig; do 			p="${sig%.sig}"; 			gpg --batch --verify "$sig" "$p"; 			rm "$sig"; 		done; 	fi; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apk del --no-network .gpg-deps; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	[ "$(bash -c 'echo "${BASH_VERSION%%[^0-9.]*}"')" = "${_BASH_VERSION%%-*}.0" ]; 	bash -c 'help' > /dev/null # buildkit
# Tue, 17 Dec 2024 17:18:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Dec 2024 17:18:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Dec 2024 17:18:53 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 19:24:56 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8dfa16fec4e605450726b913ba24922ce4072227250fe807501d6cdb43211ce`  
		Last Modified: Fri, 14 Feb 2025 22:06:17 GMT  
		Size: 2.9 MB (2885831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dda633d5ae4e6399418228adc7d61736ea5bfccb16bb6ef1b07f21b6fc1abff`  
		Last Modified: Fri, 14 Feb 2025 22:06:17 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:rc` - unknown; unknown

```console
$ docker pull bash@sha256:3d781392623955cbc4f05305fe5e54f80d85e209b4adeac5a3642fcce9426e8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 KB (20242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5efefe3876668d29d797ca89b081ea5eb53f021a86a5935e6c8243903860d002`

```dockerfile
```

-	Layers:
	-	`sha256:248eaa2eb2c9fa15151520c1797a3602735ce96edf03fdb770b37bf7f53aa07c`  
		Last Modified: Fri, 14 Feb 2025 22:06:02 GMT  
		Size: 20.2 KB (20242 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:rc` - linux; arm variant v7

```console
$ docker pull bash@sha256:65c22228ebeb0b4f96ad23c21089c8a3e7996a2ccd72cfa6290f902d97a3ba8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5935491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c856ee52601e677e7d94ac6aa53559f413198481c02c4eccee167f54e2a34842`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Dec 2024 17:18:53 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Tue, 17 Dec 2024 17:18:53 GMT
CMD ["/bin/sh"]
# Tue, 17 Dec 2024 17:18:53 GMT
ENV _BASH_VERSION=5.3-beta
# Tue, 17 Dec 2024 17:18:53 GMT
ENV _BASH_BASELINE=5.3-beta
# Tue, 17 Dec 2024 17:18:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz"; 	wget -O bash.tar.gz.sig "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz.sig"; 		: "${_BASH_BASELINE_PATCH:=0}" "${_BASH_LATEST_PATCH:=0}"; 	if [ "$_BASH_LATEST_PATCH" -gt "$_BASH_BASELINE_PATCH" ]; then 		mkdir -p bash-patches; 		first="$(printf '%03d' "$(( _BASH_BASELINE_PATCH + 1 ))")"; 		last="$(printf '%03d' "$_BASH_LATEST_PATCH")"; 		majorMinor="${_BASH_VERSION%.*}"; 		for patch in $(seq -w "$first" "$last"); do 			url="https://ftp.gnu.org/gnu/bash/bash-$majorMinor-patches/bash${majorMinor//./}-$patch"; 			wget -O "bash-patches/$patch" "$url"; 			wget -O "bash-patches/$patch.sig" "$url.sig"; 		done; 	fi; 		apk add --no-cache --virtual .gpg-deps gnupg; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7C0135FB088AAF6C66C650B9BB5869F064EA74AB; 	gpg --batch --verify bash.tar.gz.sig bash.tar.gz; 	rm bash.tar.gz.sig; 	if [ -d bash-patches ]; then 		for sig in bash-patches/*.sig; do 			p="${sig%.sig}"; 			gpg --batch --verify "$sig" "$p"; 			rm "$sig"; 		done; 	fi; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apk del --no-network .gpg-deps; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	[ "$(bash -c 'echo "${BASH_VERSION%%[^0-9.]*}"')" = "${_BASH_VERSION%%-*}.0" ]; 	bash -c 'help' > /dev/null # buildkit
# Tue, 17 Dec 2024 17:18:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Dec 2024 17:18:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Dec 2024 17:18:53 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 14:37:26 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:317397ced7adcb7e90ad672f5fcece6c2173825bf442b057d97f2012ef827356`  
		Last Modified: Fri, 14 Feb 2025 19:18:19 GMT  
		Size: 2.8 MB (2837033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48ea8ce80948c916896e720e46961c7df812790b7ebbccbb29738245033ae1c2`  
		Last Modified: Fri, 14 Feb 2025 19:18:18 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:rc` - unknown; unknown

```console
$ docker pull bash@sha256:6f860876bbfb0bcf41b66d52efde885a612449083688426ff3e3a345f159321e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.0 KB (136011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2872400d09196efb21b06b627d78ce6e51eb3beb3c0cfac500a41f5fc9ea7c7d`

```dockerfile
```

-	Layers:
	-	`sha256:360f87fa3b13462f0b06bbf71cf3cd0c3fd769c47a5731841ba052af94ae7779`  
		Last Modified: Fri, 14 Feb 2025 22:06:03 GMT  
		Size: 115.6 KB (115554 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7fdc71466ec7a7b1dabfff3571d756f9a527a1702a46862a45692f876e985beb`  
		Last Modified: Fri, 14 Feb 2025 22:06:04 GMT  
		Size: 20.5 KB (20457 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:rc` - linux; arm64 variant v8

```console
$ docker pull bash@sha256:da30e19217efeab5716048a389042461d9bcdb78613917525342fc7bd9886854
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7025709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b6d3b137241566b1774fc5a579b19608778ce1bb1437df9e7dbf7e141b3daa0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Dec 2024 17:18:53 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Tue, 17 Dec 2024 17:18:53 GMT
CMD ["/bin/sh"]
# Tue, 17 Dec 2024 17:18:53 GMT
ENV _BASH_VERSION=5.3-beta
# Tue, 17 Dec 2024 17:18:53 GMT
ENV _BASH_BASELINE=5.3-beta
# Tue, 17 Dec 2024 17:18:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz"; 	wget -O bash.tar.gz.sig "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz.sig"; 		: "${_BASH_BASELINE_PATCH:=0}" "${_BASH_LATEST_PATCH:=0}"; 	if [ "$_BASH_LATEST_PATCH" -gt "$_BASH_BASELINE_PATCH" ]; then 		mkdir -p bash-patches; 		first="$(printf '%03d' "$(( _BASH_BASELINE_PATCH + 1 ))")"; 		last="$(printf '%03d' "$_BASH_LATEST_PATCH")"; 		majorMinor="${_BASH_VERSION%.*}"; 		for patch in $(seq -w "$first" "$last"); do 			url="https://ftp.gnu.org/gnu/bash/bash-$majorMinor-patches/bash${majorMinor//./}-$patch"; 			wget -O "bash-patches/$patch" "$url"; 			wget -O "bash-patches/$patch.sig" "$url.sig"; 		done; 	fi; 		apk add --no-cache --virtual .gpg-deps gnupg; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7C0135FB088AAF6C66C650B9BB5869F064EA74AB; 	gpg --batch --verify bash.tar.gz.sig bash.tar.gz; 	rm bash.tar.gz.sig; 	if [ -d bash-patches ]; then 		for sig in bash-patches/*.sig; do 			p="${sig%.sig}"; 			gpg --batch --verify "$sig" "$p"; 			rm "$sig"; 		done; 	fi; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apk del --no-network .gpg-deps; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	[ "$(bash -c 'echo "${BASH_VERSION%%[^0-9.]*}"')" = "${_BASH_VERSION%%-*}.0" ]; 	bash -c 'help' > /dev/null # buildkit
# Tue, 17 Dec 2024 17:18:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Dec 2024 17:18:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Dec 2024 17:18:53 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b273ad184527ce65ec3de813a054915bd0281918d5ebda405648219f08f4917`  
		Last Modified: Wed, 08 Jan 2025 18:09:51 GMT  
		Size: 3.0 MB (3033019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52a3ea0480d5340d72d789680d43f7666c904bcd269cfae10d54151f8d4f6194`  
		Last Modified: Wed, 08 Jan 2025 18:09:51 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:rc` - unknown; unknown

```console
$ docker pull bash@sha256:f3df00651d48798cd4894c9e257e00ee5edc67d0fe76604784537e7996e5fd60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.1 KB (136069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33402129a9ac58cae35cc82086e853d1e822ed51ae46403f6eb3fa0bc873d931`

```dockerfile
```

-	Layers:
	-	`sha256:a4aa280e620a725080c9e69cc85170864f28499ce1d00026ea19e3d542916132`  
		Last Modified: Fri, 14 Feb 2025 22:06:05 GMT  
		Size: 115.6 KB (115576 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ad275150951b1e8a12518729dfb7bb17f3d05cb21434eff6df6c99ad794fe69`  
		Last Modified: Fri, 14 Feb 2025 22:06:05 GMT  
		Size: 20.5 KB (20493 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:rc` - linux; 386

```console
$ docker pull bash@sha256:7fec9d9ceb1b0022b7a631e680e2b6e45b9588a8f0451f8355a3d6093dd57a1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6338722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac232e6cad7a77c92977151bbc4b7b6fe6fbe5e6b6952601cecfa884d9f3c6a1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Dec 2024 17:18:53 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Tue, 17 Dec 2024 17:18:53 GMT
CMD ["/bin/sh"]
# Tue, 17 Dec 2024 17:18:53 GMT
ENV _BASH_VERSION=5.3-beta
# Tue, 17 Dec 2024 17:18:53 GMT
ENV _BASH_BASELINE=5.3-beta
# Tue, 17 Dec 2024 17:18:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz"; 	wget -O bash.tar.gz.sig "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz.sig"; 		: "${_BASH_BASELINE_PATCH:=0}" "${_BASH_LATEST_PATCH:=0}"; 	if [ "$_BASH_LATEST_PATCH" -gt "$_BASH_BASELINE_PATCH" ]; then 		mkdir -p bash-patches; 		first="$(printf '%03d' "$(( _BASH_BASELINE_PATCH + 1 ))")"; 		last="$(printf '%03d' "$_BASH_LATEST_PATCH")"; 		majorMinor="${_BASH_VERSION%.*}"; 		for patch in $(seq -w "$first" "$last"); do 			url="https://ftp.gnu.org/gnu/bash/bash-$majorMinor-patches/bash${majorMinor//./}-$patch"; 			wget -O "bash-patches/$patch" "$url"; 			wget -O "bash-patches/$patch.sig" "$url.sig"; 		done; 	fi; 		apk add --no-cache --virtual .gpg-deps gnupg; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7C0135FB088AAF6C66C650B9BB5869F064EA74AB; 	gpg --batch --verify bash.tar.gz.sig bash.tar.gz; 	rm bash.tar.gz.sig; 	if [ -d bash-patches ]; then 		for sig in bash-patches/*.sig; do 			p="${sig%.sig}"; 			gpg --batch --verify "$sig" "$p"; 			rm "$sig"; 		done; 	fi; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apk del --no-network .gpg-deps; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	[ "$(bash -c 'echo "${BASH_VERSION%%[^0-9.]*}"')" = "${_BASH_VERSION%%-*}.0" ]; 	bash -c 'help' > /dev/null # buildkit
# Tue, 17 Dec 2024 17:18:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Dec 2024 17:18:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Dec 2024 17:18:53 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 14:38:41 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42e3ce7c106b43083bae94edce53286490ab7c6e67f20482ba760a9f5e614b9c`  
		Last Modified: Fri, 14 Feb 2025 19:12:05 GMT  
		Size: 2.9 MB (2874761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4af5b0f3a626c4acb47dc3126ad2f05926481e99ef910748214bc1c327548b2e`  
		Last Modified: Fri, 14 Feb 2025 19:12:04 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:rc` - unknown; unknown

```console
$ docker pull bash@sha256:17a12297eecd3f4d3a90190c5506aadde6052390e517758d610742b6427c5571
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.8 KB (135790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7754a6ce8971f42f9e77f7d9916cb031edaa0b26a74610f0a88ffe649ea89439`

```dockerfile
```

-	Layers:
	-	`sha256:95a76cd0d9f053fd7cc7eadd0a5ca1847aa2b975afcd73c1463e95fe4d8f9368`  
		Last Modified: Fri, 14 Feb 2025 22:06:06 GMT  
		Size: 115.5 KB (115467 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f19cb03b38d7add75637e2c64dec8bece6dad1131653c568de83c6f03738d64`  
		Last Modified: Fri, 14 Feb 2025 22:06:06 GMT  
		Size: 20.3 KB (20323 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:rc` - linux; ppc64le

```console
$ docker pull bash@sha256:ae389aafe2ebf196860178c03ce0ac4193a3c2ceb82999315b25add727d23b8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6791814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4e230c34811fde3858b19b6a69b14ff428b6416adddb2c91a029b2d620dd36a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Dec 2024 17:18:53 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Tue, 17 Dec 2024 17:18:53 GMT
CMD ["/bin/sh"]
# Tue, 17 Dec 2024 17:18:53 GMT
ENV _BASH_VERSION=5.3-beta
# Tue, 17 Dec 2024 17:18:53 GMT
ENV _BASH_BASELINE=5.3-beta
# Tue, 17 Dec 2024 17:18:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz"; 	wget -O bash.tar.gz.sig "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz.sig"; 		: "${_BASH_BASELINE_PATCH:=0}" "${_BASH_LATEST_PATCH:=0}"; 	if [ "$_BASH_LATEST_PATCH" -gt "$_BASH_BASELINE_PATCH" ]; then 		mkdir -p bash-patches; 		first="$(printf '%03d' "$(( _BASH_BASELINE_PATCH + 1 ))")"; 		last="$(printf '%03d' "$_BASH_LATEST_PATCH")"; 		majorMinor="${_BASH_VERSION%.*}"; 		for patch in $(seq -w "$first" "$last"); do 			url="https://ftp.gnu.org/gnu/bash/bash-$majorMinor-patches/bash${majorMinor//./}-$patch"; 			wget -O "bash-patches/$patch" "$url"; 			wget -O "bash-patches/$patch.sig" "$url.sig"; 		done; 	fi; 		apk add --no-cache --virtual .gpg-deps gnupg; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7C0135FB088AAF6C66C650B9BB5869F064EA74AB; 	gpg --batch --verify bash.tar.gz.sig bash.tar.gz; 	rm bash.tar.gz.sig; 	if [ -d bash-patches ]; then 		for sig in bash-patches/*.sig; do 			p="${sig%.sig}"; 			gpg --batch --verify "$sig" "$p"; 			rm "$sig"; 		done; 	fi; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apk del --no-network .gpg-deps; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	[ "$(bash -c 'echo "${BASH_VERSION%%[^0-9.]*}"')" = "${_BASH_VERSION%%-*}.0" ]; 	bash -c 'help' > /dev/null # buildkit
# Tue, 17 Dec 2024 17:18:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Dec 2024 17:18:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Dec 2024 17:18:53 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 14:38:03 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ad93b01cb3b826268821dd4b214dba009d2e6dafd44990ec9b44544d45f4936`  
		Last Modified: Fri, 14 Feb 2025 19:18:00 GMT  
		Size: 3.2 MB (3217131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b990995b80d95a4361e0f33acc3f867b623a91916f421410aa3d7c9a7657d297`  
		Last Modified: Fri, 14 Feb 2025 19:18:00 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:rc` - unknown; unknown

```console
$ docker pull bash@sha256:b61a1709ff06e20dcac4798c62f16d894775b5f440e8e0efc8aafa6280884baa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.0 KB (134018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce80feed3e8ef251d345b4611491c7696dcb9a6abb33e82a3f806550ef21f3d6`

```dockerfile
```

-	Layers:
	-	`sha256:855a8a49c945b6253d756536ec41e74a6ade2e409ca3cfa595e8622d7ada5b41`  
		Last Modified: Fri, 14 Feb 2025 22:06:08 GMT  
		Size: 113.6 KB (113597 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:891c41d1a2da5d08d4b005f7bc6879033c74aaefa35b5c6d7b1c5f077418dee4`  
		Last Modified: Fri, 14 Feb 2025 22:06:08 GMT  
		Size: 20.4 KB (20421 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:rc` - linux; riscv64

```console
$ docker pull bash@sha256:76826201d542bbcec5fa31314416f8273b852334089760b703961c41a65fe316
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6251359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bac5cc482fc1b7d5fd6dadf55aca260c0a1e1a1997679c57e8238cb0a6c42af`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Dec 2024 17:18:53 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
# Tue, 17 Dec 2024 17:18:53 GMT
CMD ["/bin/sh"]
# Tue, 17 Dec 2024 17:18:53 GMT
ENV _BASH_VERSION=5.3-beta
# Tue, 17 Dec 2024 17:18:53 GMT
ENV _BASH_BASELINE=5.3-beta
# Tue, 17 Dec 2024 17:18:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz"; 	wget -O bash.tar.gz.sig "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz.sig"; 		: "${_BASH_BASELINE_PATCH:=0}" "${_BASH_LATEST_PATCH:=0}"; 	if [ "$_BASH_LATEST_PATCH" -gt "$_BASH_BASELINE_PATCH" ]; then 		mkdir -p bash-patches; 		first="$(printf '%03d' "$(( _BASH_BASELINE_PATCH + 1 ))")"; 		last="$(printf '%03d' "$_BASH_LATEST_PATCH")"; 		majorMinor="${_BASH_VERSION%.*}"; 		for patch in $(seq -w "$first" "$last"); do 			url="https://ftp.gnu.org/gnu/bash/bash-$majorMinor-patches/bash${majorMinor//./}-$patch"; 			wget -O "bash-patches/$patch" "$url"; 			wget -O "bash-patches/$patch.sig" "$url.sig"; 		done; 	fi; 		apk add --no-cache --virtual .gpg-deps gnupg; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7C0135FB088AAF6C66C650B9BB5869F064EA74AB; 	gpg --batch --verify bash.tar.gz.sig bash.tar.gz; 	rm bash.tar.gz.sig; 	if [ -d bash-patches ]; then 		for sig in bash-patches/*.sig; do 			p="${sig%.sig}"; 			gpg --batch --verify "$sig" "$p"; 			rm "$sig"; 		done; 	fi; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apk del --no-network .gpg-deps; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	[ "$(bash -c 'echo "${BASH_VERSION%%[^0-9.]*}"')" = "${_BASH_VERSION%%-*}.0" ]; 	bash -c 'help' > /dev/null # buildkit
# Tue, 17 Dec 2024 17:18:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Dec 2024 17:18:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Dec 2024 17:18:53 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:7df33f7ad8beb367ac09bdd1b2f220db3ee2bbdda14a6310d1340e5628b5ba88`  
		Last Modified: Fri, 14 Feb 2025 19:25:43 GMT  
		Size: 3.4 MB (3351439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9926e43a65f547073ffc0110423dc953aef08297e709b7ce928df9bb19898c95`  
		Last Modified: Fri, 14 Feb 2025 19:32:14 GMT  
		Size: 2.9 MB (2899581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:448eca4cdd8230bc8d4c44d664d391ca168c1290069212c9bdad9c86f1f44a15`  
		Last Modified: Fri, 14 Feb 2025 19:32:13 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:rc` - unknown; unknown

```console
$ docker pull bash@sha256:2b176053e512daa878ceb9b267a09289b4c2bc3286da03e8b0f0fa459f1a976a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.0 KB (134014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38e6a423caf5f743f1ba7e0861d1d822bfc51479d649eb45489a8be454c446cf`

```dockerfile
```

-	Layers:
	-	`sha256:bc76ada99e30c1385974d3cee3862eaf4157454f54f29958a40a83c02b137dc2`  
		Last Modified: Fri, 14 Feb 2025 22:06:09 GMT  
		Size: 113.6 KB (113593 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa0c09bb9525d221cb92abbe35ec6e9d879a0ccb0f6c73f3b06eaedeb199536c`  
		Last Modified: Fri, 14 Feb 2025 22:06:10 GMT  
		Size: 20.4 KB (20421 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:rc` - linux; s390x

```console
$ docker pull bash@sha256:da965528ddc4b053c4a016f1ed8149fd2b3226b7680d5cdf9e31f40c276d9f29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6510882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aefad94bfd2c745193f500778cf716e2cfbb28cf2a2b79cac8bf7dd5ffdf1eb2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Dec 2024 17:18:53 GMT
ADD alpine-minirootfs-3.21.2-s390x.tar.gz / # buildkit
# Tue, 17 Dec 2024 17:18:53 GMT
CMD ["/bin/sh"]
# Tue, 17 Dec 2024 17:18:53 GMT
ENV _BASH_VERSION=5.3-beta
# Tue, 17 Dec 2024 17:18:53 GMT
ENV _BASH_BASELINE=5.3-beta
# Tue, 17 Dec 2024 17:18:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz"; 	wget -O bash.tar.gz.sig "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz.sig"; 		: "${_BASH_BASELINE_PATCH:=0}" "${_BASH_LATEST_PATCH:=0}"; 	if [ "$_BASH_LATEST_PATCH" -gt "$_BASH_BASELINE_PATCH" ]; then 		mkdir -p bash-patches; 		first="$(printf '%03d' "$(( _BASH_BASELINE_PATCH + 1 ))")"; 		last="$(printf '%03d' "$_BASH_LATEST_PATCH")"; 		majorMinor="${_BASH_VERSION%.*}"; 		for patch in $(seq -w "$first" "$last"); do 			url="https://ftp.gnu.org/gnu/bash/bash-$majorMinor-patches/bash${majorMinor//./}-$patch"; 			wget -O "bash-patches/$patch" "$url"; 			wget -O "bash-patches/$patch.sig" "$url.sig"; 		done; 	fi; 		apk add --no-cache --virtual .gpg-deps gnupg; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7C0135FB088AAF6C66C650B9BB5869F064EA74AB; 	gpg --batch --verify bash.tar.gz.sig bash.tar.gz; 	rm bash.tar.gz.sig; 	if [ -d bash-patches ]; then 		for sig in bash-patches/*.sig; do 			p="${sig%.sig}"; 			gpg --batch --verify "$sig" "$p"; 			rm "$sig"; 		done; 	fi; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apk del --no-network .gpg-deps; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	[ "$(bash -c 'echo "${BASH_VERSION%%[^0-9.]*}"')" = "${_BASH_VERSION%%-*}.0" ]; 	bash -c 'help' > /dev/null # buildkit
# Tue, 17 Dec 2024 17:18:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Dec 2024 17:18:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Dec 2024 17:18:53 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:b2af93686f9384c40cfe861d7173877bb2ee1675c3ee70181799693c34c8722f`  
		Last Modified: Tue, 14 Jan 2025 20:34:39 GMT  
		Size: 3.5 MB (3466867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5a512db8e193fd67451774e886d908de9b92f451414108487f2bea2902ec6c2`  
		Last Modified: Wed, 08 Jan 2025 17:59:20 GMT  
		Size: 3.0 MB (3043679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13b561053cec229f997979f74e2ca666fba7149c108b5e4695bb57c6652cc740`  
		Last Modified: Wed, 08 Jan 2025 17:59:20 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:rc` - unknown; unknown

```console
$ docker pull bash@sha256:cca568c4bb8ef7b869dd800239b92958f8f01a3b4e284c3dbc97e627a2343689
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.9 KB (133910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5cfd05fc65aedcc72b6b2c923687265bc41fec84f6539caee2e3ff1e30e9446`

```dockerfile
```

-	Layers:
	-	`sha256:28bff7c0d10c76cbd3521b6ed271642ee1d10982d82e6e42b32e8e80f90a86a7`  
		Last Modified: Fri, 14 Feb 2025 22:06:11 GMT  
		Size: 113.5 KB (113545 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7c4a62c294bd1ba5588ebbcb4f2aff77795784fc90064210848305bc52d32db`  
		Last Modified: Fri, 14 Feb 2025 22:06:11 GMT  
		Size: 20.4 KB (20365 bytes)  
		MIME: application/vnd.in-toto+json
