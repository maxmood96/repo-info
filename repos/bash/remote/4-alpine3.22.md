## `bash:4-alpine3.22`

```console
$ docker pull bash@sha256:996ec8e8546a56c9204f2f891f4514043a27c1c333ddf67b8fd6dc92b11c0af9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; 386
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
		Last Modified: Fri, 30 May 2025 18:04:24 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cca7947b045046ae688c811401f56d768614bd200e041163906d7c900a26a56a`  
		Last Modified: Fri, 30 May 2025 20:49:16 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e1f9ab8520fa557307d941b0fa150b0676d0b4940f6ffba29fa12d3b0043900`  
		Last Modified: Fri, 30 May 2025 20:49:16 GMT  
		Size: 1.1 MB (1077291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc6a9154c1ca8b52a7ad943858a1e759d48ad598a85650b48c99f493bd5357b7`  
		Last Modified: Fri, 30 May 2025 20:49:16 GMT  
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
		Last Modified: Fri, 30 May 2025 20:49:16 GMT  
		Size: 119.0 KB (118981 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:999380a8673956665a770b30166e22b22620abb6b20b50e939d52b1f82b94b1c`  
		Last Modified: Fri, 30 May 2025 20:49:16 GMT  
		Size: 23.5 KB (23496 bytes)  
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
		Last Modified: Fri, 30 May 2025 18:04:26 GMT  
		Size: 3.6 MB (3616029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8a805e00e4bacc440abd6490a521e8725b5ec2a55f15b04a1f78963cbc47665`  
		Last Modified: Fri, 30 May 2025 20:49:41 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d04615467d20e1338b4e40d4eabc9220b50e2033e29deb2766c541150ae9f402`  
		Last Modified: Fri, 30 May 2025 20:49:42 GMT  
		Size: 1.1 MB (1054068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7cb3a05d73cff31c29854d11dca5a9a371d8b4b04ff978469987953c589ec90`  
		Last Modified: Fri, 30 May 2025 20:49:41 GMT  
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
		Last Modified: Fri, 30 May 2025 20:49:42 GMT  
		Size: 118.9 KB (118946 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:343c4f02dd593c988918e849145c92e43dc65e7efc9cc7d974c25d7c87cdc94d`  
		Last Modified: Fri, 30 May 2025 20:49:41 GMT  
		Size: 23.5 KB (23453 bytes)  
		MIME: application/vnd.in-toto+json
