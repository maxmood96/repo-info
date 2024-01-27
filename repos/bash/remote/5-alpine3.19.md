## `bash:5-alpine3.19`

```console
$ docker pull bash@sha256:eab77f722c37a6b1afb22825ae624b7020775e5a5440cbc1a3adcf8b4471f140
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

### `bash:5-alpine3.19` - linux; amd64

```console
$ docker pull bash@sha256:9236ac4a1ca718a371c73c5633ff8e275f71a26cbae38f3c40dab9dc80c85bf2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6102954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6281a9c255295b1df2091c416e605da360e6dc5094a9f12dcb478e7151338d9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sun, 14 Jan 2024 05:17:51 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sun, 14 Jan 2024 05:17:51 GMT
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
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9202680e8b04cfe6a7291ff0f10cf057d816030b4c59df0bf9817982584872c0`  
		Last Modified: Sat, 27 Jan 2024 00:53:20 GMT  
		Size: 2.7 MB (2693890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9348d69e180fcbee20e0b5cc1886c1da4e2317718f90c4c5e889ab8b2ad0af3f`  
		Last Modified: Sat, 27 Jan 2024 00:53:19 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:5-alpine3.19` - unknown; unknown

```console
$ docker pull bash@sha256:4e9ae8b8ab73459e5e62c8ba5c30f9e740ee9d57343ff1479f066df27c57d903
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.8 KB (119794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2451aaa7836237423c922c688bf4c28df0f0e2a5f2e352bf36ebacbb8df9172`

```dockerfile
```

-	Layers:
	-	`sha256:e0b6e8a181f4b1a7f7c87e329b3b86ef96344f55f36d12966a3c9041cb6d78e5`  
		Last Modified: Sat, 27 Jan 2024 00:53:19 GMT  
		Size: 98.9 KB (98886 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8dc1f30dd93c878e9b267eb6b9409ef1c89fb93c39e6ccb8068b5a242579f101`  
		Last Modified: Sat, 27 Jan 2024 00:53:20 GMT  
		Size: 20.9 KB (20908 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:5-alpine3.19` - linux; arm variant v6

```console
$ docker pull bash@sha256:889eeac2ef30407b28bf27f3a89f1f17b69bbc0063aea4e4e70edddb96724f07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5802550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e242cbb79179e8166298e4d4acd4ce160628b9cb73832a6f2e87c9933d7aa1ee`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 08 Dec 2023 01:49:15 GMT
ADD file:d43ed267a41631ce0e5a4ef5aac821a75300a83f85ecb6259f5616852f89e989 in / 
# Fri, 08 Dec 2023 01:49:15 GMT
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
	-	`sha256:0803c38384d9fd0f9afaec8fd13d267547b660dcd46bb92a3d63c5d76e78b04c`  
		Last Modified: Fri, 08 Dec 2023 01:49:33 GMT  
		Size: 3.2 MB (3165143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:957efb14c438930c33d4b99efeb89a1e9f830f71935ca5b9abade3048abcf1d5`  
		Last Modified: Wed, 17 Jan 2024 07:52:21 GMT  
		Size: 2.6 MB (2637074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:754f8569c7519a8392b1e1c1054f64783e3a091125c6a04f21f241bf444cabdd`  
		Last Modified: Wed, 17 Jan 2024 07:52:20 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:5-alpine3.19` - unknown; unknown

```console
$ docker pull bash@sha256:f353cfe96193b296606d5a44aaaeb3034cfafc523727d9e1bb071c83c1434ba8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fccd14a46cdf39435f400abca3eaefeaf1828687f04c2e6d283b294ed3aa2da`

```dockerfile
```

-	Layers:
	-	`sha256:67d902bd9527378d9661c9acb8fc8d942301cf351da6df8413ae6dae8d1a777d`  
		Last Modified: Wed, 17 Jan 2024 07:52:20 GMT  
		Size: 20.6 KB (20629 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:5-alpine3.19` - linux; arm variant v7

```console
$ docker pull bash@sha256:e3b0bcc4435d351f45d96e1b82916f217a05724c1e48d57d17122400449ddec4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5509935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45785ba682cb0ecb784fedff55c2d2c40e26fe9bb42b9b3e06f3272aa90932ce`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sun, 14 Jan 2024 05:17:51 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sun, 14 Jan 2024 05:17:51 GMT
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
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36194bb578bb36006a7d9236ead8fd98f1eef920275e9526dbe7f5df5396998f`  
		Last Modified: Sat, 27 Jan 2024 12:45:25 GMT  
		Size: 2.6 MB (2590699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5367e1600015119aff157b76158ce84dd0e30bd06c5af61da9300bd3faaa23d9`  
		Last Modified: Sat, 27 Jan 2024 12:45:25 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:5-alpine3.19` - unknown; unknown

```console
$ docker pull bash@sha256:dba9c76b556e46ee8941631297a53b83cefb7645cc328b17a1fca1f14d1349ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.8 KB (119798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1dae333129e2839d7e34904efba988363ffb084761b690eebf8b0aca7fa9378`

```dockerfile
```

-	Layers:
	-	`sha256:7b1a077a2f319fc09e354e43e7a9cf06b1ba4084ce2ec0d483f65e6ac82dc734`  
		Last Modified: Sat, 27 Jan 2024 12:45:25 GMT  
		Size: 99.0 KB (98954 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ba95ade4a8fcbb80e7f90334974204dbb6337fb3cde93341b66fd01fb91bdf8`  
		Last Modified: Sat, 27 Jan 2024 12:45:25 GMT  
		Size: 20.8 KB (20844 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:5-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull bash@sha256:ef39a98191212dffb44a68f082a77f5635445ac8ad908376fd411bc641deceb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6129600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffacd8acfe8ff515711e1fa11b3c6d559a1cb111a2bd56dd04f2d459a281b1c8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sun, 14 Jan 2024 05:17:51 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Sun, 14 Jan 2024 05:17:51 GMT
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
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9ebaaa69514940cc9bd285c4c6548ae4ba31f085b3be0741884c9e0122790da`  
		Last Modified: Sat, 27 Jan 2024 17:38:32 GMT  
		Size: 2.8 MB (2781551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc62388f4f1ba2b03e38ec804e9b23b919a5477f0e8e2ae0abb8b9e5c9066bf3`  
		Last Modified: Sat, 27 Jan 2024 17:38:32 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:5-alpine3.19` - unknown; unknown

```console
$ docker pull bash@sha256:ac890b5b77139a2ec2bb99900730496c3290671c2823012057ed60732651cfd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.7 KB (119665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a3e07cdbe17ec560b39649bd0fa4d09ce7ef65a5148b7eda5e21fddb8fb5395`

```dockerfile
```

-	Layers:
	-	`sha256:0341be06772531fbf2b3c02da2f6e5f2ac20acf1f3ec4d8538a910c0b59eeb2d`  
		Last Modified: Sat, 27 Jan 2024 17:38:32 GMT  
		Size: 98.9 KB (98905 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c7f988c35e1c9872f6e8e506048785b2b952082c31e6c545a1ce519bfa4e916`  
		Last Modified: Sat, 27 Jan 2024 17:38:32 GMT  
		Size: 20.8 KB (20760 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:5-alpine3.19` - linux; 386

```console
$ docker pull bash@sha256:96f82247988d3adf193a8659ab2c3252bb92ea1d4bc9644761496e5b2ad12f9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5888781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0764d06575bde6934b053e70d9ea40a64f7e27ba80178304eea66d58778c35fc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sun, 14 Jan 2024 05:17:51 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Sun, 14 Jan 2024 05:17:51 GMT
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
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3be5e3a5ce8141de8936cf99750c892b464558c40394ebf60c3965bcbd0c37c`  
		Last Modified: Sat, 27 Jan 2024 01:54:26 GMT  
		Size: 2.6 MB (2644362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aade79c902f92d466bb40b820d972a8332f1df8fbbbbafb3998546fe4be9b1c`  
		Last Modified: Sat, 27 Jan 2024 01:54:26 GMT  
		Size: 330.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:5-alpine3.19` - unknown; unknown

```console
$ docker pull bash@sha256:f5c7c4671289737d70ae9101a65e06130657b1a59571aa13f2caaa6a1e2599b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.7 KB (119700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa1cf719419ec3ea3eb00d2dd322c5dd1f8684e96c1016bf117a35310729df51`

```dockerfile
```

-	Layers:
	-	`sha256:8cdd422808a5f50a690bbbf39990b64ab40b0aedb67fb03b3c4bb1ce37224123`  
		Last Modified: Sat, 27 Jan 2024 01:54:26 GMT  
		Size: 98.8 KB (98841 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1d65e5317f8b4ae5412c705886134ab923f19039f582071929a0b5a6017e7a6`  
		Last Modified: Sat, 27 Jan 2024 01:54:26 GMT  
		Size: 20.9 KB (20859 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:5-alpine3.19` - linux; ppc64le

```console
$ docker pull bash@sha256:080a0adbc5171627b870b5a898620cccadec114c81762f468bea3052a9c0c24b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6304024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1cf212329504b5d2b338a0e6ad09bf5b5b86d782b78da52385dc1df3d2a219f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sun, 14 Jan 2024 05:17:51 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sun, 14 Jan 2024 05:17:51 GMT
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
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76f8f820cafa1157e15be6659feb8f57f7f20d6b28f58c19616392be7a6947b9`  
		Last Modified: Sat, 27 Jan 2024 08:52:57 GMT  
		Size: 2.9 MB (2945335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e37e8e5ee71f9003e6be094fc2d719058f554029bda786931b3557ab456f7e9`  
		Last Modified: Sat, 27 Jan 2024 08:52:57 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:5-alpine3.19` - unknown; unknown

```console
$ docker pull bash@sha256:39f6032be4cb6483b9dcec024e24d5e4c2475d57f6427b7ff0ec4f8c555416ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.1 KB (118111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d803402fff37a92945cb67d80ae705332632bd0945305e00314cc64a774a60f`

```dockerfile
```

-	Layers:
	-	`sha256:05c8c22b47d2542f5b01a83dab404e3871aa0be0fb435646d8cce6eda18100f6`  
		Last Modified: Sat, 27 Jan 2024 08:52:57 GMT  
		Size: 97.3 KB (97308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c65b14bb5edc4036281363edad9d024ee40c460bd9dce7b5365f3a039d832a0`  
		Last Modified: Sat, 27 Jan 2024 08:52:57 GMT  
		Size: 20.8 KB (20803 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:5-alpine3.19` - linux; s390x

```console
$ docker pull bash@sha256:c3bfeb62c13371ff3185f414ee07ca2c9c8852a07b8605564f5e46313925d685
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6024744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2539b8b99d4cdbb554667be6d4015b5038a43b3972ed580d35478d2d6b86df6d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sun, 14 Jan 2024 05:17:51 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sun, 14 Jan 2024 05:17:51 GMT
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
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:773523f073c1f586ce2fdc70c56d3e4332aeb3e6789c0abed80eeb7435f3f280`  
		Last Modified: Sat, 27 Jan 2024 20:18:50 GMT  
		Size: 2.8 MB (2781773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:979958642450231a1712504bf7382ad3be30e03b4ba5b573c70de9f8f72bf4b1`  
		Last Modified: Sat, 27 Jan 2024 20:18:49 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:5-alpine3.19` - unknown; unknown

```console
$ docker pull bash@sha256:c025d13613f3b48e79d9dcb1b429121e297e784af489cb30887c0137c0e429b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.0 KB (117992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bb7a87e436a0c220e831128b54965bddc540a6dfccc61e2e635ae4fc46002d6`

```dockerfile
```

-	Layers:
	-	`sha256:7884a36e0c3e05d91addce80cef7e850e9bfa70ecc3d43cbc6314492266acc5b`  
		Last Modified: Sat, 27 Jan 2024 20:18:49 GMT  
		Size: 97.2 KB (97250 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ecbfd5ce7bb50d347b5fa5369d002de1ed6a45f11247aa46af607461b6247a64`  
		Last Modified: Sat, 27 Jan 2024 20:18:49 GMT  
		Size: 20.7 KB (20742 bytes)  
		MIME: application/vnd.in-toto+json
