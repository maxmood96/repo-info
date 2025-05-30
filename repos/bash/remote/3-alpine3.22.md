## `bash:3-alpine3.22`

```console
$ docker pull bash@sha256:3f734e97d036905f74fc79c46e6f8845dcb53cce95fe714299b598c9c9210ac7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `bash:3-alpine3.22` - linux; amd64

```console
$ docker pull bash@sha256:8e59ef6a362745410d0294b5a5f92c9edcd2a6235c8b8108dfc5d0b9744b66fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4454298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:056b8f75fdac420c3c911859bc3b05f7aee56a2d96154870e0b64d388ea7fa1c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
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
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Fri, 30 May 2025 18:04:24 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a624641b39a294e1854b62706c572d9ab658082e263d7af1a6fdc6e977108cb`  
		Last Modified: Fri, 30 May 2025 20:49:33 GMT  
		Size: 1.6 KB (1630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e8d241bd26eaf81835c8e1c0e9879fc3e3e6c4af97dc3d25a2bf9d11a89f15a`  
		Last Modified: Fri, 30 May 2025 20:49:33 GMT  
		Size: 655.5 KB (655488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:380f0ced90fd6d362dba23df012ccb868c5e2852b9198ad7347ccffa3caf4777`  
		Last Modified: Fri, 30 May 2025 20:49:33 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:3-alpine3.22` - unknown; unknown

```console
$ docker pull bash@sha256:860ab57def27a286a6e791bda8cffeeb0d100960e78feaf23de358a5dea4d560
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.7 KB (142709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c358daa3713a6e7176274b4f1944e3e66b22620a5208be3427d94834c8f5c006`

```dockerfile
```

-	Layers:
	-	`sha256:02e0c617540ac10d98b20fe75fd9534b7dbf40a4d09f9b32364fe15487714dcf`  
		Last Modified: Fri, 30 May 2025 20:49:33 GMT  
		Size: 119.0 KB (118981 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32ad0a5c23834ddc51158acfcc09c91d588e3ce3a7c02dbb047a7279d2f99676`  
		Last Modified: Fri, 30 May 2025 20:49:33 GMT  
		Size: 23.7 KB (23728 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:3-alpine3.22` - linux; 386

```console
$ docker pull bash@sha256:c931c10e594c8578419a2ee58dafa17499b6a88f6bb4ac0b091dc56daf67a3ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4256858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adf4a157f6604d1831c805a49ea34bffd2883d8aa4fd23adae58090e45b35921`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86.tar.gz / # buildkit
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
	-	`sha256:c787620501b746b3aa9ec021f3ddb0b707572b5c68e33d73be392b9c078a4993`  
		Last Modified: Fri, 30 May 2025 18:04:26 GMT  
		Size: 3.6 MB (3616029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b400a1b05692c669947f7429e6dabda5d1600f7722b2b6cc6d558dd31e0f5ec`  
		Last Modified: Fri, 30 May 2025 20:49:21 GMT  
		Size: 1.6 KB (1628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c0ce459c9789d09aa48270214826225742d862f5a01ff5c3aa911fac53f4240`  
		Last Modified: Fri, 30 May 2025 20:49:21 GMT  
		Size: 638.9 KB (638871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:778608fb5b0c94a73ad38eeccf815fdd89e7005595678cbcce642a17c53320ad`  
		Last Modified: Fri, 30 May 2025 20:49:21 GMT  
		Size: 330.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:3-alpine3.22` - unknown; unknown

```console
$ docker pull bash@sha256:264c03623f3372326e29b56a7a824e1745ddd78eab66f0f5607914b4f43a28f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.6 KB (142635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ab50af37be0e8a16043597735d24d103bb4795b382fb1a1df0a5e6f6c9ccffd`

```dockerfile
```

-	Layers:
	-	`sha256:a15eea85f3738c6bb65901082fefea9811f18ed0b4c86d6b667165b0833db167`  
		Last Modified: Fri, 30 May 2025 20:49:21 GMT  
		Size: 118.9 KB (118946 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:464a9c942d652a6cd518bedd5606e1e2230dea2bb98e7a902606b4d935746818`  
		Last Modified: Fri, 30 May 2025 20:49:21 GMT  
		Size: 23.7 KB (23689 bytes)  
		MIME: application/vnd.in-toto+json
