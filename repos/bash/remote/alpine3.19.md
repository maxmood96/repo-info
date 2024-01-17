## `bash:alpine3.19`

```console
$ docker pull bash@sha256:352942fa9797bb705574ebe60918045d3b7c75a36c56a839ecdfa421355b5db7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
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
	-	linux; s390x
	-	unknown; unknown

### `bash:alpine3.19` - linux; amd64

```console
$ docker pull bash@sha256:04a159e6aabe3573e73db0bb2965cc8f8df24e964b2616db63def9eb1e27ece0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6102721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1352efe85de22790c0b6933536f5c0c22ec9da46c437e173ec2520d410a59f8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 08 Dec 2023 01:20:49 GMT
ADD file:1f4eb46669b5b6275af19eb7471a6899a61c276aa7d925b8ae99310b14b75b92 in / 
# Fri, 08 Dec 2023 01:20:49 GMT
CMD ["/bin/sh"]
# Sun, 14 Jan 2024 05:17:51 GMT
ENV _BASH_VERSION=5.2.26
# Sun, 14 Jan 2024 05:17:51 GMT
ENV _BASH_BASELINE=5.2.21
# Sun, 14 Jan 2024 05:17:51 GMT
ENV _BASH_BASELINE_PATCH=21
# Sun, 14 Jan 2024 05:17:51 GMT
ENV _BASH_LATEST_PATCH=26
# Sun, 14 Jan 2024 05:17:51 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz"; 	wget -O bash.tar.gz.sig "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz.sig"; 		: "${_BASH_BASELINE_PATCH:=0}" "${_BASH_LATEST_PATCH:=0}"; 	if [ "$_BASH_LATEST_PATCH" -gt "$_BASH_BASELINE_PATCH" ]; then 		mkdir -p bash-patches; 		first="$(printf '%03d' "$(( _BASH_BASELINE_PATCH + 1 ))")"; 		last="$(printf '%03d' "$_BASH_LATEST_PATCH")"; 		majorMinor="${_BASH_VERSION%.*}"; 		for patch in $(seq -w "$first" "$last"); do 			url="https://ftp.gnu.org/gnu/bash/bash-$majorMinor-patches/bash${majorMinor//./}-$patch"; 			wget -O "bash-patches/$patch" "$url"; 			wget -O "bash-patches/$patch.sig" "$url.sig"; 		done; 	fi; 		apk add --no-cache --virtual .gpg-deps gnupg; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7C0135FB088AAF6C66C650B9BB5869F064EA74AB; 	gpg --batch --verify bash.tar.gz.sig bash.tar.gz; 	rm bash.tar.gz.sig; 	if [ -d bash-patches ]; then 		for sig in bash-patches/*.sig; do 			p="${sig%.sig}"; 			gpg --batch --verify "$sig" "$p"; 			rm "$sig"; 		done; 	fi; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apk del --no-network .gpg-deps; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	[ "$(bash -c 'echo "${BASH_VERSION%%[^0-9.]*}"')" = "$_BASH_VERSION" ]; 	bash -c 'help' > /dev/null # buildkit
# Sun, 14 Jan 2024 05:17:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 14 Jan 2024 05:17:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 14 Jan 2024 05:17:51 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:661ff4d9561e3fd050929ee5097067c34bafc523ee60f5294a37fd08056a73ca`  
		Last Modified: Fri, 08 Dec 2023 01:21:10 GMT  
		Size: 3.4 MB (3408480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3457e77a5d5630618e0c190cd2aaf706c133e86b2ac2f9820a4b0cc585e90e0`  
		Last Modified: Tue, 16 Jan 2024 23:55:55 GMT  
		Size: 2.7 MB (2693903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:031bc8ff5d45b54b420457a7c15b950930c6d2143564754a2c99b4e6ed7802c3`  
		Last Modified: Tue, 16 Jan 2024 23:55:55 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:alpine3.19` - unknown; unknown

```console
$ docker pull bash@sha256:6fd197e2b56c74fe5e83688a6dc3c7b4ae0b9447873e85764146030b7068623b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.8 KB (119788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e35f2fd12d8ab3add1f001829852c4348e8d87202809994b0ca86e1f6e8d96d`

```dockerfile
```

-	Layers:
	-	`sha256:1e7c01f8f40e65bafa5c335f3b607fcfede160a45e22032a3a05213f68554bdc`  
		Last Modified: Tue, 16 Jan 2024 23:55:55 GMT  
		Size: 98.9 KB (98880 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff296dbe96de4b1e7faedffe2dcc99c097996dd38d58e24942ffc31fb1238b7f`  
		Last Modified: Tue, 16 Jan 2024 23:55:55 GMT  
		Size: 20.9 KB (20908 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:alpine3.19` - linux; arm variant v6

```console
$ docker pull bash@sha256:b335a9005d19080c7708fa5d58dadd81eb9b15a3ed80375c7e51d84ba1f3bcec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5802650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51e3706ba17a79a8f336aa6473a4d0e346db1f8beb00eca7ded63bdf8f8bf3a3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 08 Dec 2023 01:49:15 GMT
ADD file:d43ed267a41631ce0e5a4ef5aac821a75300a83f85ecb6259f5616852f89e989 in / 
# Fri, 08 Dec 2023 01:49:15 GMT
CMD ["/bin/sh"]
# Fri, 08 Dec 2023 05:42:09 GMT
ENV _BASH_VERSION=5.2.21
# Fri, 08 Dec 2023 05:42:09 GMT
ENV _BASH_BASELINE=5.2.21
# Fri, 08 Dec 2023 05:42:09 GMT
ENV _BASH_BASELINE_PATCH=21
# Fri, 08 Dec 2023 05:42:09 GMT
ENV _BASH_LATEST_PATCH=21
# Fri, 08 Dec 2023 05:42:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz"; 	wget -O bash.tar.gz.sig "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz.sig"; 		: "${_BASH_BASELINE_PATCH:=0}" "${_BASH_LATEST_PATCH:=0}"; 	if [ "$_BASH_LATEST_PATCH" -gt "$_BASH_BASELINE_PATCH" ]; then 		mkdir -p bash-patches; 		first="$(printf '%03d' "$(( _BASH_BASELINE_PATCH + 1 ))")"; 		last="$(printf '%03d' "$_BASH_LATEST_PATCH")"; 		majorMinor="${_BASH_VERSION%.*}"; 		for patch in $(seq -w "$first" "$last"); do 			url="https://ftp.gnu.org/gnu/bash/bash-$majorMinor-patches/bash${majorMinor//./}-$patch"; 			wget -O "bash-patches/$patch" "$url"; 			wget -O "bash-patches/$patch.sig" "$url.sig"; 		done; 	fi; 		apk add --no-cache --virtual .gpg-deps gnupg; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7C0135FB088AAF6C66C650B9BB5869F064EA74AB; 	gpg --batch --verify bash.tar.gz.sig bash.tar.gz; 	rm bash.tar.gz.sig; 	if [ -d bash-patches ]; then 		for sig in bash-patches/*.sig; do 			p="${sig%.sig}"; 			gpg --batch --verify "$sig" "$p"; 			rm "$sig"; 		done; 	fi; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apk del --no-network .gpg-deps; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	[ "$(bash -c 'echo "${BASH_VERSION%%[^0-9.]*}"')" = "$_BASH_VERSION" ]; 	bash -c 'help' > /dev/null # buildkit
# Fri, 08 Dec 2023 05:42:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 Dec 2023 05:42:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 Dec 2023 05:42:09 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:0803c38384d9fd0f9afaec8fd13d267547b660dcd46bb92a3d63c5d76e78b04c`  
		Last Modified: Fri, 08 Dec 2023 01:49:33 GMT  
		Size: 3.2 MB (3165143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f22d23fd041832352ea0fb10e4e5ca0019579ab7acf07aaa1388461cc435b71a`  
		Last Modified: Wed, 20 Dec 2023 21:26:12 GMT  
		Size: 2.6 MB (2637170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:872c32d809bedd6ac0541aec36c235984289e45b5776b4ab693fe42269b49f63`  
		Last Modified: Wed, 20 Dec 2023 21:26:11 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:alpine3.19` - unknown; unknown

```console
$ docker pull bash@sha256:2304b5bdec00965a9e7e8e7350f8261f8453ca422f334de46df1d218dffcd7b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf164d7db6e9b0d8864a903cb7eb016807a9adf80e9abc87035fc7fbc0c9e1d5`

```dockerfile
```

-	Layers:
	-	`sha256:acf24fc11bcb7625f43e975a839c6f9fdaf1bd14ebde36e7dfb92084b220e1af`  
		Last Modified: Wed, 20 Dec 2023 21:26:12 GMT  
		Size: 20.6 KB (20628 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:alpine3.19` - linux; arm variant v7

```console
$ docker pull bash@sha256:a71fd4a19d2c29e7c09ef21c5fea3381a947f3312dd066dd32480fe9059fcd52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5509480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9fdd4a3be0084b1452d5b01478cf631875385ed6683851756fbc604d3a2a5be`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 08 Dec 2023 01:57:20 GMT
ADD file:13b9291053208eec61cd7c97bac2fa154380ad8d10182567763eea3e10c5882f in / 
# Fri, 08 Dec 2023 01:57:20 GMT
CMD ["/bin/sh"]
# Fri, 08 Dec 2023 05:42:09 GMT
ENV _BASH_VERSION=5.2.21
# Fri, 08 Dec 2023 05:42:09 GMT
ENV _BASH_BASELINE=5.2.21
# Fri, 08 Dec 2023 05:42:09 GMT
ENV _BASH_BASELINE_PATCH=21
# Fri, 08 Dec 2023 05:42:09 GMT
ENV _BASH_LATEST_PATCH=21
# Fri, 08 Dec 2023 05:42:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz"; 	wget -O bash.tar.gz.sig "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz.sig"; 		: "${_BASH_BASELINE_PATCH:=0}" "${_BASH_LATEST_PATCH:=0}"; 	if [ "$_BASH_LATEST_PATCH" -gt "$_BASH_BASELINE_PATCH" ]; then 		mkdir -p bash-patches; 		first="$(printf '%03d' "$(( _BASH_BASELINE_PATCH + 1 ))")"; 		last="$(printf '%03d' "$_BASH_LATEST_PATCH")"; 		majorMinor="${_BASH_VERSION%.*}"; 		for patch in $(seq -w "$first" "$last"); do 			url="https://ftp.gnu.org/gnu/bash/bash-$majorMinor-patches/bash${majorMinor//./}-$patch"; 			wget -O "bash-patches/$patch" "$url"; 			wget -O "bash-patches/$patch.sig" "$url.sig"; 		done; 	fi; 		apk add --no-cache --virtual .gpg-deps gnupg; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7C0135FB088AAF6C66C650B9BB5869F064EA74AB; 	gpg --batch --verify bash.tar.gz.sig bash.tar.gz; 	rm bash.tar.gz.sig; 	if [ -d bash-patches ]; then 		for sig in bash-patches/*.sig; do 			p="${sig%.sig}"; 			gpg --batch --verify "$sig" "$p"; 			rm "$sig"; 		done; 	fi; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apk del --no-network .gpg-deps; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	[ "$(bash -c 'echo "${BASH_VERSION%%[^0-9.]*}"')" = "$_BASH_VERSION" ]; 	bash -c 'help' > /dev/null # buildkit
# Fri, 08 Dec 2023 05:42:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 Dec 2023 05:42:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 Dec 2023 05:42:09 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:1086c24c41097f090ce847d192c11307e1715eeb563a2cf4f410b2a199ae1942`  
		Last Modified: Fri, 08 Dec 2023 01:57:36 GMT  
		Size: 2.9 MB (2918701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b977dafdcdf7057d33926d1e1e89678b15f6ecabe3d23088dfc12768df29641a`  
		Last Modified: Wed, 20 Dec 2023 21:54:06 GMT  
		Size: 2.6 MB (2590446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50e905cf9da13641c76fb5710fb171d6fdacaea0c04cfbc72d1d818767bf21ab`  
		Last Modified: Wed, 20 Dec 2023 21:54:06 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:alpine3.19` - unknown; unknown

```console
$ docker pull bash@sha256:fc4eb8b5d8c97dc7d833025c2cc50d40d553d1234f5a49a25c1d1d355e1cda77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.8 KB (119792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7696b2289196ced54c3c223101af65f5b030a97e69a2e6c2aa3edda6b9ad3fc2`

```dockerfile
```

-	Layers:
	-	`sha256:8f74c806581643484526e9ac9b9672540962b828a59d02e735b654d9164f7c00`  
		Last Modified: Wed, 20 Dec 2023 21:54:06 GMT  
		Size: 98.9 KB (98948 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:088cce0f875de3a7accbdc9ce065856fc5f9e01e34de780c85e30015b10202f7`  
		Last Modified: Wed, 20 Dec 2023 21:54:06 GMT  
		Size: 20.8 KB (20844 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:alpine3.19` - linux; arm64 variant v8

```console
$ docker pull bash@sha256:615b881705e8def55870228e0c6af48b835b88b09a4d330bf647de1dac6d6e98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6129683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6fbb53c83922776e28bd7c0259d7c293aa65ab3822c140ec28afe5eeb5d7a1a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 08 Dec 2023 01:39:30 GMT
ADD file:8182c73f869a899cf624a59c400acb8226776d15e4d3a0d240a94e65340540d0 in / 
# Fri, 08 Dec 2023 01:39:30 GMT
CMD ["/bin/sh"]
# Sun, 14 Jan 2024 05:17:51 GMT
ENV _BASH_VERSION=5.2.26
# Sun, 14 Jan 2024 05:17:51 GMT
ENV _BASH_BASELINE=5.2.21
# Sun, 14 Jan 2024 05:17:51 GMT
ENV _BASH_BASELINE_PATCH=21
# Sun, 14 Jan 2024 05:17:51 GMT
ENV _BASH_LATEST_PATCH=26
# Sun, 14 Jan 2024 05:17:51 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz"; 	wget -O bash.tar.gz.sig "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz.sig"; 		: "${_BASH_BASELINE_PATCH:=0}" "${_BASH_LATEST_PATCH:=0}"; 	if [ "$_BASH_LATEST_PATCH" -gt "$_BASH_BASELINE_PATCH" ]; then 		mkdir -p bash-patches; 		first="$(printf '%03d' "$(( _BASH_BASELINE_PATCH + 1 ))")"; 		last="$(printf '%03d' "$_BASH_LATEST_PATCH")"; 		majorMinor="${_BASH_VERSION%.*}"; 		for patch in $(seq -w "$first" "$last"); do 			url="https://ftp.gnu.org/gnu/bash/bash-$majorMinor-patches/bash${majorMinor//./}-$patch"; 			wget -O "bash-patches/$patch" "$url"; 			wget -O "bash-patches/$patch.sig" "$url.sig"; 		done; 	fi; 		apk add --no-cache --virtual .gpg-deps gnupg; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7C0135FB088AAF6C66C650B9BB5869F064EA74AB; 	gpg --batch --verify bash.tar.gz.sig bash.tar.gz; 	rm bash.tar.gz.sig; 	if [ -d bash-patches ]; then 		for sig in bash-patches/*.sig; do 			p="${sig%.sig}"; 			gpg --batch --verify "$sig" "$p"; 			rm "$sig"; 		done; 	fi; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apk del --no-network .gpg-deps; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	[ "$(bash -c 'echo "${BASH_VERSION%%[^0-9.]*}"')" = "$_BASH_VERSION" ]; 	bash -c 'help' > /dev/null # buildkit
# Sun, 14 Jan 2024 05:17:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 14 Jan 2024 05:17:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 14 Jan 2024 05:17:51 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:c303524923177661067f7eb378c3dd5277088c2676ebd1cd78e68397bb80fdbf`  
		Last Modified: Fri, 08 Dec 2023 01:39:48 GMT  
		Size: 3.3 MB (3347794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61bb5347ef9f696a5837179ac7d880333cd0c7288e283d68e92c36d8c1b945ca`  
		Last Modified: Wed, 17 Jan 2024 01:33:47 GMT  
		Size: 2.8 MB (2781557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e73ed318ffea23658f94b9b9cae51a2f5658d2b5f7ebf7731afbbf6b2a23e63a`  
		Last Modified: Wed, 17 Jan 2024 01:33:47 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:alpine3.19` - unknown; unknown

```console
$ docker pull bash@sha256:6a8f97f13c8e7ae1afe890b386dd2a2e5773ad6bb140a3a1a4975ff50068c705
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.7 KB (119659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f7a8cf517bedbed7006bc6652593a20e1ac81afb5ea45b9c6e58cdafa5eb27e`

```dockerfile
```

-	Layers:
	-	`sha256:de87834d9c5383ec29fd7740cea58aecf1ef2cd36cc044a92af4fc69e4ef492c`  
		Last Modified: Wed, 17 Jan 2024 01:33:47 GMT  
		Size: 98.9 KB (98899 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16bfc7a84b7ef310ebd8ba879abb27062cbc0fd74e427640ec6834246f0d8c97`  
		Last Modified: Wed, 17 Jan 2024 01:33:47 GMT  
		Size: 20.8 KB (20760 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:alpine3.19` - linux; 386

```console
$ docker pull bash@sha256:31752a21bea7775fe0bd57d76e2a97403f9397dc6a4b9eaf2d19eb5e2f34e0b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5888813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88d5befe36375639b702ed6f766e90d865cdb39703600921e7cb7661eb2602a0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 08 Dec 2023 01:38:25 GMT
ADD file:bd52540f209ba362654d795d7893669c819d35011a16f9f319301727a33b3bd9 in / 
# Fri, 08 Dec 2023 01:38:25 GMT
CMD ["/bin/sh"]
# Sun, 14 Jan 2024 05:17:51 GMT
ENV _BASH_VERSION=5.2.26
# Sun, 14 Jan 2024 05:17:51 GMT
ENV _BASH_BASELINE=5.2.21
# Sun, 14 Jan 2024 05:17:51 GMT
ENV _BASH_BASELINE_PATCH=21
# Sun, 14 Jan 2024 05:17:51 GMT
ENV _BASH_LATEST_PATCH=26
# Sun, 14 Jan 2024 05:17:51 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz"; 	wget -O bash.tar.gz.sig "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz.sig"; 		: "${_BASH_BASELINE_PATCH:=0}" "${_BASH_LATEST_PATCH:=0}"; 	if [ "$_BASH_LATEST_PATCH" -gt "$_BASH_BASELINE_PATCH" ]; then 		mkdir -p bash-patches; 		first="$(printf '%03d' "$(( _BASH_BASELINE_PATCH + 1 ))")"; 		last="$(printf '%03d' "$_BASH_LATEST_PATCH")"; 		majorMinor="${_BASH_VERSION%.*}"; 		for patch in $(seq -w "$first" "$last"); do 			url="https://ftp.gnu.org/gnu/bash/bash-$majorMinor-patches/bash${majorMinor//./}-$patch"; 			wget -O "bash-patches/$patch" "$url"; 			wget -O "bash-patches/$patch.sig" "$url.sig"; 		done; 	fi; 		apk add --no-cache --virtual .gpg-deps gnupg; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7C0135FB088AAF6C66C650B9BB5869F064EA74AB; 	gpg --batch --verify bash.tar.gz.sig bash.tar.gz; 	rm bash.tar.gz.sig; 	if [ -d bash-patches ]; then 		for sig in bash-patches/*.sig; do 			p="${sig%.sig}"; 			gpg --batch --verify "$sig" "$p"; 			rm "$sig"; 		done; 	fi; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apk del --no-network .gpg-deps; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	[ "$(bash -c 'echo "${BASH_VERSION%%[^0-9.]*}"')" = "$_BASH_VERSION" ]; 	bash -c 'help' > /dev/null # buildkit
# Sun, 14 Jan 2024 05:17:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 14 Jan 2024 05:17:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 14 Jan 2024 05:17:51 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:9acd8b4c9d4385585f74dabb4bc6b3351888710ae37ec5dbd9ea950281b8f9bb`  
		Last Modified: Fri, 08 Dec 2023 01:38:43 GMT  
		Size: 3.2 MB (3244115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f803d3f0b0aa59d297a24efe7a2cc837d1983c417a1a33a64c5e963185ab283`  
		Last Modified: Tue, 16 Jan 2024 23:55:54 GMT  
		Size: 2.6 MB (2644364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe09d41f52149de1cca3588c491301b441320bff28734a63d21b808dab5efacf`  
		Last Modified: Tue, 16 Jan 2024 23:55:53 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:alpine3.19` - unknown; unknown

```console
$ docker pull bash@sha256:b7225de1403e9e3a1a54934da0a50c7676f1b2a0355ebdf3782ff918c835b48b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.7 KB (119693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b5be755e27174fa019dd04cde7f1f58a33d2c84aa00a9182dd7c0fa14f3cf8a`

```dockerfile
```

-	Layers:
	-	`sha256:f065bf5b7b38e9cfddd69351d9617ceb7b80107b79d993bf1650332a7979287c`  
		Last Modified: Tue, 16 Jan 2024 23:55:53 GMT  
		Size: 98.8 KB (98835 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53afdb51fdfcd28835ab1e69f131a04de8f1d12855c9213f7d4fdd944772deb1`  
		Last Modified: Tue, 16 Jan 2024 23:55:53 GMT  
		Size: 20.9 KB (20858 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:alpine3.19` - linux; ppc64le

```console
$ docker pull bash@sha256:791cbbd427388c4d69c356c71b131759a63b28d907bcc89307cf1c41969f5477
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6303925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d95360598975c677c59fd9d84a5cd380d43ad81d0dd8cb5fed1b300e68eb226a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 08 Dec 2023 01:22:51 GMT
ADD file:052421189f8d269382daaaa8beb63c687e4d8ca908c421abdce53bcc627a40b4 in / 
# Fri, 08 Dec 2023 01:22:51 GMT
CMD ["/bin/sh"]
# Sun, 14 Jan 2024 05:17:51 GMT
ENV _BASH_VERSION=5.2.26
# Sun, 14 Jan 2024 05:17:51 GMT
ENV _BASH_BASELINE=5.2.21
# Sun, 14 Jan 2024 05:17:51 GMT
ENV _BASH_BASELINE_PATCH=21
# Sun, 14 Jan 2024 05:17:51 GMT
ENV _BASH_LATEST_PATCH=26
# Sun, 14 Jan 2024 05:17:51 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz"; 	wget -O bash.tar.gz.sig "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz.sig"; 		: "${_BASH_BASELINE_PATCH:=0}" "${_BASH_LATEST_PATCH:=0}"; 	if [ "$_BASH_LATEST_PATCH" -gt "$_BASH_BASELINE_PATCH" ]; then 		mkdir -p bash-patches; 		first="$(printf '%03d' "$(( _BASH_BASELINE_PATCH + 1 ))")"; 		last="$(printf '%03d' "$_BASH_LATEST_PATCH")"; 		majorMinor="${_BASH_VERSION%.*}"; 		for patch in $(seq -w "$first" "$last"); do 			url="https://ftp.gnu.org/gnu/bash/bash-$majorMinor-patches/bash${majorMinor//./}-$patch"; 			wget -O "bash-patches/$patch" "$url"; 			wget -O "bash-patches/$patch.sig" "$url.sig"; 		done; 	fi; 		apk add --no-cache --virtual .gpg-deps gnupg; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7C0135FB088AAF6C66C650B9BB5869F064EA74AB; 	gpg --batch --verify bash.tar.gz.sig bash.tar.gz; 	rm bash.tar.gz.sig; 	if [ -d bash-patches ]; then 		for sig in bash-patches/*.sig; do 			p="${sig%.sig}"; 			gpg --batch --verify "$sig" "$p"; 			rm "$sig"; 		done; 	fi; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apk del --no-network .gpg-deps; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	[ "$(bash -c 'echo "${BASH_VERSION%%[^0-9.]*}"')" = "$_BASH_VERSION" ]; 	bash -c 'help' > /dev/null # buildkit
# Sun, 14 Jan 2024 05:17:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 14 Jan 2024 05:17:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 14 Jan 2024 05:17:51 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:243ac51c334a47917a84be93e972ee6378987e9b3b917a5a8df29025e161c1f3`  
		Last Modified: Fri, 08 Dec 2023 01:23:14 GMT  
		Size: 3.4 MB (3358233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59f05419accd2be197b67b8674c86bd3d6ae6436cf9b30d2fb9eb972464e9ccf`  
		Last Modified: Wed, 17 Jan 2024 00:18:13 GMT  
		Size: 2.9 MB (2945356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7992beccc58757d04fc0767d55ed5f643dea83780e7fc890b91604353685133`  
		Last Modified: Wed, 17 Jan 2024 00:18:12 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:alpine3.19` - unknown; unknown

```console
$ docker pull bash@sha256:2ba879ce93e5212b39ed15ed5ef761e313b8569b099b8e5c879012dc14cfa632
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.1 KB (118106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:113274d25915560df6e7d136ec1999a5d4b0bdd023e639ffc3af7170bb221de0`

```dockerfile
```

-	Layers:
	-	`sha256:edd9a4093df5a169c5f2add57333dacdaee14d9d55f3fd23953959f99e282ea0`  
		Last Modified: Wed, 17 Jan 2024 00:18:13 GMT  
		Size: 97.3 KB (97302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae3117444fe5c8b5bedc6718d58043de41750b27fb9406dcff2234c02da4a305`  
		Last Modified: Wed, 17 Jan 2024 00:18:12 GMT  
		Size: 20.8 KB (20804 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:alpine3.19` - linux; s390x

```console
$ docker pull bash@sha256:fed1a0589c4b4444536202734129bce9fa8bf4073423aea32c988ebab8ac9a5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6024446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d32d9014616d15c77428b7fdfdf9ce9e057558280ac6089d619f1240aba341c3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 08 Dec 2023 01:41:50 GMT
ADD file:47e0982fc3ae485c06d46f3c0022afd39ed7ec95fe755c2391e6b0cfcae65dfc in / 
# Fri, 08 Dec 2023 01:41:51 GMT
CMD ["/bin/sh"]
# Sun, 14 Jan 2024 05:17:51 GMT
ENV _BASH_VERSION=5.2.26
# Sun, 14 Jan 2024 05:17:51 GMT
ENV _BASH_BASELINE=5.2.21
# Sun, 14 Jan 2024 05:17:51 GMT
ENV _BASH_BASELINE_PATCH=21
# Sun, 14 Jan 2024 05:17:51 GMT
ENV _BASH_LATEST_PATCH=26
# Sun, 14 Jan 2024 05:17:51 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz"; 	wget -O bash.tar.gz.sig "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz.sig"; 		: "${_BASH_BASELINE_PATCH:=0}" "${_BASH_LATEST_PATCH:=0}"; 	if [ "$_BASH_LATEST_PATCH" -gt "$_BASH_BASELINE_PATCH" ]; then 		mkdir -p bash-patches; 		first="$(printf '%03d' "$(( _BASH_BASELINE_PATCH + 1 ))")"; 		last="$(printf '%03d' "$_BASH_LATEST_PATCH")"; 		majorMinor="${_BASH_VERSION%.*}"; 		for patch in $(seq -w "$first" "$last"); do 			url="https://ftp.gnu.org/gnu/bash/bash-$majorMinor-patches/bash${majorMinor//./}-$patch"; 			wget -O "bash-patches/$patch" "$url"; 			wget -O "bash-patches/$patch.sig" "$url.sig"; 		done; 	fi; 		apk add --no-cache --virtual .gpg-deps gnupg; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7C0135FB088AAF6C66C650B9BB5869F064EA74AB; 	gpg --batch --verify bash.tar.gz.sig bash.tar.gz; 	rm bash.tar.gz.sig; 	if [ -d bash-patches ]; then 		for sig in bash-patches/*.sig; do 			p="${sig%.sig}"; 			gpg --batch --verify "$sig" "$p"; 			rm "$sig"; 		done; 	fi; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apk del --no-network .gpg-deps; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	[ "$(bash -c 'echo "${BASH_VERSION%%[^0-9.]*}"')" = "$_BASH_VERSION" ]; 	bash -c 'help' > /dev/null # buildkit
# Sun, 14 Jan 2024 05:17:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 14 Jan 2024 05:17:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 14 Jan 2024 05:17:51 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:0fca3ee44ced87b7184bc23390283fdf10cfae0e844a25b785dd11c463815227`  
		Last Modified: Fri, 08 Dec 2023 01:42:30 GMT  
		Size: 3.2 MB (3242332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1449d66b85c92cc3f56b2732af659c38c763354d7428007b15ff6743c162e28`  
		Last Modified: Wed, 17 Jan 2024 04:43:47 GMT  
		Size: 2.8 MB (2781784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e38cec64d8123fbc5d13442c305b289eb2eaf045a54bcdeca46f56ab46a18e6`  
		Last Modified: Wed, 17 Jan 2024 04:43:47 GMT  
		Size: 330.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:alpine3.19` - unknown; unknown

```console
$ docker pull bash@sha256:6248532cf22a7944aac22b69067f033ec33c2c04e9d6702e72fbae7091db9bc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.0 KB (117986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f6bb22b3e151b2ac2ef9393c442deffe17d9b1269f53c07bb365225c79c2598`

```dockerfile
```

-	Layers:
	-	`sha256:d71bef787f005cdd2bb34edf5c24c251b4cc9dc05c2509fb0f2a665685ceb7e9`  
		Last Modified: Wed, 17 Jan 2024 04:43:47 GMT  
		Size: 97.2 KB (97244 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e26344485c367ca7b705eff17525fed2386c292441e9274411b8f1da80af212a`  
		Last Modified: Wed, 17 Jan 2024 04:43:47 GMT  
		Size: 20.7 KB (20742 bytes)  
		MIME: application/vnd.in-toto+json
