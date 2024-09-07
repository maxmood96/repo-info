## `bash:4-alpine3.20`

```console
$ docker pull bash@sha256:83e1ff15d9735b3ad8b15e6a8def9deb6bdd59003383e69f8f54603c83d55061
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

### `bash:4-alpine3.20` - linux; amd64

```console
$ docker pull bash@sha256:eb95cb12ece746d98b96d9765e464206ac3a9b7d0e4602e36c9ee45999613bf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5968892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24bf5797062779fadb69b91ec53ae486883b4fa5aca1d51b69e4873d4bfeb51e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 May 2024 19:24:23 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Wed, 22 May 2024 19:24:23 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 19:24:23 GMT
ENV _BASH_VERSION=4.4.23
# Wed, 22 May 2024 19:24:23 GMT
ENV _BASH_BASELINE=4.4.18
# Wed, 22 May 2024 19:24:23 GMT
ENV _BASH_BASELINE_PATCH=18
# Wed, 22 May 2024 19:24:23 GMT
ENV _BASH_LATEST_PATCH=23
# Wed, 22 May 2024 19:24:23 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz"; 	wget -O bash.tar.gz.sig "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz.sig"; 		: "${_BASH_BASELINE_PATCH:=0}" "${_BASH_LATEST_PATCH:=0}"; 	if [ "$_BASH_LATEST_PATCH" -gt "$_BASH_BASELINE_PATCH" ]; then 		mkdir -p bash-patches; 		first="$(printf '%03d' "$(( _BASH_BASELINE_PATCH + 1 ))")"; 		last="$(printf '%03d' "$_BASH_LATEST_PATCH")"; 		majorMinor="${_BASH_VERSION%.*}"; 		for patch in $(seq -w "$first" "$last"); do 			url="https://ftp.gnu.org/gnu/bash/bash-$majorMinor-patches/bash${majorMinor//./}-$patch"; 			wget -O "bash-patches/$patch" "$url"; 			wget -O "bash-patches/$patch.sig" "$url.sig"; 		done; 	fi; 		apk add --no-cache --virtual .gpg-deps gnupg; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7C0135FB088AAF6C66C650B9BB5869F064EA74AB; 	gpg --batch --verify bash.tar.gz.sig bash.tar.gz; 	rm bash.tar.gz.sig; 	if [ -d bash-patches ]; then 		for sig in bash-patches/*.sig; do 			p="${sig%.sig}"; 			gpg --batch --verify "$sig" "$p"; 			rm "$sig"; 		done; 	fi; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apk del --no-network .gpg-deps; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	for f in config.guess config.sub; do 		wget -O "support/$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 	done; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	[ "$(bash -c 'echo "${BASH_VERSION%%[^0-9.]*}"')" = "$_BASH_VERSION" ]; 	bash -c 'help' > /dev/null # buildkit
# Wed, 22 May 2024 19:24:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 May 2024 19:24:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 May 2024 19:24:23 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83846b88effab0ba75b91ca098f6448ad6cf82aceb3cdcea05b3686baaaf6121`  
		Last Modified: Fri, 06 Sep 2024 23:16:10 GMT  
		Size: 2.3 MB (2344752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:838e5908b25589ce0dce62ec94f78782bb8fb82ce9dfd223f850f11276be79d7`  
		Last Modified: Fri, 06 Sep 2024 23:16:10 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:4-alpine3.20` - unknown; unknown

```console
$ docker pull bash@sha256:8262a6d9107a4ea1802eae09b2c6bee672636bc5329da4ae61938a696f00d2ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.3 KB (131339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06254db9133b8781307f404eec590752d6ad8852528b698bf34f98b2d765ca8c`

```dockerfile
```

-	Layers:
	-	`sha256:1bcc734dc97deadd9a3daf67bf1fb5048dc5685a280e25156aa426dcbf2b1c35`  
		Last Modified: Fri, 06 Sep 2024 23:16:09 GMT  
		Size: 110.4 KB (110435 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5fb03b44867174d069f220a3a0f1e0ba3d9dbf8fe68d79ff36dbe2034fd4311a`  
		Last Modified: Fri, 06 Sep 2024 23:16:10 GMT  
		Size: 20.9 KB (20904 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:4-alpine3.20` - linux; arm variant v6

```console
$ docker pull bash@sha256:78ffc323371815413a6f1f7a9f452e01eb73047d105040ddae80d1c79a518bb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5667643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:090b9cbdcbee853b14f3fc70753947a3cb53d1b60464da1e81f2e244113d0564`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 May 2024 19:24:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Wed, 22 May 2024 19:24:23 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 19:24:23 GMT
ENV _BASH_VERSION=4.4.23
# Wed, 22 May 2024 19:24:23 GMT
ENV _BASH_BASELINE=4.4.18
# Wed, 22 May 2024 19:24:23 GMT
ENV _BASH_BASELINE_PATCH=18
# Wed, 22 May 2024 19:24:23 GMT
ENV _BASH_LATEST_PATCH=23
# Wed, 22 May 2024 19:24:23 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz"; 	wget -O bash.tar.gz.sig "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz.sig"; 		: "${_BASH_BASELINE_PATCH:=0}" "${_BASH_LATEST_PATCH:=0}"; 	if [ "$_BASH_LATEST_PATCH" -gt "$_BASH_BASELINE_PATCH" ]; then 		mkdir -p bash-patches; 		first="$(printf '%03d' "$(( _BASH_BASELINE_PATCH + 1 ))")"; 		last="$(printf '%03d' "$_BASH_LATEST_PATCH")"; 		majorMinor="${_BASH_VERSION%.*}"; 		for patch in $(seq -w "$first" "$last"); do 			url="https://ftp.gnu.org/gnu/bash/bash-$majorMinor-patches/bash${majorMinor//./}-$patch"; 			wget -O "bash-patches/$patch" "$url"; 			wget -O "bash-patches/$patch.sig" "$url.sig"; 		done; 	fi; 		apk add --no-cache --virtual .gpg-deps gnupg; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7C0135FB088AAF6C66C650B9BB5869F064EA74AB; 	gpg --batch --verify bash.tar.gz.sig bash.tar.gz; 	rm bash.tar.gz.sig; 	if [ -d bash-patches ]; then 		for sig in bash-patches/*.sig; do 			p="${sig%.sig}"; 			gpg --batch --verify "$sig" "$p"; 			rm "$sig"; 		done; 	fi; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apk del --no-network .gpg-deps; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	for f in config.guess config.sub; do 		wget -O "support/$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 	done; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	[ "$(bash -c 'echo "${BASH_VERSION%%[^0-9.]*}"')" = "$_BASH_VERSION" ]; 	bash -c 'help' > /dev/null # buildkit
# Wed, 22 May 2024 19:24:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 May 2024 19:24:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 May 2024 19:24:23 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c3703d9c2644797e8fed4d65660a276a8cea6fdccc845fc533aa235981e5808`  
		Last Modified: Sat, 07 Sep 2024 01:02:16 GMT  
		Size: 2.3 MB (2300804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beaee2f95624517ba779a4129db383bb6945a94786f80922e838b26ad7a5c98c`  
		Last Modified: Sat, 07 Sep 2024 01:02:16 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:4-alpine3.20` - unknown; unknown

```console
$ docker pull bash@sha256:50b07f0aedd1bade74090dfb6a55dc6e19d26e751db6ad3a119c4e26f4c72739
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7667d68ec1cbc193adbf5b3469331309674bae3f3cff83e4f0bff1d1c4d6c468`

```dockerfile
```

-	Layers:
	-	`sha256:ce8b9259ff9c8ecc2f35b8a4197a19fa3e3b69a87f7abbfded73eb5db5fe36de`  
		Last Modified: Sat, 07 Sep 2024 01:02:16 GMT  
		Size: 20.8 KB (20771 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:4-alpine3.20` - linux; arm variant v7

```console
$ docker pull bash@sha256:96d5f19a91f2cf8c6514ddf0e95e268297295533e0e414b3d37b743a8275b1eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5349360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcd8cf2176b14784289e2bf136fb1e50e4d8c9651c6b7e200b465a926d773985`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 May 2024 19:24:23 GMT
ADD file:816da1ff7b962e1f52c650dfd66caeb2b88f3ab9fadc249c30f86ebe5372538c in / 
# Wed, 22 May 2024 19:24:23 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 19:24:23 GMT
ENV _BASH_VERSION=4.4.23
# Wed, 22 May 2024 19:24:23 GMT
ENV _BASH_BASELINE=4.4.18
# Wed, 22 May 2024 19:24:23 GMT
ENV _BASH_BASELINE_PATCH=18
# Wed, 22 May 2024 19:24:23 GMT
ENV _BASH_LATEST_PATCH=23
# Wed, 22 May 2024 19:24:23 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz"; 	wget -O bash.tar.gz.sig "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz.sig"; 		: "${_BASH_BASELINE_PATCH:=0}" "${_BASH_LATEST_PATCH:=0}"; 	if [ "$_BASH_LATEST_PATCH" -gt "$_BASH_BASELINE_PATCH" ]; then 		mkdir -p bash-patches; 		first="$(printf '%03d' "$(( _BASH_BASELINE_PATCH + 1 ))")"; 		last="$(printf '%03d' "$_BASH_LATEST_PATCH")"; 		majorMinor="${_BASH_VERSION%.*}"; 		for patch in $(seq -w "$first" "$last"); do 			url="https://ftp.gnu.org/gnu/bash/bash-$majorMinor-patches/bash${majorMinor//./}-$patch"; 			wget -O "bash-patches/$patch" "$url"; 			wget -O "bash-patches/$patch.sig" "$url.sig"; 		done; 	fi; 		apk add --no-cache --virtual .gpg-deps gnupg; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7C0135FB088AAF6C66C650B9BB5869F064EA74AB; 	gpg --batch --verify bash.tar.gz.sig bash.tar.gz; 	rm bash.tar.gz.sig; 	if [ -d bash-patches ]; then 		for sig in bash-patches/*.sig; do 			p="${sig%.sig}"; 			gpg --batch --verify "$sig" "$p"; 			rm "$sig"; 		done; 	fi; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apk del --no-network .gpg-deps; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	for f in config.guess config.sub; do 		wget -O "support/$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 	done; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	[ "$(bash -c 'echo "${BASH_VERSION%%[^0-9.]*}"')" = "$_BASH_VERSION" ]; 	bash -c 'help' > /dev/null # buildkit
# Wed, 22 May 2024 19:24:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 May 2024 19:24:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 May 2024 19:24:23 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:9c6652a37da7fb600faac56897745bdde89a4f9bd260a082b6bf4a0d173b5906`  
		Last Modified: Mon, 22 Jul 2024 22:00:23 GMT  
		Size: 3.1 MB (3094960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4476d56a8e3852c2ed402e6985ea4fd67abc7384a0aeff4be93ceab6db02581`  
		Last Modified: Tue, 23 Jul 2024 11:37:55 GMT  
		Size: 2.3 MB (2254062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:967d369315cca5cf1ef04b76fe8f46b21339897ee0fe72af6c52e09d8ac5d941`  
		Last Modified: Tue, 23 Jul 2024 11:37:55 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:4-alpine3.20` - unknown; unknown

```console
$ docker pull bash@sha256:8d2fa8d6c4911f2d3083988c224822a231934232d989e0fb7edfdc5954152364
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.5 KB (131477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1714f6c262638b4eda093ec480391ca09db938e6363c8f3580821c07588fb184`

```dockerfile
```

-	Layers:
	-	`sha256:3e9706d9cf6e3c19223388ec3308a3ecc83b3ec8f255ea3a368c9cd123b50569`  
		Last Modified: Tue, 23 Jul 2024 11:37:55 GMT  
		Size: 110.5 KB (110487 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:523d3550bec44c52f5e53902fbfa195c1d6f5f1fbbb48cac6bcd7d768790e957`  
		Last Modified: Tue, 23 Jul 2024 11:37:55 GMT  
		Size: 21.0 KB (20990 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:4-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull bash@sha256:80646ea9ae54446e263e5f9ee005981d717c6572388c34eda1e35abe1d52b05d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6494189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:986182d4e59404b01b1381f904bbe54ca4a368560ceb26de31dc26ab31e9ac53`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 May 2024 19:24:23 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Wed, 22 May 2024 19:24:23 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 19:24:23 GMT
ENV _BASH_VERSION=4.4.23
# Wed, 22 May 2024 19:24:23 GMT
ENV _BASH_BASELINE=4.4.18
# Wed, 22 May 2024 19:24:23 GMT
ENV _BASH_BASELINE_PATCH=18
# Wed, 22 May 2024 19:24:23 GMT
ENV _BASH_LATEST_PATCH=23
# Wed, 22 May 2024 19:24:23 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz"; 	wget -O bash.tar.gz.sig "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz.sig"; 		: "${_BASH_BASELINE_PATCH:=0}" "${_BASH_LATEST_PATCH:=0}"; 	if [ "$_BASH_LATEST_PATCH" -gt "$_BASH_BASELINE_PATCH" ]; then 		mkdir -p bash-patches; 		first="$(printf '%03d' "$(( _BASH_BASELINE_PATCH + 1 ))")"; 		last="$(printf '%03d' "$_BASH_LATEST_PATCH")"; 		majorMinor="${_BASH_VERSION%.*}"; 		for patch in $(seq -w "$first" "$last"); do 			url="https://ftp.gnu.org/gnu/bash/bash-$majorMinor-patches/bash${majorMinor//./}-$patch"; 			wget -O "bash-patches/$patch" "$url"; 			wget -O "bash-patches/$patch.sig" "$url.sig"; 		done; 	fi; 		apk add --no-cache --virtual .gpg-deps gnupg; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7C0135FB088AAF6C66C650B9BB5869F064EA74AB; 	gpg --batch --verify bash.tar.gz.sig bash.tar.gz; 	rm bash.tar.gz.sig; 	if [ -d bash-patches ]; then 		for sig in bash-patches/*.sig; do 			p="${sig%.sig}"; 			gpg --batch --verify "$sig" "$p"; 			rm "$sig"; 		done; 	fi; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apk del --no-network .gpg-deps; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	for f in config.guess config.sub; do 		wget -O "support/$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 	done; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	[ "$(bash -c 'echo "${BASH_VERSION%%[^0-9.]*}"')" = "$_BASH_VERSION" ]; 	bash -c 'help' > /dev/null # buildkit
# Wed, 22 May 2024 19:24:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 May 2024 19:24:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 May 2024 19:24:23 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dc1074f08283c978636f45e8b9f77351f0aad32a3e4ac0c204107fe7b03b21d`  
		Last Modified: Tue, 23 Jul 2024 11:23:54 GMT  
		Size: 2.4 MB (2406919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3ca5aa26fd7bb6038a5b6f9280a4fb2368145de6de9e266dc245d90f6ffd436`  
		Last Modified: Tue, 23 Jul 2024 11:23:53 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:4-alpine3.20` - unknown; unknown

```console
$ docker pull bash@sha256:41846d9c4d21be108d75fdc11e80b322918277bb0bf3b83bdcdcd1bed9271516
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.7 KB (131743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6eaddb7546cb540a65d5f090b54d4487684ca3d9a6e3b47126e150350a96a79`

```dockerfile
```

-	Layers:
	-	`sha256:07c5a86b313564c5bd40c5876baab7cf6eb67c6a17631167a2232ff2db3943d6`  
		Last Modified: Tue, 23 Jul 2024 11:23:53 GMT  
		Size: 110.5 KB (110515 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a61c33d7c91a891e7e791c49ca6cf68a033e67b553737423aa84ffed46c1ff0`  
		Last Modified: Tue, 23 Jul 2024 11:23:53 GMT  
		Size: 21.2 KB (21228 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:4-alpine3.20` - linux; 386

```console
$ docker pull bash@sha256:76551f9f0b9a78c232783aaa1cf0c2d205da0c366bceef22cbed08fdbe348ea7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5775375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b96667f56cc535c8b329a3e75495c4cd7ded05172207c1a73789c24a020f825`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 May 2024 19:24:23 GMT
ADD file:00e6c22c1917031dd97c411814ae384c25a7f2bb91890494a73ea34f3c168453 in / 
# Wed, 22 May 2024 19:24:23 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 19:24:23 GMT
ENV _BASH_VERSION=4.4.23
# Wed, 22 May 2024 19:24:23 GMT
ENV _BASH_BASELINE=4.4.18
# Wed, 22 May 2024 19:24:23 GMT
ENV _BASH_BASELINE_PATCH=18
# Wed, 22 May 2024 19:24:23 GMT
ENV _BASH_LATEST_PATCH=23
# Wed, 22 May 2024 19:24:23 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz"; 	wget -O bash.tar.gz.sig "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz.sig"; 		: "${_BASH_BASELINE_PATCH:=0}" "${_BASH_LATEST_PATCH:=0}"; 	if [ "$_BASH_LATEST_PATCH" -gt "$_BASH_BASELINE_PATCH" ]; then 		mkdir -p bash-patches; 		first="$(printf '%03d' "$(( _BASH_BASELINE_PATCH + 1 ))")"; 		last="$(printf '%03d' "$_BASH_LATEST_PATCH")"; 		majorMinor="${_BASH_VERSION%.*}"; 		for patch in $(seq -w "$first" "$last"); do 			url="https://ftp.gnu.org/gnu/bash/bash-$majorMinor-patches/bash${majorMinor//./}-$patch"; 			wget -O "bash-patches/$patch" "$url"; 			wget -O "bash-patches/$patch.sig" "$url.sig"; 		done; 	fi; 		apk add --no-cache --virtual .gpg-deps gnupg; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7C0135FB088AAF6C66C650B9BB5869F064EA74AB; 	gpg --batch --verify bash.tar.gz.sig bash.tar.gz; 	rm bash.tar.gz.sig; 	if [ -d bash-patches ]; then 		for sig in bash-patches/*.sig; do 			p="${sig%.sig}"; 			gpg --batch --verify "$sig" "$p"; 			rm "$sig"; 		done; 	fi; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apk del --no-network .gpg-deps; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	for f in config.guess config.sub; do 		wget -O "support/$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 	done; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	[ "$(bash -c 'echo "${BASH_VERSION%%[^0-9.]*}"')" = "$_BASH_VERSION" ]; 	bash -c 'help' > /dev/null # buildkit
# Wed, 22 May 2024 19:24:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 May 2024 19:24:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 May 2024 19:24:23 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:2689ac6c14fd48d5dbd1df1dd2d317f177e131f689c1a010922edcd778518efd`  
		Last Modified: Fri, 06 Sep 2024 22:41:47 GMT  
		Size: 3.5 MB (3469165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aae363860fc4595c76a566ba8e10ce027f651afa11f6a12128bd15e46b13d9d`  
		Last Modified: Fri, 06 Sep 2024 23:15:40 GMT  
		Size: 2.3 MB (2305872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90d72dc6d6929fee29513f995984c66655ed60f80633701a95ba258ff32c16f2`  
		Last Modified: Fri, 06 Sep 2024 23:15:40 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:4-alpine3.20` - unknown; unknown

```console
$ docker pull bash@sha256:4e010b7a4e04862f22d15a03fe095a1a14a9a319f4b9208f8c7e17b3fd630c3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.3 KB (131265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3f73c3d7cf375895fc4efab8d3367d0cddb49934be3fdcf9fea2f24fd6702e7`

```dockerfile
```

-	Layers:
	-	`sha256:75a8c11383abfcaad292a31576b1553554b56bd694fa6ddea4cc59aa21e04f0a`  
		Last Modified: Fri, 06 Sep 2024 23:15:40 GMT  
		Size: 110.4 KB (110400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5dd95b7687281fce2a6cfe6f62d77b1190a2404487752c47613f53c27bf89ca7`  
		Last Modified: Fri, 06 Sep 2024 23:15:40 GMT  
		Size: 20.9 KB (20865 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:4-alpine3.20` - linux; ppc64le

```console
$ docker pull bash@sha256:f23b60c84e91c7468c3d9817f7c158566cdfd947fef645681744f023607876e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6123200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40343bf7d09e179b97f589001349c6d4298e02d408e546d282d163bbd539015d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 May 2024 19:24:23 GMT
ADD file:9fcad21b83b7efd6ef267ba714c3ef5a8d4d2064a0bdf528cbb17d0c3388f03f in / 
# Wed, 22 May 2024 19:24:23 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 19:24:23 GMT
ENV _BASH_VERSION=4.4.23
# Wed, 22 May 2024 19:24:23 GMT
ENV _BASH_BASELINE=4.4.18
# Wed, 22 May 2024 19:24:23 GMT
ENV _BASH_BASELINE_PATCH=18
# Wed, 22 May 2024 19:24:23 GMT
ENV _BASH_LATEST_PATCH=23
# Wed, 22 May 2024 19:24:23 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz"; 	wget -O bash.tar.gz.sig "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz.sig"; 		: "${_BASH_BASELINE_PATCH:=0}" "${_BASH_LATEST_PATCH:=0}"; 	if [ "$_BASH_LATEST_PATCH" -gt "$_BASH_BASELINE_PATCH" ]; then 		mkdir -p bash-patches; 		first="$(printf '%03d' "$(( _BASH_BASELINE_PATCH + 1 ))")"; 		last="$(printf '%03d' "$_BASH_LATEST_PATCH")"; 		majorMinor="${_BASH_VERSION%.*}"; 		for patch in $(seq -w "$first" "$last"); do 			url="https://ftp.gnu.org/gnu/bash/bash-$majorMinor-patches/bash${majorMinor//./}-$patch"; 			wget -O "bash-patches/$patch" "$url"; 			wget -O "bash-patches/$patch.sig" "$url.sig"; 		done; 	fi; 		apk add --no-cache --virtual .gpg-deps gnupg; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7C0135FB088AAF6C66C650B9BB5869F064EA74AB; 	gpg --batch --verify bash.tar.gz.sig bash.tar.gz; 	rm bash.tar.gz.sig; 	if [ -d bash-patches ]; then 		for sig in bash-patches/*.sig; do 			p="${sig%.sig}"; 			gpg --batch --verify "$sig" "$p"; 			rm "$sig"; 		done; 	fi; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apk del --no-network .gpg-deps; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	for f in config.guess config.sub; do 		wget -O "support/$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 	done; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	[ "$(bash -c 'echo "${BASH_VERSION%%[^0-9.]*}"')" = "$_BASH_VERSION" ]; 	bash -c 'help' > /dev/null # buildkit
# Wed, 22 May 2024 19:24:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 May 2024 19:24:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 May 2024 19:24:23 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:6e59b4988c495782a5b0c8f8d6698931851c16c5c0fc5ef09cbb0637ade56e36`  
		Last Modified: Mon, 22 Jul 2024 21:26:52 GMT  
		Size: 3.6 MB (3571555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:804bd566bc9d160e666d17fc609eff9a6b3edfba0643783f2b7ad7bdba51127c`  
		Last Modified: Tue, 23 Jul 2024 08:18:33 GMT  
		Size: 2.6 MB (2551311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:118753d39ca18e2a4ca780ae311490ed5034316197132eee7a3c271d2d770782`  
		Last Modified: Tue, 23 Jul 2024 08:18:32 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:4-alpine3.20` - unknown; unknown

```console
$ docker pull bash@sha256:6ea82a3e5af2a398568b10909949227b4da1b63f027bcbacb4c84196a750312b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.5 KB (129481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6feaca5cc7f08d1e7c2921c041a2b5e18fe20f7f3e8d4fb042fb3e2f46a120ec`

```dockerfile
```

-	Layers:
	-	`sha256:c38c886750518a36521237d3228c096a842d9ea260ea1025df7be42fc7ee3cc1`  
		Last Modified: Tue, 23 Jul 2024 08:18:32 GMT  
		Size: 108.5 KB (108527 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8ff6c33ea52c1fa2cc729897a32c00c63e6988d198564cca7f7d92dc73f637c`  
		Last Modified: Tue, 23 Jul 2024 08:18:32 GMT  
		Size: 21.0 KB (20954 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:4-alpine3.20` - linux; riscv64

```console
$ docker pull bash@sha256:8bb521d59b87637f9065db5263e40890c59e1d67fe42132681ffa35a2d4e27d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5680573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34fdf991f4806ea1eb48037a0dacc0b6d1d6c7a5858ad2bbbc458743b8dbe69a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 May 2024 19:24:23 GMT
ADD file:cdf7088bbd70519f0f5d7b4249df34386e40f0194752f45842b3d85f2d331cf5 in / 
# Wed, 22 May 2024 19:24:23 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 19:24:23 GMT
ENV _BASH_VERSION=4.4.23
# Wed, 22 May 2024 19:24:23 GMT
ENV _BASH_BASELINE=4.4.18
# Wed, 22 May 2024 19:24:23 GMT
ENV _BASH_BASELINE_PATCH=18
# Wed, 22 May 2024 19:24:23 GMT
ENV _BASH_LATEST_PATCH=23
# Wed, 22 May 2024 19:24:23 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz"; 	wget -O bash.tar.gz.sig "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz.sig"; 		: "${_BASH_BASELINE_PATCH:=0}" "${_BASH_LATEST_PATCH:=0}"; 	if [ "$_BASH_LATEST_PATCH" -gt "$_BASH_BASELINE_PATCH" ]; then 		mkdir -p bash-patches; 		first="$(printf '%03d' "$(( _BASH_BASELINE_PATCH + 1 ))")"; 		last="$(printf '%03d' "$_BASH_LATEST_PATCH")"; 		majorMinor="${_BASH_VERSION%.*}"; 		for patch in $(seq -w "$first" "$last"); do 			url="https://ftp.gnu.org/gnu/bash/bash-$majorMinor-patches/bash${majorMinor//./}-$patch"; 			wget -O "bash-patches/$patch" "$url"; 			wget -O "bash-patches/$patch.sig" "$url.sig"; 		done; 	fi; 		apk add --no-cache --virtual .gpg-deps gnupg; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7C0135FB088AAF6C66C650B9BB5869F064EA74AB; 	gpg --batch --verify bash.tar.gz.sig bash.tar.gz; 	rm bash.tar.gz.sig; 	if [ -d bash-patches ]; then 		for sig in bash-patches/*.sig; do 			p="${sig%.sig}"; 			gpg --batch --verify "$sig" "$p"; 			rm "$sig"; 		done; 	fi; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apk del --no-network .gpg-deps; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	for f in config.guess config.sub; do 		wget -O "support/$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 	done; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	[ "$(bash -c 'echo "${BASH_VERSION%%[^0-9.]*}"')" = "$_BASH_VERSION" ]; 	bash -c 'help' > /dev/null # buildkit
# Wed, 22 May 2024 19:24:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 May 2024 19:24:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 May 2024 19:24:23 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:faf447acae27573624c0613a79c4bcf1f9bc46d29f523140352abfd3f7691282`  
		Last Modified: Mon, 22 Jul 2024 22:21:18 GMT  
		Size: 3.4 MB (3370673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9c38d7060a7197c23d1621f1019866c04260ccb4aa18eed874a97bb502a9b38`  
		Last Modified: Tue, 23 Jul 2024 17:55:59 GMT  
		Size: 2.3 MB (2309561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7a742047f79ab926eb8a193116e87b39096896df753611f8fadb9324f95c19d`  
		Last Modified: Tue, 23 Jul 2024 17:55:59 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:4-alpine3.20` - unknown; unknown

```console
$ docker pull bash@sha256:4cc02c397f6461fab3cde9a2322926f712675e80ee4907fc833b72332877ada8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.5 KB (129477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a0dddb8f16c648c0f207a718c684ed745265f14d51816fc228bfed65fda1f34`

```dockerfile
```

-	Layers:
	-	`sha256:c52f47a0d4a0f6379d4ddb23384c6e13610c8b100d9caaa875bd9f68df64a8d2`  
		Last Modified: Tue, 23 Jul 2024 17:55:59 GMT  
		Size: 108.5 KB (108523 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0663fe613c1b878f13d79da00920d1ef6a52ed32a8ba8a2ca5b757c4b6130297`  
		Last Modified: Tue, 23 Jul 2024 17:55:59 GMT  
		Size: 21.0 KB (20954 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:4-alpine3.20` - linux; s390x

```console
$ docker pull bash@sha256:18a806437bf3269e3686ddef0b2eea5418fbe7617a353971f418856883f7f748
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5885236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:945bfd7a535c6d45a24a14e8506d446ae5e66d4c9a0b42528d9af8b23af4efa5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 May 2024 19:24:23 GMT
ADD file:ba2637314e600db5a647501cf1ab287c5f51de1627c13bc1d82aa48925a3dd78 in / 
# Wed, 22 May 2024 19:24:23 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 19:24:23 GMT
ENV _BASH_VERSION=4.4.23
# Wed, 22 May 2024 19:24:23 GMT
ENV _BASH_BASELINE=4.4.18
# Wed, 22 May 2024 19:24:23 GMT
ENV _BASH_BASELINE_PATCH=18
# Wed, 22 May 2024 19:24:23 GMT
ENV _BASH_LATEST_PATCH=23
# Wed, 22 May 2024 19:24:23 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz"; 	wget -O bash.tar.gz.sig "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz.sig"; 		: "${_BASH_BASELINE_PATCH:=0}" "${_BASH_LATEST_PATCH:=0}"; 	if [ "$_BASH_LATEST_PATCH" -gt "$_BASH_BASELINE_PATCH" ]; then 		mkdir -p bash-patches; 		first="$(printf '%03d' "$(( _BASH_BASELINE_PATCH + 1 ))")"; 		last="$(printf '%03d' "$_BASH_LATEST_PATCH")"; 		majorMinor="${_BASH_VERSION%.*}"; 		for patch in $(seq -w "$first" "$last"); do 			url="https://ftp.gnu.org/gnu/bash/bash-$majorMinor-patches/bash${majorMinor//./}-$patch"; 			wget -O "bash-patches/$patch" "$url"; 			wget -O "bash-patches/$patch.sig" "$url.sig"; 		done; 	fi; 		apk add --no-cache --virtual .gpg-deps gnupg; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7C0135FB088AAF6C66C650B9BB5869F064EA74AB; 	gpg --batch --verify bash.tar.gz.sig bash.tar.gz; 	rm bash.tar.gz.sig; 	if [ -d bash-patches ]; then 		for sig in bash-patches/*.sig; do 			p="${sig%.sig}"; 			gpg --batch --verify "$sig" "$p"; 			rm "$sig"; 		done; 	fi; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apk del --no-network .gpg-deps; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	for f in config.guess config.sub; do 		wget -O "support/$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 	done; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	[ "$(bash -c 'echo "${BASH_VERSION%%[^0-9.]*}"')" = "$_BASH_VERSION" ]; 	bash -c 'help' > /dev/null # buildkit
# Wed, 22 May 2024 19:24:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 May 2024 19:24:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 May 2024 19:24:23 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:df110db6acd600b9ee5ebd7b510779652f96424d3f80321a4e0dcb8a09aa0526`  
		Last Modified: Fri, 06 Sep 2024 22:48:57 GMT  
		Size: 3.5 MB (3461598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf0214bfe6f9ad79af5b69e1ba60e57caac614fe6a81e05b8add8e4c23975d22`  
		Last Modified: Sat, 07 Sep 2024 02:03:30 GMT  
		Size: 2.4 MB (2423302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84a8dcc356ad2c3ee784c8a9da70ab269e15372b055378fb2ae5b5d130d12225`  
		Last Modified: Sat, 07 Sep 2024 02:03:30 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:4-alpine3.20` - unknown; unknown

```console
$ docker pull bash@sha256:0f8a20b1f29f0000f61a4353a95953b771a92704e73ee2f5c01282e3c45784aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.4 KB (129385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76a221fd5688230e5f5b08129c9a4f561a2a6ef1b69c8304fbf2ed15591df1c8`

```dockerfile
```

-	Layers:
	-	`sha256:0e7dc3603de7f6a242de0dbc61506c8d6a33d409052346a20e7edb8278d8fdc5`  
		Last Modified: Sat, 07 Sep 2024 02:03:30 GMT  
		Size: 108.5 KB (108481 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2bfa3aa1c42d323598632c2c36d6dffa485d0879eff2cdaaae154456a9e06539`  
		Last Modified: Sat, 07 Sep 2024 02:03:30 GMT  
		Size: 20.9 KB (20904 bytes)  
		MIME: application/vnd.in-toto+json
