## `bash:devel`

```console
$ docker pull bash@sha256:a3847d82697b2f24dc7600f2bb952134f481233bae111a3a55ff3ead0aa7fa64
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

### `bash:devel` - linux; amd64

```console
$ docker pull bash@sha256:2e993ae534e819417d337041d2b81c72eb413d2c63b1fd02b9d14fbaf5f7322e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6890235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9528b67408668def989940a1bb888c29a893f56e505a307f7d83ae7432bdc776`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Tue, 31 Mar 2026 19:03:54 GMT
ENV _BASH_COMMIT=55f721c51e2d7999144b28cb2e97d1d077d1d1ef
# Tue, 31 Mar 2026 19:03:54 GMT
ENV _BASH_VERSION=devel-20260324
# Tue, 31 Mar 2026 19:03:54 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 31 Mar 2026 19:04:31 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 31 Mar 2026 19:04:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 31 Mar 2026 19:04:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 31 Mar 2026 19:04:31 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79526b33335949548866ef5830e110682ff485c44a64e508116e03068d3d6147`  
		Last Modified: Tue, 31 Mar 2026 19:04:36 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f0d66b59266d97113f99cf6c2d424cbe99517714134768d7f88d2ef75224a5a`  
		Last Modified: Tue, 31 Mar 2026 19:04:36 GMT  
		Size: 3.0 MB (3027621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73a19215d1e1079efc306137f934a3b8bfc84d368b6c7b4c8fbc023e648dbf1b`  
		Last Modified: Tue, 31 Mar 2026 19:04:36 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:06b6db50e7aa1117fca7e101cfec3afe43a2fc6bd0c337bcac83a6050ec9aba0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.1 KB (135145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57b7416f51a9041013552d59816903c614c2f13abf8f10428419696fedbba66c`

```dockerfile
```

-	Layers:
	-	`sha256:5af1e786f38b65b727d768eede7a52ff0c99ed9f037d75f6af59ec2526633e2f`  
		Last Modified: Tue, 31 Mar 2026 19:04:36 GMT  
		Size: 117.1 KB (117122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f92505a03f657d6e454e3532f454774f8de90e677e78aefc8fac6274a17e933`  
		Last Modified: Tue, 31 Mar 2026 19:04:36 GMT  
		Size: 18.0 KB (18023 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; arm variant v6

```console
$ docker pull bash@sha256:8d55a484b345f28b15f71cdaf52253a80897a948b8a23e954b1c624c3543fc88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6557568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3632f112c87cbd45ef271605e11358c9b2f0b0fc6f43a5a1611677db370cfaf9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Tue, 31 Mar 2026 19:03:40 GMT
ENV _BASH_COMMIT=55f721c51e2d7999144b28cb2e97d1d077d1d1ef
# Tue, 31 Mar 2026 19:03:40 GMT
ENV _BASH_VERSION=devel-20260324
# Tue, 31 Mar 2026 19:03:40 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 31 Mar 2026 19:04:22 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 31 Mar 2026 19:04:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 31 Mar 2026 19:04:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 31 Mar 2026 19:04:22 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02190fd29f66ae0d241651d948ed7f5946025ac8d293768c986e859e37a87cfc`  
		Last Modified: Tue, 31 Mar 2026 19:04:26 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5e4af2b2fa392b220018ef429a8a509b705fd9e69a71a2ac3478783b28057ab`  
		Last Modified: Tue, 31 Mar 2026 19:04:26 GMT  
		Size: 3.0 MB (2986957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:997c4a82a0938333cc6b0e365e75a1b2f6eed469542d33233f6db79c8bb7c146`  
		Last Modified: Tue, 31 Mar 2026 19:04:26 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:6c8a93ccb0fae878f4624386c1070265211701bc4d1e88d053d1b054a1f621c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 KB (17889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb4ab9191e364246a08d591071dd3b075e169dc97bcaa8a24c8d3222c359f556`

```dockerfile
```

-	Layers:
	-	`sha256:f6a74079866e2904bfc6d9b16cde892974c6638534d923e63413e8a44616fb1d`  
		Last Modified: Tue, 31 Mar 2026 19:04:26 GMT  
		Size: 17.9 KB (17889 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; arm variant v7

```console
$ docker pull bash@sha256:bcf2494368cb6629fec14f7587314db45be289fee49bcb3f46314aa8e7e6faac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6219149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f294a608b692763beacbc5c7505fbe041794978d02912584bc078438815d44f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Tue, 31 Mar 2026 19:03:40 GMT
ENV _BASH_COMMIT=55f721c51e2d7999144b28cb2e97d1d077d1d1ef
# Tue, 31 Mar 2026 19:03:40 GMT
ENV _BASH_VERSION=devel-20260324
# Tue, 31 Mar 2026 19:03:40 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 31 Mar 2026 19:04:23 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 31 Mar 2026 19:04:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 31 Mar 2026 19:04:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 31 Mar 2026 19:04:23 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67aff95bca706709cf64d8c04e32df6f7e160f34ccc39f531c4e04b823e8131e`  
		Last Modified: Tue, 31 Mar 2026 19:04:29 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b991fbaac229ee6e369f27b50c0d1d6e764d8b241d94b40df99b6d1111ac0cd7`  
		Last Modified: Tue, 31 Mar 2026 19:04:29 GMT  
		Size: 2.9 MB (2936636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03241312e41d13f8b5395f6f8d8b94be3731b04bc60e61f44ceabec9eac13448`  
		Last Modified: Tue, 31 Mar 2026 19:04:28 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:dee77ddb416f15483a6a1db33d8bc1e1c488e04cfb33a264e69c70eaa6085407
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.6 KB (134612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e0137ea99853a9811cfa409eac17c8ef5222a915253f68e6eee3b110d3b3e70`

```dockerfile
```

-	Layers:
	-	`sha256:f4d81ab9c08848acc9a529e303c188091110555c9ce0d3a373ecdf4acc570354`  
		Last Modified: Tue, 31 Mar 2026 19:04:28 GMT  
		Size: 116.5 KB (116508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9bbdb87c013e7bc91a90b477cf58224018b730a6f5b71ee0cb848d6e33a25e65`  
		Last Modified: Tue, 31 Mar 2026 19:04:29 GMT  
		Size: 18.1 KB (18104 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; arm64 variant v8

```console
$ docker pull bash@sha256:aadf1c3623f57b5a7de26888ffbb78b72930f38723cb5f577d4aeddeed131b72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7295577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:099eebac3eb6fbbc3227eb76eee91183ae9e56811d51d550a8f15f859aa17129`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Tue, 31 Mar 2026 19:04:19 GMT
ENV _BASH_COMMIT=55f721c51e2d7999144b28cb2e97d1d077d1d1ef
# Tue, 31 Mar 2026 19:04:19 GMT
ENV _BASH_VERSION=devel-20260324
# Tue, 31 Mar 2026 19:04:19 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 31 Mar 2026 19:04:59 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 31 Mar 2026 19:04:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 31 Mar 2026 19:04:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 31 Mar 2026 19:04:59 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d526998d43f54ae762c941fcfacddf6971fb8c699d2cbd49d27d6d4cd5c29d6d`  
		Last Modified: Tue, 31 Mar 2026 19:05:04 GMT  
		Size: 458.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:300d6e1561d415de6feba29b61a39e45cc17bcddcd7cabe849cb2076981a3d7d`  
		Last Modified: Tue, 31 Mar 2026 19:05:05 GMT  
		Size: 3.1 MB (3097695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f44f7c1c1d98a254b6c7491149fd606d8436f93e2cf38077ba6db8ed902044c8`  
		Last Modified: Tue, 31 Mar 2026 19:05:05 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:2f64f52fb8b9fb616379a7730174023efeff13de540f4c4d392681749d8c738f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 KB (134655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8969b41677eb19559a1b6cb1a8dd2ec225fb87c28a01aa683a2efa15c3f45075`

```dockerfile
```

-	Layers:
	-	`sha256:1f2b6b09294e64fcc3a25c6591f6c661f3873e833b48f13ddc5c3277d9a0ce64`  
		Last Modified: Tue, 31 Mar 2026 19:05:04 GMT  
		Size: 116.5 KB (116528 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddffc91259ece62f386ca41f9903b6b7469db7d99bb94f6b9b5033981ac5e577`  
		Last Modified: Tue, 31 Mar 2026 19:05:04 GMT  
		Size: 18.1 KB (18127 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; 386

```console
$ docker pull bash@sha256:fb2264fb92be428a26c095aaaa2cd26c3a5948795565fcc0c92613d3c4af3b07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6642104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e381f5cd26a9ea33edf46ae4ff305ebf7f5dab559c4ec6bbd74f704cf1bf3823`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:11 GMT
ADD alpine-minirootfs-3.23.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:11 GMT
CMD ["/bin/sh"]
# Tue, 31 Mar 2026 19:05:04 GMT
ENV _BASH_COMMIT=55f721c51e2d7999144b28cb2e97d1d077d1d1ef
# Tue, 31 Mar 2026 19:05:04 GMT
ENV _BASH_VERSION=devel-20260324
# Tue, 31 Mar 2026 19:05:04 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 31 Mar 2026 19:05:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 31 Mar 2026 19:05:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 31 Mar 2026 19:05:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 31 Mar 2026 19:05:40 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:18bdec7eea78464ecf9b88f4ec630eaeb694ea1c0101ecd9c20eda20c9065e23`  
		Last Modified: Wed, 28 Jan 2026 01:18:16 GMT  
		Size: 3.7 MB (3686998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1246a899e88b1c1f57fc84beb6e42beaac83c15451f6aec987abee32fe52f32f`  
		Last Modified: Tue, 31 Mar 2026 19:05:45 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efe3474e59191b2dd2eec2ae3b878784211aae33733f525d546682e369af50b8`  
		Last Modified: Tue, 31 Mar 2026 19:05:45 GMT  
		Size: 3.0 MB (2954318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:217b8396405822065052e91b5d42259af988274c54e2adeaa2e6e447d59739ea`  
		Last Modified: Tue, 31 Mar 2026 19:05:45 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:ba2a7ca253e2b69d79b834e288cc8973c19c5c43effa4e8972bff4f50c3abf07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.1 KB (135089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f677c2fc10d7d8404380aea1f1087bdc832b17bee39eb1abd646999f1d2c6485`

```dockerfile
```

-	Layers:
	-	`sha256:9fd940da8a3d7b552c3cdd66b802588e363373b179c0ec172bdac0ad7a8972f7`  
		Last Modified: Tue, 31 Mar 2026 19:05:45 GMT  
		Size: 117.1 KB (117097 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a970470662fc873c8044de782050b7c8625c01d1f42d85d9e4645e3cdf1fc68`  
		Last Modified: Tue, 31 Mar 2026 19:05:45 GMT  
		Size: 18.0 KB (17992 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; ppc64le

```console
$ docker pull bash@sha256:a646a5c5cc0ccb8df81dcb7c2f2431d7bd462a53e04e5daeec0e5ba4cc3a8e7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7168280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:201e93aaf6ca0fb1a6f3fc6368d1838926723202c60229b16928481572a09f47`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Tue, 31 Mar 2026 19:03:22 GMT
ENV _BASH_COMMIT=55f721c51e2d7999144b28cb2e97d1d077d1d1ef
# Tue, 31 Mar 2026 19:03:22 GMT
ENV _BASH_VERSION=devel-20260324
# Tue, 31 Mar 2026 19:03:22 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 31 Mar 2026 19:04:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 31 Mar 2026 19:04:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 31 Mar 2026 19:04:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 31 Mar 2026 19:04:25 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c08bb691418e5a32a0c8f94624fdea6c8d5682f809119847a1041ea14c05810`  
		Last Modified: Tue, 31 Mar 2026 19:04:34 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5f0720ffb3ed599edf025359ce56faa06c2c3ae02abf8403e302dcdcb7c13c3`  
		Last Modified: Tue, 31 Mar 2026 19:04:34 GMT  
		Size: 3.3 MB (3337843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c396be0ffcb43daf06dfdbe83f8a006734c430c5d9f2693401d4f7b61417042`  
		Last Modified: Tue, 31 Mar 2026 19:04:34 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:9a126c1ca9c840bebe8c68539e334376142623a322a8036144813e38972f9597
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.6 KB (134573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90d8d538e5502a09ba4559b5822d1b0c6ae2c39837e62d4449a81503011aab93`

```dockerfile
```

-	Layers:
	-	`sha256:a1b9af502d006d9e47f8b85e6d6d7834c18ca7d8c21b4bf1dde6ee11dfc3541c`  
		Last Modified: Tue, 31 Mar 2026 19:04:34 GMT  
		Size: 116.5 KB (116505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e07b79fff343821ecc180f38d530f3dd8b8f180a9057f814888699b7b7fdbd2`  
		Last Modified: Tue, 31 Mar 2026 19:04:34 GMT  
		Size: 18.1 KB (18068 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; riscv64

```console
$ docker pull bash@sha256:d8fb17e2d5d9a0c324027a9db0204f6a11774fbc7765386e918b38cd3b5b0cb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6804665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8311d80506a57eceae2b635018e96a766fd56bc80a95fb2c9e5b433fe0324a0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Tue, 31 Mar 2026 19:02:59 GMT
ENV _BASH_COMMIT=55f721c51e2d7999144b28cb2e97d1d077d1d1ef
# Tue, 31 Mar 2026 19:02:59 GMT
ENV _BASH_VERSION=devel-20260324
# Tue, 31 Mar 2026 19:02:59 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 31 Mar 2026 19:12:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 31 Mar 2026 19:12:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 31 Mar 2026 19:12:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 31 Mar 2026 19:12:12 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3e2dbde469253cfcf4eaebf5f3d3b7312e489891f20cf42fca2d5f662448f9b`  
		Last Modified: Tue, 31 Mar 2026 19:12:37 GMT  
		Size: 460.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8177eb952d03a3cbd43622e4fd7151c4593962e4d1029a034d04ac6dc2974cd0`  
		Last Modified: Tue, 31 Mar 2026 19:12:37 GMT  
		Size: 3.2 MB (3218577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4782bc18d0d912a84461bf4897c963951484b45c6716a2b87500e3d2d6c0b796`  
		Last Modified: Tue, 31 Mar 2026 19:12:37 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:ffce7374bf69fd5440c03635825d65964698df0b89d01ace6182f0b336b18df8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.6 KB (134569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac7aef37d3aba3ba73ec7a8fecf3e239add9d7513ac68f5ad2b05e07973fbadd`

```dockerfile
```

-	Layers:
	-	`sha256:ff503d43e1da106ffd6159cf8b40b266564741453501da695a280c86e38b8003`  
		Last Modified: Tue, 31 Mar 2026 19:12:37 GMT  
		Size: 116.5 KB (116501 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3d980c4bcb47a05f3d38932438e06e36be151fa0097c36b36fc74aa22209c41`  
		Last Modified: Tue, 31 Mar 2026 19:12:37 GMT  
		Size: 18.1 KB (18068 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; s390x

```console
$ docker pull bash@sha256:5a80bd08765e8881904b786a5f6b89b98a4a2a5491bbc34ff32b62d29816174b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6846157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01d6e57ee8dfa2b8164cb5c7cf2ca4da348dce67f6b459f5147ceff539564ff7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Tue, 31 Mar 2026 19:03:30 GMT
ENV _BASH_COMMIT=55f721c51e2d7999144b28cb2e97d1d077d1d1ef
# Tue, 31 Mar 2026 19:03:30 GMT
ENV _BASH_VERSION=devel-20260324
# Tue, 31 Mar 2026 19:03:30 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 31 Mar 2026 19:04:18 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 31 Mar 2026 19:04:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 31 Mar 2026 19:04:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 31 Mar 2026 19:04:18 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a3cbf10c5c3c10a8db5dfd88d5b9a92e941b9ff73726e7336bf59079e9237fd`  
		Last Modified: Tue, 31 Mar 2026 19:04:26 GMT  
		Size: 458.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1bb8b71242c832b0185623c276e32c2922decbd330d5313feab446c978e1829`  
		Last Modified: Tue, 31 Mar 2026 19:04:27 GMT  
		Size: 3.1 MB (3120031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6232bc46f79d431d4d937a4587fb5f5aad167dc2beb30261b04b3222a3e00265`  
		Last Modified: Tue, 31 Mar 2026 19:04:26 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:cad0b1e1fe6e23648af0324f829f6224c2ec8df1d270d6627fa84fee64e246bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.5 KB (134494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93acbb38b0d5a2c09dc6b1cbe611f9bca3ce5b4af6a1dc1ff9f88fcbf5b0dfe6`

```dockerfile
```

-	Layers:
	-	`sha256:1c8b0b87b853a816c28e4724cd48e955ee4c7e71d3ac06a2da22c1f16026f4c5`  
		Last Modified: Tue, 31 Mar 2026 19:04:26 GMT  
		Size: 116.5 KB (116471 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e9415e6cca83f21b2ad8cdb2cf23f123c1567e1c2bdd9ebd4b96ff298350776`  
		Last Modified: Tue, 31 Mar 2026 19:04:26 GMT  
		Size: 18.0 KB (18023 bytes)  
		MIME: application/vnd.in-toto+json
