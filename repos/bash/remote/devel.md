## `bash:devel`

```console
$ docker pull bash@sha256:1d4f142396939350e3c9588815f2d181970412d6de46861e2915f85ddf1fffc5
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
$ docker pull bash@sha256:161639abf44878d6fa4cfe1ab457ab99980b29d2ed4e5dc1aabcf9376ed44083
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6593215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:436069ea3c4195808bee1d78ac421e839d69c0d00c098919e762c1e59eb6678a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-x86_64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Wed, 11 Dec 2024 00:55:58 GMT
ENV _BASH_COMMIT=49c2670226b045746d66765b23af37c1c7ba5597
# Wed, 11 Dec 2024 00:55:58 GMT
ENV _BASH_VERSION=devel-20241126
# Wed, 11 Dec 2024 00:55:58 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Wed, 11 Dec 2024 00:55:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Wed, 11 Dec 2024 00:55:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 11 Dec 2024 00:55:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 Dec 2024 00:55:58 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:38a8310d387e375e0ec6fabe047a9149e8eb214073db9f461fee6251fd936a75`  
		Last Modified: Thu, 05 Dec 2024 21:56:24 GMT  
		Size: 3.6 MB (3644443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d897d7d999cefb3be59997e1e0db3a21d237406ca576fe6aa6a53729090eb2b`  
		Last Modified: Fri, 13 Dec 2024 01:30:27 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff1de24a4b0759b1fce02c8a27908e57fc20bb34b3827a8070e36e6fcf64f6f2`  
		Last Modified: Fri, 13 Dec 2024 01:30:27 GMT  
		Size: 2.9 MB (2947982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e471160c1c114a3dc72963f2b224a9519b2e619d66333472a0286e54cc76247`  
		Last Modified: Fri, 13 Dec 2024 01:30:27 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:959a89d5022dca61b8f6061183804a53ac9b6846d20a6be1874be61ff56d9892
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.7 KB (132700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:742bfda9a1777827f0da481415fc607fe6c62773b39ec7fa76dc4f6cf10816f1`

```dockerfile
```

-	Layers:
	-	`sha256:6cf4ede86c40d65aa09d5d129d2bbd98ee3a680b8a8db2d5b139f2b0f758c594`  
		Last Modified: Fri, 13 Dec 2024 01:30:27 GMT  
		Size: 115.0 KB (115047 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a351143d9e311b50ce76dac9b7101be72900732b049d69b8b96b24bdf8faa50`  
		Last Modified: Fri, 13 Dec 2024 01:30:27 GMT  
		Size: 17.7 KB (17653 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; arm variant v6

```console
$ docker pull bash@sha256:ef0a91717f98af43b5733a53ab828255defd0d5fcdbe375a1fb8bf81a1134731
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6253345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91d08102dd5ac44ab76c66526ac9ae22b9a43f528965ce22c656f5f4541f64a2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armhf.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Wed, 11 Dec 2024 00:55:58 GMT
ENV _BASH_COMMIT=49c2670226b045746d66765b23af37c1c7ba5597
# Wed, 11 Dec 2024 00:55:58 GMT
ENV _BASH_VERSION=devel-20241126
# Wed, 11 Dec 2024 00:55:58 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Wed, 11 Dec 2024 00:55:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Wed, 11 Dec 2024 00:55:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 11 Dec 2024 00:55:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 Dec 2024 00:55:58 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:f2148afcbc6cd4497527fc652f65872130774bf9baace0e1e6a85cad9da5f62e`  
		Last Modified: Thu, 05 Dec 2024 22:17:29 GMT  
		Size: 3.4 MB (3367182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dad000104d8d6e4aac117d865936836caa8bf357d618a8bb7acf231795da1a2`  
		Last Modified: Fri, 13 Dec 2024 01:30:55 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c379a383514881e13839044ce9a6ee3421b29bcec1b9699dad48d9b6d9ef65c`  
		Last Modified: Fri, 13 Dec 2024 01:30:56 GMT  
		Size: 2.9 MB (2885370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ba1302ebb7d4814a9e55d0d4ff3f0ae1448f3acad46d2ffca550ddb75ee0641`  
		Last Modified: Fri, 13 Dec 2024 01:30:55 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:672f8086b7107a0c9dbf4e96394b28b72471572838130047573e90e1900c95a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 KB (17514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4be181fea94e33c5d2acbdc0c8398315d75d705c9d2192ff8cb310e01ac87bb`

```dockerfile
```

-	Layers:
	-	`sha256:2a1faf3eba551f3e8b6fcd0afeeb7b8fa7fad6ba64490d68bc540937f6fe1560`  
		Last Modified: Fri, 13 Dec 2024 01:30:55 GMT  
		Size: 17.5 KB (17514 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; arm variant v7

```console
$ docker pull bash@sha256:78d8eecd31da877141888c62c5170391d26d95c9696c39346b87c6e06aefe817
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5937375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1bef69be84ab2974c6b8ad1c665a893916d89dd8be6e7f24bb6dc8f43563772`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armv7.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Wed, 11 Dec 2024 00:55:58 GMT
ENV _BASH_COMMIT=49c2670226b045746d66765b23af37c1c7ba5597
# Wed, 11 Dec 2024 00:55:58 GMT
ENV _BASH_VERSION=devel-20241126
# Wed, 11 Dec 2024 00:55:58 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Wed, 11 Dec 2024 00:55:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Wed, 11 Dec 2024 00:55:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 11 Dec 2024 00:55:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 Dec 2024 00:55:58 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:39ad020c297459aff9281e5c635286218011e335f3460834ae8397a771bfec55`  
		Last Modified: Thu, 05 Dec 2024 22:17:38 GMT  
		Size: 3.1 MB (3100035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:092b47e0e9bd9310a551d1dc6827d9f6b0069c38ba1559b7a818161c42820f4a`  
		Last Modified: Fri, 13 Dec 2024 01:32:24 GMT  
		Size: 458.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cc138421a27df1ffe2f0ef755b312ce1eebdb96cc1fac874477ce578664ba3d`  
		Last Modified: Fri, 13 Dec 2024 01:32:24 GMT  
		Size: 2.8 MB (2836544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:713751ee3a00448089a74167ef3ca6ce18c333e6fb3284ea74af082f4afc8a46`  
		Last Modified: Fri, 13 Dec 2024 01:32:24 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:1ac2d87d96788abdc143c929a41abfc17852fa2c4dde212072141a01610bb8b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.8 KB (132812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad93094b7f1e088feebd6657021671bb22e04a0e9ae6d6c0a8a26632d51cacac`

```dockerfile
```

-	Layers:
	-	`sha256:5e0fd6baf8f407869f3968cfcbf49121c896e17eba24a51df1c0b37679986eb1`  
		Last Modified: Fri, 13 Dec 2024 01:32:24 GMT  
		Size: 115.1 KB (115083 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb96c75f60a6902db8105d869267e55fbb6b722ff71e491feaeb7d2449bcbb78`  
		Last Modified: Fri, 13 Dec 2024 01:32:23 GMT  
		Size: 17.7 KB (17729 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; arm64 variant v8

```console
$ docker pull bash@sha256:b62ca94e2bd1aee9f16287e36464af77ab791beb1e26819386f23f496d09f456
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7026576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f665dcc34ab2d3f4a53ab72cbe19d7b811394ba5d4c9ae9ec63ca8e1b6ea4b31`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-aarch64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Wed, 11 Dec 2024 00:55:58 GMT
ENV _BASH_COMMIT=49c2670226b045746d66765b23af37c1c7ba5597
# Wed, 11 Dec 2024 00:55:58 GMT
ENV _BASH_VERSION=devel-20241126
# Wed, 11 Dec 2024 00:55:58 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Wed, 11 Dec 2024 00:55:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Wed, 11 Dec 2024 00:55:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 11 Dec 2024 00:55:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 Dec 2024 00:55:58 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:cb8611c9fe5154550f45e284cf977cda4e2b2fee3478552eee31d84be3c95003`  
		Last Modified: Thu, 05 Dec 2024 22:17:35 GMT  
		Size: 4.0 MB (3993186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22bf7a7d9a0c61bb76ce352187a74e22a43dc03fc95614ed659a63b2a9f0b716`  
		Last Modified: Fri, 13 Dec 2024 01:32:25 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6264f830a73066c940d49714cf976e69c36932e5f770843d29cdaa42c9747bed`  
		Last Modified: Fri, 13 Dec 2024 01:32:25 GMT  
		Size: 3.0 MB (3032601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f88e8ca1c7794c5966266b92b393faccb4ac10b9d697a9ad491b130b392c968f`  
		Last Modified: Fri, 13 Dec 2024 01:32:25 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:588409c34bdfdd52f062235ca14a0bb07431a2b5baaf370fe2deeff8b1919037
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.9 KB (132860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d98f75706dd804f4adb89ee719dc71648c848957eddee6209cf6af6357b3d098`

```dockerfile
```

-	Layers:
	-	`sha256:0e81600be5c723465fedd673a58fb854586014049107b2d8a9110ff1d3454503`  
		Last Modified: Fri, 13 Dec 2024 01:32:25 GMT  
		Size: 115.1 KB (115103 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9dfaa9b8bca9a56dab18788f653e62d8ceab64f20c77e9e9bc466b4fe3c35ee6`  
		Last Modified: Fri, 13 Dec 2024 01:32:25 GMT  
		Size: 17.8 KB (17757 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; 386

```console
$ docker pull bash@sha256:6e5190311bda0eb797b8b8087e24eb8e7a08f1727a8493697b33c0a2dd03f399
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6340955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e69649f46f55a2557592d5f80150638296182bbe6326f36abc9f99ec16ba5e7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-x86.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Wed, 11 Dec 2024 00:55:58 GMT
ENV _BASH_COMMIT=49c2670226b045746d66765b23af37c1c7ba5597
# Wed, 11 Dec 2024 00:55:58 GMT
ENV _BASH_VERSION=devel-20241126
# Wed, 11 Dec 2024 00:55:58 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Wed, 11 Dec 2024 00:55:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Wed, 11 Dec 2024 00:55:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 11 Dec 2024 00:55:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 Dec 2024 00:55:58 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:8e5e849a30a22d7386238d38bd56dd5564638f4856bee415fad2bc5852c31989`  
		Last Modified: Thu, 05 Dec 2024 22:17:33 GMT  
		Size: 3.5 MB (3466081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cab98a14cf443fb7971f2d6867ba0d2c197e732d2caff45586c6a00d7afa442`  
		Last Modified: Fri, 13 Dec 2024 01:32:26 GMT  
		Size: 458.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b621cbcbba1a6a679ebae287bb4936080fbe47133b4cf64e9cf7e02803177cf`  
		Last Modified: Fri, 13 Dec 2024 01:32:27 GMT  
		Size: 2.9 MB (2874078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c59fae991d0403a279c38c7a5a36d223e0fd75829ccc17d28f3b5ac8352cccd`  
		Last Modified: Fri, 13 Dec 2024 01:32:26 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:15a10fcbe151981173ff18fcd67572a718c04bbffc10fb330671b63b8d6101c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.6 KB (132643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f44e96851e214c5e0b48fbad2baef37516edb644dc5c2dc653bf8b3b75fc54ab`

```dockerfile
```

-	Layers:
	-	`sha256:271f70bb0539e3530aadc8347a6bde1b27ff2525ac51777db866fa06bd1e639a`  
		Last Modified: Fri, 13 Dec 2024 01:32:26 GMT  
		Size: 115.0 KB (115022 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30f2449e66b85c1631026a56583b39903c1700a1834676dda74f4fe7f0e62354`  
		Last Modified: Fri, 13 Dec 2024 01:32:26 GMT  
		Size: 17.6 KB (17621 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; ppc64le

```console
$ docker pull bash@sha256:3ce1e3a5b8aad8ccf29753bc41bc13336f60535d5bab76d42144f6fe4ea49b54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6794459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b0d0f1339aaa5eac2223a836145b683fac11cd0e293b73866086ed85bec0f77`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-ppc64le.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Wed, 11 Dec 2024 00:55:58 GMT
ENV _BASH_COMMIT=49c2670226b045746d66765b23af37c1c7ba5597
# Wed, 11 Dec 2024 00:55:58 GMT
ENV _BASH_VERSION=devel-20241126
# Wed, 11 Dec 2024 00:55:58 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Wed, 11 Dec 2024 00:55:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Wed, 11 Dec 2024 00:55:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 11 Dec 2024 00:55:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 Dec 2024 00:55:58 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:a12ff663c50b78339bd273940ba035e29d8220954846a4c35a5f79080b37a3d3`  
		Last Modified: Thu, 05 Dec 2024 22:18:21 GMT  
		Size: 3.6 MB (3577108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b87b85a573e0641b22c0c1975b4daedc795bfc844d58d95354403cfa86fb1d5`  
		Last Modified: Fri, 13 Dec 2024 01:32:04 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e043d7bdc29aa9f4df77288ab8b654508edafcb30d9a3739e6eb7a6cbf423040`  
		Last Modified: Fri, 13 Dec 2024 01:32:04 GMT  
		Size: 3.2 MB (3216559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c82722218c425e5d8e2d9337ba67af4f81933e68b6031700c5433082abcdaa2`  
		Last Modified: Fri, 13 Dec 2024 01:32:04 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:6b12bee511cfc492b93fe3c2cfbd4b2ebd3a746272512ec696e03215682a5cc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.8 KB (130824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aca3c927ffb36b82c7b627b65807f75f95709a718abe4572b02bfd60f02af0d`

```dockerfile
```

-	Layers:
	-	`sha256:ca847d12af9c6ca804932631e297ab733fd9c0458f07f93aac7eec641cd0fbf5`  
		Last Modified: Fri, 13 Dec 2024 01:32:04 GMT  
		Size: 113.1 KB (113127 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7672ea43407996cf8db0c806d02f37696478c84dde46416f0b5ac33a1fc88ca`  
		Last Modified: Fri, 13 Dec 2024 01:32:04 GMT  
		Size: 17.7 KB (17697 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; riscv64

```console
$ docker pull bash@sha256:916a922006b94f24572edb3aad8b2684e35b4ee5490a8a9a2334aff79c0baa81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6238752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d96fc777ac9f53a8d015d53543f116d47750ee6c7b45e611df8b9bbcf8898d02`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-riscv64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Tue, 03 Dec 2024 05:17:57 GMT
ENV _BASH_COMMIT=49c2670226b045746d66765b23af37c1c7ba5597
# Tue, 03 Dec 2024 05:17:57 GMT
ENV _BASH_VERSION=devel-20241126
# Tue, 03 Dec 2024 05:17:57 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 03 Dec 2024 05:17:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Dec 2024 05:17:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Dec 2024 05:17:57 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:ea37667e50ca807fa8abc1caf0d21091cbbe1d66b2c217158fb3e91c2787afaf`  
		Last Modified: Tue, 12 Nov 2024 00:55:56 GMT  
		Size: 3.4 MB (3371482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:310aac4cafc7c95b52bc14a776561424688f45262b86ce1e6b69ccb111407c70`  
		Last Modified: Tue, 03 Dec 2024 20:35:39 GMT  
		Size: 2.9 MB (2866928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0facf7b5d582f2a20476194d6fe5aac2d3d20688ee3462df94ceba45775707bf`  
		Last Modified: Tue, 03 Dec 2024 20:35:38 GMT  
		Size: 342.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:f36f467571d4b98aa5a20df282be91a56bc1580b71e372eae976bd83ebd05aec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.6 KB (124577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cdf3ba7235f7345c825ae662956f0abf55b769d83931b6b88a9db425f9319b8`

```dockerfile
```

-	Layers:
	-	`sha256:6a3be803f83a9954734b7b6eb2035f1af2fd914b013b8c9dbd045dc4c069acde`  
		Last Modified: Tue, 03 Dec 2024 20:35:38 GMT  
		Size: 108.2 KB (108171 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99d3dbe9383277b2208bf28e42c8888f47b7867588a30046c8ff3aab12f9b795`  
		Last Modified: Tue, 03 Dec 2024 20:35:38 GMT  
		Size: 16.4 KB (16406 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; s390x

```console
$ docker pull bash@sha256:1755de348f163c52a0486727ab0b8c546f4957693a5adc9dc259ae2ff133a1bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6513285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cc82319af8756ef87506c1fa7c9e87ff44115a23f085ed6a09d7030b59fa990`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-s390x.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Wed, 11 Dec 2024 00:55:58 GMT
ENV _BASH_COMMIT=49c2670226b045746d66765b23af37c1c7ba5597
# Wed, 11 Dec 2024 00:55:58 GMT
ENV _BASH_VERSION=devel-20241126
# Wed, 11 Dec 2024 00:55:58 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Wed, 11 Dec 2024 00:55:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Wed, 11 Dec 2024 00:55:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 11 Dec 2024 00:55:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 Dec 2024 00:55:58 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:ff43eb924acdd7a1002f16e7eb02fc41d4f0bae5329c5666d70c223b6e44f6a1`  
		Last Modified: Thu, 05 Dec 2024 22:19:55 GMT  
		Size: 3.5 MB (3469520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7913dad0640ae3de60db04eecf7fac8f80f68bc8b846efa764ba07e8ce672eb9`  
		Last Modified: Fri, 13 Dec 2024 01:31:15 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ff2404eb941fa9e2b08f2bb09e62032dc3f2265093b09febe7404eb8789412e`  
		Last Modified: Fri, 13 Dec 2024 01:31:15 GMT  
		Size: 3.0 MB (3042970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e846a7b7356a77724d223090c1d8d5b65317ea47bcba26530ea8e08c20544d96`  
		Last Modified: Fri, 13 Dec 2024 01:31:14 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:5fe50644c68dc709a292d09fcf8ee53e89aee23d0bb0894690f9a3d214a47e69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.7 KB (130746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cc17810e1d3658aa79c6093f34f9f5cf8952959860146daeed666ba8d769822`

```dockerfile
```

-	Layers:
	-	`sha256:5f5b037ad3b6cd1aedec8c710aa69303375a89e731ea47b811fac29ec61c08b2`  
		Last Modified: Fri, 13 Dec 2024 01:31:15 GMT  
		Size: 113.1 KB (113093 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:865cb18d67c8da43ae53d716ce8c1e7eeda2d6396841e0ddb1d31316755e6b34`  
		Last Modified: Fri, 13 Dec 2024 01:31:15 GMT  
		Size: 17.7 KB (17653 bytes)  
		MIME: application/vnd.in-toto+json
