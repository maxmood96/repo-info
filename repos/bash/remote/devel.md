## `bash:devel`

```console
$ docker pull bash@sha256:ce81cb2c54c50c497033f0a965b56821e10c4d3d4bebe526278487f2c12a92ee
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
$ docker pull bash@sha256:52f1bacc7971d292f948fc065e8878c8e412846cdcac186c7087e90a099b0ac0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6806666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02d0eba8284834cac6945cea1b9addc300522f968beeef0abc2c2bb01dea54f4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 07 Oct 2025 04:18:10 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Tue, 07 Oct 2025 04:18:10 GMT
CMD ["/bin/sh"]
# Tue, 07 Oct 2025 04:18:10 GMT
ENV _BASH_COMMIT=25c6aa5b230167c6471898539c46dd2891d891a5
# Tue, 07 Oct 2025 04:18:10 GMT
ENV _BASH_VERSION=devel-20251006
# Tue, 07 Oct 2025 04:18:10 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 07 Oct 2025 04:18:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 07 Oct 2025 04:18:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Oct 2025 04:18:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Oct 2025 04:18:10 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bedb1ceb6a954e3d76a9989190501096d77ee73e10b0804e1d019bef90867e4`  
		Last Modified: Wed, 08 Oct 2025 23:07:35 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f65e80ec812dcb377751d93cae5a0bc548273bdf6c3a8a4468ffd4ff1dde9ca3`  
		Last Modified: Wed, 08 Oct 2025 23:07:36 GMT  
		Size: 3.0 MB (3003426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0c6fac95a8943e1bd4a2cabc68a857924665d20c2fa123a0df35314e3c49782`  
		Last Modified: Wed, 08 Oct 2025 23:07:35 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:b68b208947ea99024d88572074e3f10c5182c4ec5137e547eaf7154987bc2729
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.6 KB (136575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6627e1aaac96e84fc6607c5517d765ce6c84ced75045e7f4e46f8a52a200c038`

```dockerfile
```

-	Layers:
	-	`sha256:56e7cfab52fedc530f69e08e383553d81dac76bb32abc8b33aba31e933282f1f`  
		Last Modified: Thu, 09 Oct 2025 00:07:44 GMT  
		Size: 118.4 KB (118429 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32b4e04ffa80752d58173db0dc9049225ed9d8e74172a66aec5fbc063f73f447`  
		Last Modified: Thu, 09 Oct 2025 00:07:45 GMT  
		Size: 18.1 KB (18146 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; arm variant v6

```console
$ docker pull bash@sha256:269fc043b29118f62baee080376aeeffb050867efedaa2a4c0a2c1db3122740f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6447173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65521d2736905d8a5ff6665dc461e6feb0313f49357b5cfd75180372250d2d82`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 07 Oct 2025 04:18:10 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Tue, 07 Oct 2025 04:18:10 GMT
CMD ["/bin/sh"]
# Tue, 07 Oct 2025 04:18:10 GMT
ENV _BASH_COMMIT=25c6aa5b230167c6471898539c46dd2891d891a5
# Tue, 07 Oct 2025 04:18:10 GMT
ENV _BASH_VERSION=devel-20251006
# Tue, 07 Oct 2025 04:18:10 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 07 Oct 2025 04:18:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 07 Oct 2025 04:18:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Oct 2025 04:18:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Oct 2025 04:18:10 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfbd7ac2c608893f7e89bf575a3c2fffa970e22f1f715deb58dd6d508c52f66e`  
		Last Modified: Wed, 08 Oct 2025 21:12:28 GMT  
		Size: 460.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e05c6b5fb0fc1c11eda5b175ac7f05348fb6994f12572fa6f8992b9a5b26d905`  
		Last Modified: Wed, 08 Oct 2025 21:12:30 GMT  
		Size: 2.9 MB (2942297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1bde1d0a33e3ce4c4376abfbe0f613732de75e4eb407bd5f983e723316e6dc5`  
		Last Modified: Wed, 08 Oct 2025 21:12:28 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:3474252ba7a4eb3a7b3779e0f7f51e80833f24cd5d0368f522c85f38e23fe060
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (18012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d6154199f51757f5813bc2f6dfed1a8d03f505753caf0990fab90c2fa6859b1`

```dockerfile
```

-	Layers:
	-	`sha256:be90fa8e0d678fd649c6040e6072a789d128216c22ea5ac11b0cb17dc7cb02b4`  
		Last Modified: Thu, 09 Oct 2025 00:07:49 GMT  
		Size: 18.0 KB (18012 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; arm variant v7

```console
$ docker pull bash@sha256:6fbde4526233adf4471ff818f397c72e4746bbe1856f0b2881be78d7bc88c392
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6114918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:710f462beab869e56780100155926537ebe41a280c8c33c6f18e79ef774a88a0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 07 Oct 2025 04:18:10 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Tue, 07 Oct 2025 04:18:10 GMT
CMD ["/bin/sh"]
# Tue, 07 Oct 2025 04:18:10 GMT
ENV _BASH_COMMIT=25c6aa5b230167c6471898539c46dd2891d891a5
# Tue, 07 Oct 2025 04:18:10 GMT
ENV _BASH_VERSION=devel-20251006
# Tue, 07 Oct 2025 04:18:10 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 07 Oct 2025 04:18:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 07 Oct 2025 04:18:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Oct 2025 04:18:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Oct 2025 04:18:10 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b6c501b22d455aeb86c4e16651d1e8e945952a09dba3f20ccd505fc32b09e5f`  
		Last Modified: Wed, 08 Oct 2025 21:21:04 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8402ed639b177f0d90e504d0c5e520b78c6772737cc84b5065d0b02ca49c109e`  
		Last Modified: Wed, 08 Oct 2025 21:21:04 GMT  
		Size: 2.9 MB (2892572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a717ae1922841122bcfdc0497f598cd203247d968ccba9b50660bbbccac35f3f`  
		Last Modified: Wed, 08 Oct 2025 21:21:06 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:81d83148b561399610977f1ee56de40f59321220621718074c31263ebb329939
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.7 KB (136692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:243bdbd9cc85df1d8c2e087bb5e681a85e388cff3cc7abf9f60546857c530e7a`

```dockerfile
```

-	Layers:
	-	`sha256:8828aad7dd472494b7dcbaeea4d1033cbf15d16c040a5025fa8c7ae22d600067`  
		Last Modified: Thu, 09 Oct 2025 00:07:52 GMT  
		Size: 118.5 KB (118465 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6df118c137b5d015d37071a2840579387c846e213a67c7bcf9510c6c6f5af0ef`  
		Last Modified: Thu, 09 Oct 2025 00:07:53 GMT  
		Size: 18.2 KB (18227 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; arm64 variant v8

```console
$ docker pull bash@sha256:9a389e3fd8d3cd3993c2e6f06799e7f07ceaad6744524de2df5c65be933fb51e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7230284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5170c9bdf9e9e42b3c51da13b45b8265493a748a24263c7112121dd1dcfc6681`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 07 Oct 2025 04:18:10 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Tue, 07 Oct 2025 04:18:10 GMT
CMD ["/bin/sh"]
# Tue, 07 Oct 2025 04:18:10 GMT
ENV _BASH_COMMIT=25c6aa5b230167c6471898539c46dd2891d891a5
# Tue, 07 Oct 2025 04:18:10 GMT
ENV _BASH_VERSION=devel-20251006
# Tue, 07 Oct 2025 04:18:10 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 07 Oct 2025 04:18:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 07 Oct 2025 04:18:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Oct 2025 04:18:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Oct 2025 04:18:10 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c4cd909a7c93679da6f24d33d16a75b8f346720fb996da1ea2f7417c0df284e`  
		Last Modified: Wed, 08 Oct 2025 21:13:26 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71e8d5bde9d8a49a06617f8adf98bdfdb1c5a014ed3bc3715edf3300b00cc52e`  
		Last Modified: Wed, 08 Oct 2025 21:13:26 GMT  
		Size: 3.1 MB (3091430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd0119b0fe7a9e89b9370cee0a2b0338e5f911f8f4fc4fb69bdb6c46031732d9`  
		Last Modified: Wed, 08 Oct 2025 21:13:26 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:e8fc29eb84a3ce8043802a80b8a137b4f48daea38a7328d5b4bdf2319dea2c85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.7 KB (136735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59308b4beb9429c6b3f19342811e2897d25b5e80f3a36d5c299edb59e59acf8e`

```dockerfile
```

-	Layers:
	-	`sha256:353d82003e2441d82d85db0b057a133abd8fa852b2cc7a586e7373296371a4b7`  
		Last Modified: Thu, 09 Oct 2025 00:07:56 GMT  
		Size: 118.5 KB (118485 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:636ab667aa9e38699805ca3939a282d29fdf0ec07e68e15b95544fee10375ad9`  
		Last Modified: Thu, 09 Oct 2025 00:07:57 GMT  
		Size: 18.2 KB (18250 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; 386

```console
$ docker pull bash@sha256:89cda3cd2d56d53f23ba67cdd21a3c0bf96fb6c1f65d9c4edf9ac6afd4f3506a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6549272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de3ca209a077847dbadf44cb8e6ebec1fd5ae94b36453c99dc6de9aa842190a7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 07 Oct 2025 04:18:10 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Tue, 07 Oct 2025 04:18:10 GMT
CMD ["/bin/sh"]
# Tue, 07 Oct 2025 04:18:10 GMT
ENV _BASH_COMMIT=25c6aa5b230167c6471898539c46dd2891d891a5
# Tue, 07 Oct 2025 04:18:10 GMT
ENV _BASH_VERSION=devel-20251006
# Tue, 07 Oct 2025 04:18:10 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 07 Oct 2025 04:18:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 07 Oct 2025 04:18:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Oct 2025 04:18:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Oct 2025 04:18:10 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2aa1d858fb5b657c12234028548ba8952cfd584e7281333858e3dcf0a66111a`  
		Last Modified: Wed, 08 Oct 2025 21:14:10 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81ef04fd9cf27ec7d933077c3fe42ed8a544448b6c1d8473cee39aabccc30842`  
		Last Modified: Wed, 08 Oct 2025 21:14:11 GMT  
		Size: 2.9 MB (2929551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10a92ba17d047bf7dfce07257276226fd4f5f2c5287d0d6b46f8eddfccd58d2c`  
		Last Modified: Wed, 08 Oct 2025 21:14:10 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:2dd2c0de69958e757c42e5067369cde6afdcc771835b0f46c7a1c1baed8064d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.5 KB (136519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:510718c58f2dc0f6ab1368a331607c2143fc01441e280ca25ea8b82c9eba5cee`

```dockerfile
```

-	Layers:
	-	`sha256:caf7cb19017aa35ea3328ca98df18ddbb5bb912e0961f75e76ee8780bdcae25a`  
		Last Modified: Thu, 09 Oct 2025 00:08:00 GMT  
		Size: 118.4 KB (118404 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a77a1648208ca94f05e47fd369bc328d22da92ab296e6d6c916051b102c42f9e`  
		Last Modified: Thu, 09 Oct 2025 00:08:01 GMT  
		Size: 18.1 KB (18115 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; ppc64le

```console
$ docker pull bash@sha256:7b23690250822659955dad9fe3f0891990e8e41af78727dd81008e19b47e4a1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7009716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b96f734659f8d652984326edac1815247516531d5664992901e3606c64229ac8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 07 Oct 2025 04:18:10 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Tue, 07 Oct 2025 04:18:10 GMT
CMD ["/bin/sh"]
# Tue, 07 Oct 2025 04:18:10 GMT
ENV _BASH_COMMIT=25c6aa5b230167c6471898539c46dd2891d891a5
# Tue, 07 Oct 2025 04:18:10 GMT
ENV _BASH_VERSION=devel-20251006
# Tue, 07 Oct 2025 04:18:10 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 07 Oct 2025 04:18:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 07 Oct 2025 04:18:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Oct 2025 04:18:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Oct 2025 04:18:10 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69500dfe6b7b000e2cee5c0511b44e509e2a7009d51cdae01b1f6c9420a78a0d`  
		Last Modified: Wed, 08 Oct 2025 21:12:02 GMT  
		Size: 458.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59480d86251ef4f957431f84c6bf7757bf913629e79e2baeb6b1151cae86f396`  
		Last Modified: Wed, 08 Oct 2025 21:12:03 GMT  
		Size: 3.3 MB (3276684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:330d595490a4d04b99ff22e57dd8882f9ef3122081ed05ceacda05279f479a5b`  
		Last Modified: Wed, 08 Oct 2025 21:12:02 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:a8eafa98511d9fccab1f9bb91f4b7d8f6384df642bc9af47f91f6c9d0a080d2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 KB (134702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd742d2e0bc83c16c15ea1ecdc7550504f81b0b250638b8de7b205b7e1ec37af`

```dockerfile
```

-	Layers:
	-	`sha256:ddcfc010cae89a32abea38a70ba54ccdda3edafdff8c997e916f5c1cafc7b2df`  
		Last Modified: Thu, 09 Oct 2025 00:08:05 GMT  
		Size: 116.5 KB (116512 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a782bc34c187ff0072c12b244b2faca13b1fca1d5290a19ba44983b58857845`  
		Last Modified: Thu, 09 Oct 2025 00:08:05 GMT  
		Size: 18.2 KB (18190 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; riscv64

```console
$ docker pull bash@sha256:02e06154f624910ace857de964521e92360f97a188c2f7b763c24b9a159b7151
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6465144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0df1c3d3da81728e6045e0aff938e48e764baba35127af575eae8789fd2b4436`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 07 Oct 2025 04:18:10 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Tue, 07 Oct 2025 04:18:10 GMT
CMD ["/bin/sh"]
# Tue, 07 Oct 2025 04:18:10 GMT
ENV _BASH_COMMIT=25c6aa5b230167c6471898539c46dd2891d891a5
# Tue, 07 Oct 2025 04:18:10 GMT
ENV _BASH_VERSION=devel-20251006
# Tue, 07 Oct 2025 04:18:10 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 07 Oct 2025 04:18:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 07 Oct 2025 04:18:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Oct 2025 04:18:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Oct 2025 04:18:10 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Wed, 08 Oct 2025 21:18:33 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b125a0571d69acffa5c2fc31545cc552342d248d34cc6a400b72035cc99d44e8`  
		Last Modified: Thu, 09 Oct 2025 00:51:35 GMT  
		Size: 459.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58fe7829fe4d446ba75ec610d1ad39956c2945c121bf707f6ee6f66afb2f9530`  
		Last Modified: Thu, 09 Oct 2025 00:51:36 GMT  
		Size: 2.9 MB (2949107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:639ec2b6d16eeb8e3874ee4d6b0e6c0dfc9a1a89f548e0797c1ebc054cdc82a6`  
		Last Modified: Thu, 09 Oct 2025 00:51:36 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:7901d8c5cf4dc4fb0975504f9d6dcb84f6f8242872bd9950f8140525edf82ff6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 KB (134699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32ab9ea046cf5b79d793c2bfe3c3cf88edb08b5bc351fbc3fc7a6a50c4562669`

```dockerfile
```

-	Layers:
	-	`sha256:cb3b0d70f1e39acf59ca4dda02700e0dd62cac5eb7dc2649bad2884602f3f689`  
		Last Modified: Thu, 09 Oct 2025 03:04:53 GMT  
		Size: 116.5 KB (116508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7b2e9e5d3ddce50ead1b365d8347d3a3fe18bf14643fe70168f696315ea2e93`  
		Last Modified: Thu, 09 Oct 2025 03:04:54 GMT  
		Size: 18.2 KB (18191 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; s390x

```console
$ docker pull bash@sha256:19d46c5d66f5dd4815bef96fe1ad40a4389c4ddb14ad498955ddd4143681449d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6743810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e854d097dbc30aaf77746ccc37da956463cbab287598450a4a2f2232946369ab`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 07 Oct 2025 04:18:10 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Tue, 07 Oct 2025 04:18:10 GMT
CMD ["/bin/sh"]
# Tue, 07 Oct 2025 04:18:10 GMT
ENV _BASH_COMMIT=25c6aa5b230167c6471898539c46dd2891d891a5
# Tue, 07 Oct 2025 04:18:10 GMT
ENV _BASH_VERSION=devel-20251006
# Tue, 07 Oct 2025 04:18:10 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 07 Oct 2025 04:18:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 07 Oct 2025 04:18:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Oct 2025 04:18:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Oct 2025 04:18:10 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52542f80f7eac23ac5faaa8542212ddfa07dc162276b5a71a26e1ef9281af9e0`  
		Last Modified: Wed, 08 Oct 2025 21:17:33 GMT  
		Size: 460.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bed56522b0b65afd1bfe1a1bc721739027b0efa143f22e7babc14b7bab8d989`  
		Last Modified: Wed, 08 Oct 2025 21:17:33 GMT  
		Size: 3.1 MB (3093767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d683f76cbb555179c10455b1165e32708d8e46ec3dc52c0e6b088e828c243fd0`  
		Last Modified: Wed, 08 Oct 2025 21:17:33 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:24258d9427a7ee969766600d371d3aea66e06cd2b1f9c92bfa8303d6d483f51b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.6 KB (134625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:630e044f9a5ff805e9a8b459ffbf71253d3827baddc8c910516b46324af1d0c3`

```dockerfile
```

-	Layers:
	-	`sha256:00a7ce71c0ab83824b82519b1a72708e83d77f6853ee2ee2a94a6146106e393b`  
		Last Modified: Thu, 09 Oct 2025 00:08:11 GMT  
		Size: 116.5 KB (116478 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18c63f98defecc620b999abbf03b8a0f3262e9cf80dbed3171b5e15a3b0053b6`  
		Last Modified: Thu, 09 Oct 2025 00:08:12 GMT  
		Size: 18.1 KB (18147 bytes)  
		MIME: application/vnd.in-toto+json
