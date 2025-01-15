## `bash:devel-alpine3.21`

```console
$ docker pull bash@sha256:c934944ff8bda3946c6111f822cbcd30a84ca8f1bc7993810cae8bbbb701123d
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

### `bash:devel-alpine3.21` - linux; amd64

```console
$ docker pull bash@sha256:67c230ffaa3c5b10ec7208053870bc5890902a158cc2c109bf704df65aadd29a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6591088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:890b0afd5343c396999b8fd09d541226e6b03699bbd5800a364f1ea4b9c222d4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Tue, 14 Jan 2025 05:18:08 GMT
ENV _BASH_COMMIT=2ea356081dbfbac2c791f9b8072ed4b824e3d9df
# Tue, 14 Jan 2025 05:18:08 GMT
ENV _BASH_VERSION=devel-20250109
# Tue, 14 Jan 2025 05:18:08 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 14 Jan 2025 05:18:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 14 Jan 2025 05:18:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 05:18:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Jan 2025 05:18:08 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1de555d55d2a18554ef9be62c0af2cecde69352bc8e9e9f84422234027e0f9bf`  
		Last Modified: Tue, 14 Jan 2025 20:28:14 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:242cd21478df193367a2a52b19dafc0a8bc4f79e98b31acf1708380d823bc647`  
		Last Modified: Tue, 14 Jan 2025 20:28:14 GMT  
		Size: 2.9 MB (2948579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:419e1813b60b26ab9f85300581dfb4e4be2ec415e4dd3a9386f23fb3f892fd40`  
		Last Modified: Tue, 14 Jan 2025 20:28:14 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.21` - unknown; unknown

```console
$ docker pull bash@sha256:7cffaefcb79f7301bfee7572b06a551f0ab0a4bd78c4de6910e80911490b672b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.6 KB (132571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a07915289c03a37b3fe24d22ee5375bf47176a01fd09455df539fdb2d13e193`

```dockerfile
```

-	Layers:
	-	`sha256:7b94927eb2c0fb3e67a629e0fdd894bd6e73ff35ab3a32106494c762ae9679e8`  
		Last Modified: Tue, 14 Jan 2025 20:28:14 GMT  
		Size: 114.9 KB (114922 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a240e7e61c47f3818f89952986c51afbaa5bbaab6e560b1d7decf9714f80f514`  
		Last Modified: Tue, 14 Jan 2025 20:28:14 GMT  
		Size: 17.6 KB (17649 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.21` - linux; arm variant v6

```console
$ docker pull bash@sha256:aeb7b8b09c7ba9a29d67a228e385ab8edd30018c069b5e2167f76a76e673b0fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6250467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d72e4b930910bceb12c541df5af6bc8a426cab7e4e0bf3a1a757bc736bd9d86`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Tue, 14 Jan 2025 05:18:08 GMT
ENV _BASH_COMMIT=2ea356081dbfbac2c791f9b8072ed4b824e3d9df
# Tue, 14 Jan 2025 05:18:08 GMT
ENV _BASH_VERSION=devel-20250109
# Tue, 14 Jan 2025 05:18:08 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 14 Jan 2025 05:18:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 14 Jan 2025 05:18:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 05:18:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Jan 2025 05:18:08 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:d3e229a4bb72770bd404e0f6590519a8e566146523e984834c6a3d82836f0069`  
		Last Modified: Wed, 08 Jan 2025 17:23:44 GMT  
		Size: 3.4 MB (3363879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30df67167d1632c1a6da7d7229864f0609dc42113df896a226fec5ace7d08e24`  
		Last Modified: Wed, 08 Jan 2025 18:07:26 GMT  
		Size: 459.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfb7d1f34d070c3bc126bcb0e31a4276f3b4abadeff015c8971ab51a90214b67`  
		Last Modified: Tue, 14 Jan 2025 20:28:20 GMT  
		Size: 2.9 MB (2885792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f71c6b012fef221ad20978f9e44f5666ca652f6408078fc7839e28b8622b7e48`  
		Last Modified: Tue, 14 Jan 2025 20:28:19 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.21` - unknown; unknown

```console
$ docker pull bash@sha256:bcd37f25d54afdcb430707d271144dee9577c3c5e0f3226d96e91430970075e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 KB (17510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2b4da449fc57a0f016724919ef338227d7344a08c6b908c2d7c0da3908ad054`

```dockerfile
```

-	Layers:
	-	`sha256:3b8850f405b65e1ef651fd31961e3b6c1f4ba5f6c7975ee9b13eb6e43abdd995`  
		Last Modified: Tue, 14 Jan 2025 20:28:19 GMT  
		Size: 17.5 KB (17510 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.21` - linux; arm variant v7

```console
$ docker pull bash@sha256:51c51909c2207a5823a4d8c9ce4f8fa04baf4ab48cf746dc9bcf3ff65c44c83c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5935090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe4f8fc888575efd7177f923483d8eb5b9d1d55c587e0000b6a39d06c611b374`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armv7.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Tue, 14 Jan 2025 05:18:08 GMT
ENV _BASH_COMMIT=2ea356081dbfbac2c791f9b8072ed4b824e3d9df
# Tue, 14 Jan 2025 05:18:08 GMT
ENV _BASH_VERSION=devel-20250109
# Tue, 14 Jan 2025 05:18:08 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 14 Jan 2025 05:18:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 14 Jan 2025 05:18:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 05:18:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Jan 2025 05:18:08 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:824bc99f06f2c6bebc1172ff7e39d7a1cdbd077ec44632079a629f69e9db7abf`  
		Last Modified: Wed, 08 Jan 2025 17:34:01 GMT  
		Size: 3.1 MB (3097112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d3d2fdc30c5f6606f38c2be797bae397d151f4f1ee7e78e1ab4868fb463f4a0`  
		Last Modified: Wed, 08 Jan 2025 18:23:46 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59a9b000361dfcc7de7dd9f9c0bc7f9edf6159cc67ddc3ac7aea640a42a79f3f`  
		Last Modified: Tue, 14 Jan 2025 21:52:36 GMT  
		Size: 2.8 MB (2837185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ae47bd5a39a1f42cb26f9a40f4c4508ea77b4ff75aa633b77b9bec341c27f0a`  
		Last Modified: Tue, 14 Jan 2025 21:52:36 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.21` - unknown; unknown

```console
$ docker pull bash@sha256:bd80ad3e0b475983d8acab548a391dd6a076222a85a2740aa6ec6e1ade2773e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.7 KB (132683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f446e5efc039149d1f757ed5aa99dbcbb1ac541142b779fc892e7ac696a403a`

```dockerfile
```

-	Layers:
	-	`sha256:171219ae95bcde5354b6abeecb58c1871f87a982bc8e0702d0cebbdecf3d8d52`  
		Last Modified: Tue, 14 Jan 2025 21:52:36 GMT  
		Size: 115.0 KB (114958 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a7b92d106bc9f5b76c5c137ddb4e84ac350ea6d2efa6a9b9dbebb22c5f20b95`  
		Last Modified: Tue, 14 Jan 2025 21:52:36 GMT  
		Size: 17.7 KB (17725 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull bash@sha256:982b180c96e921d57b465fddbaca65a5550f00d4b8be91b163e644ccc79ea02c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7026401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79137cdfa8c1f39f0725635a253149910f89edd6dd8017d242dc8847bffccf95`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Tue, 14 Jan 2025 05:18:08 GMT
ENV _BASH_COMMIT=2ea356081dbfbac2c791f9b8072ed4b824e3d9df
# Tue, 14 Jan 2025 05:18:08 GMT
ENV _BASH_VERSION=devel-20250109
# Tue, 14 Jan 2025 05:18:08 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 14 Jan 2025 05:18:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 14 Jan 2025 05:18:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 05:18:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Jan 2025 05:18:08 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c609346feefd24f529f25fd37883c8f54483d60d36f9cf7bc7e058e6699b4437`  
		Last Modified: Wed, 15 Jan 2025 01:24:58 GMT  
		Size: 458.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33d1893916dbfe440cf0722d53205a5ffc6f03491bdf023a4e690aae3a954141`  
		Last Modified: Wed, 15 Jan 2025 01:24:59 GMT  
		Size: 3.0 MB (3033247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b9df302663e4413c36ce0d809d045c3afaafb6f9768e63094698bdfd908b149`  
		Last Modified: Wed, 15 Jan 2025 01:24:58 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.21` - unknown; unknown

```console
$ docker pull bash@sha256:84a188337d3ebf2ff9d7232e09746920eafdef41a0c2067c23a640cdb9fe2d08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.7 KB (132730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22b0d54f37c50bf12586349d4a535ca73d7670440856e99e354f214df521a077`

```dockerfile
```

-	Layers:
	-	`sha256:5c135183d445674bd960319a28e26b19f91b0b30efca01cc39d4cc28b77b30ed`  
		Last Modified: Wed, 15 Jan 2025 01:24:58 GMT  
		Size: 115.0 KB (114978 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f68ccfa70e4ab23b9deb1a911e97cad56e78984751bc5c40ce3593bca20c4dc`  
		Last Modified: Wed, 15 Jan 2025 01:24:58 GMT  
		Size: 17.8 KB (17752 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.21` - linux; 386

```console
$ docker pull bash@sha256:8f58dbe6047b6d49319af988f5705576fda13f57d910218af6c33250538b9c83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6338830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4671834e4aa6fa1b5f6350805d458d16885c992c00b989a4b78d05a202719e43`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Tue, 14 Jan 2025 05:18:08 GMT
ENV _BASH_COMMIT=2ea356081dbfbac2c791f9b8072ed4b824e3d9df
# Tue, 14 Jan 2025 05:18:08 GMT
ENV _BASH_VERSION=devel-20250109
# Tue, 14 Jan 2025 05:18:08 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 14 Jan 2025 05:18:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 14 Jan 2025 05:18:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 05:18:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Jan 2025 05:18:08 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:dbaac2331104495e5df0818a1db05c402cfc13af140c75beccf51922d5f37ad5`  
		Last Modified: Wed, 08 Jan 2025 17:23:36 GMT  
		Size: 3.5 MB (3463126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2dc0f19d21068152bdd9c5bf08bb1b5163494ebd5de975a580f9fd0939be4b5`  
		Last Modified: Tue, 14 Jan 2025 20:27:57 GMT  
		Size: 458.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b33c675530a98b9aa2ae95d35e5b204bc4f82e257508cab3aa13b208490a7104`  
		Last Modified: Tue, 14 Jan 2025 20:27:57 GMT  
		Size: 2.9 MB (2874912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7124b29eb4b6fbe551b79056b2a63e8a15b6620b450888ef89ab76b0591913c`  
		Last Modified: Tue, 14 Jan 2025 20:27:57 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.21` - unknown; unknown

```console
$ docker pull bash@sha256:c7147b7b55d877afaa33b5181d012aac2b78673b5b4782a6bdbc45918c297b7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.5 KB (132514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9881b1746d450eaa18860478effe53383143013215e004212f74a63da077aa7`

```dockerfile
```

-	Layers:
	-	`sha256:299ef5cbf65f0bf22615e72d0599e2b58be7efa9ce93ebad1573bb344e850997`  
		Last Modified: Tue, 14 Jan 2025 20:27:57 GMT  
		Size: 114.9 KB (114897 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49e5b9e6aae93786afb561927d85a593856a90c7da5583974ff4ab9717e09232`  
		Last Modified: Tue, 14 Jan 2025 20:27:57 GMT  
		Size: 17.6 KB (17617 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.21` - linux; ppc64le

```console
$ docker pull bash@sha256:152312d816a99225272f7f9c2b97152e56f0ea892055e447ea421d9521011164
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6791530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be2c615fb344b8d95e0dc8092a53e5e1928509088f692f9f214c98e6840672c7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Tue, 14 Jan 2025 05:18:08 GMT
ENV _BASH_COMMIT=2ea356081dbfbac2c791f9b8072ed4b824e3d9df
# Tue, 14 Jan 2025 05:18:08 GMT
ENV _BASH_VERSION=devel-20250109
# Tue, 14 Jan 2025 05:18:08 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 14 Jan 2025 05:18:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 14 Jan 2025 05:18:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 05:18:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Jan 2025 05:18:08 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:244ac55e5ecd413dee99efe3ace7cb84420bfc9a727ec2327dae7805045d7470`  
		Last Modified: Wed, 08 Jan 2025 17:24:16 GMT  
		Size: 3.6 MB (3573601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba2864eb05966c89ecc2f693f15dd35b154f22759821c1d4a8757dec136d82aa`  
		Last Modified: Wed, 08 Jan 2025 17:58:42 GMT  
		Size: 458.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ceaf5a80b7a5af71d94ffaff4e9c980add2eaf653961c311171c16704a3c820`  
		Last Modified: Tue, 14 Jan 2025 20:31:35 GMT  
		Size: 3.2 MB (3217134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd54ec10580ff3e30a0b69632334e8f58d7cc9902d5b84d27e53188d38559ca3`  
		Last Modified: Tue, 14 Jan 2025 20:31:35 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.21` - unknown; unknown

```console
$ docker pull bash@sha256:75f8737f206c4b360cff6960d10ed7ee353ac9b2f01dd9dfac0ec78b809de7e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.7 KB (130698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12007e6fca045a8911e24d70224fd715656c49f542526938bc87fde04ca4c23e`

```dockerfile
```

-	Layers:
	-	`sha256:29f3ea7cc991f7d0dcafe417a903875160a3ffece498f8cf02eada5b7320c325`  
		Last Modified: Tue, 14 Jan 2025 20:31:35 GMT  
		Size: 113.0 KB (113005 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b12f4237c9a7ffbc1435c4d22b258e8eeaaf09e4a5358155d3647ef3e2dda57`  
		Last Modified: Tue, 14 Jan 2025 20:31:35 GMT  
		Size: 17.7 KB (17693 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.21` - linux; riscv64

```console
$ docker pull bash@sha256:081534954d6e6dd160e0dd127200016d278cd977f926013e9f9d0a1a2355bc78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6250624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dad926f94e1b39dc03e83a60708b73b3089b705a0e1241f65a5b43a4a7a5c6d2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-riscv64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Tue, 14 Jan 2025 05:18:08 GMT
ENV _BASH_COMMIT=2ea356081dbfbac2c791f9b8072ed4b824e3d9df
# Tue, 14 Jan 2025 05:18:08 GMT
ENV _BASH_VERSION=devel-20250109
# Tue, 14 Jan 2025 05:18:08 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 14 Jan 2025 05:18:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 14 Jan 2025 05:18:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 05:18:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Jan 2025 05:18:08 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:21a89fc8a7107842fa0935d999d700ca9a9df964110a7076d946b16f07a54de5`  
		Last Modified: Wed, 08 Jan 2025 17:48:43 GMT  
		Size: 3.4 MB (3350256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cee5ec45bdf477db840352ec8979a5377f81b57c5bd134c10ef0dd422448e2c3`  
		Last Modified: Wed, 08 Jan 2025 18:10:13 GMT  
		Size: 459.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4039f8cd00171df09406181873e7c4cbffecad03dfac827a52a5c02129402dd7`  
		Last Modified: Tue, 14 Jan 2025 20:56:22 GMT  
		Size: 2.9 MB (2899568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a53ac5c8e0f751a2591945bd46372aaee3a9adebdfca74ebf03488db3a2b56d`  
		Last Modified: Tue, 14 Jan 2025 20:56:21 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.21` - unknown; unknown

```console
$ docker pull bash@sha256:6dc519a19dedc3baf80ce51e567c1b5ed2613684a21eee497d49ed0a44d76f79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.7 KB (130694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09737f81a733e4a23c084ba31118056322e3203a9abd8956d3d1929074718090`

```dockerfile
```

-	Layers:
	-	`sha256:1908cba360ee42a5946e60bfa1e36eb488fccbfdbdd1e3dd10194e071ab4d7a8`  
		Last Modified: Tue, 14 Jan 2025 20:56:21 GMT  
		Size: 113.0 KB (113001 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0cdb6a941594f06f9dbb9d43407885c32169be85ac8abfbc88c3ce823797e200`  
		Last Modified: Tue, 14 Jan 2025 20:56:21 GMT  
		Size: 17.7 KB (17693 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.21` - linux; s390x

```console
$ docker pull bash@sha256:54b0819c429763d111bf6008fcc3cfb5d6039a57003cde3351d9adf203f0ef94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6511327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5662f55a100e6f8314d3fe0997f64a8abc4c476cb353476a3a9f4ceadc3ccc4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-s390x.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Tue, 14 Jan 2025 05:18:08 GMT
ENV _BASH_COMMIT=2ea356081dbfbac2c791f9b8072ed4b824e3d9df
# Tue, 14 Jan 2025 05:18:08 GMT
ENV _BASH_VERSION=devel-20250109
# Tue, 14 Jan 2025 05:18:08 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 14 Jan 2025 05:18:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 14 Jan 2025 05:18:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 05:18:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Jan 2025 05:18:08 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:b2af93686f9384c40cfe861d7173877bb2ee1675c3ee70181799693c34c8722f`  
		Last Modified: Wed, 08 Jan 2025 17:25:12 GMT  
		Size: 3.5 MB (3466867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5a540196e840d845bf43b1d53eef177cb5b4cb8a0d8c3c3d0ed9a38955a9f84`  
		Last Modified: Wed, 08 Jan 2025 17:58:08 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed1fb575a1b03f8cee41c963577509ac776418bf2a65a9de0a86c3679436df1f`  
		Last Modified: Tue, 14 Jan 2025 21:59:13 GMT  
		Size: 3.0 MB (3043670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4055ed54b1980fbf078c9e539238481c5b92ff3bc94e85b5d68f6990c3d9e6c`  
		Last Modified: Tue, 14 Jan 2025 21:59:13 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.21` - unknown; unknown

```console
$ docker pull bash@sha256:37c83ce023c9e98f346091e42807a9cc788291ac9a3e08cf9a6e08e1e0a5e95c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.6 KB (130620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b609deea7b6e64d217e2efb1f5d6ffef743b0dd6e66d5a31ad2a39c58218e98b`

```dockerfile
```

-	Layers:
	-	`sha256:6ae07ed138a677f1c210af127a94b5f9de02ed943db5f5c901fc9f09e8523a26`  
		Last Modified: Tue, 14 Jan 2025 21:59:13 GMT  
		Size: 113.0 KB (112971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8894ff8c4a8cd1e3674248de241928a06d3679f29a79acb9c2bb9a3886689ec`  
		Last Modified: Tue, 14 Jan 2025 21:59:13 GMT  
		Size: 17.6 KB (17649 bytes)  
		MIME: application/vnd.in-toto+json
