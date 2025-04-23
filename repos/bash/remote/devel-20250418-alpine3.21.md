## `bash:devel-20250418-alpine3.21`

```console
$ docker pull bash@sha256:81df70c910bf99dd8b61e64996601e10e027a92d81711eaefe5457ae19ddbf47
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

### `bash:devel-20250418-alpine3.21` - linux; amd64

```console
$ docker pull bash@sha256:06a51fc3a6ab374287e62939964dc8dc75afe7472ad8b9a84321610efb1ccb62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6637022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f6c7d3772f4c65b807bebc8872c81c58527551ced0a30afc8bce4ffd8a2c516`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 22 Apr 2025 04:18:03 GMT
ENV _BASH_COMMIT=482872ed8b51408066c3275a18350436f4d0ee41
# Tue, 22 Apr 2025 04:18:03 GMT
ENV _BASH_VERSION=devel-20250418
# Tue, 22 Apr 2025 04:18:03 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 22 Apr 2025 04:18:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 22 Apr 2025 04:18:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Apr 2025 04:18:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Apr 2025 04:18:03 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95eaeb9fb9c57b683c3a86c9026d651954a8d93854dbc2f8c0954a2389f82b00`  
		Last Modified: Tue, 22 Apr 2025 21:49:34 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d56c3f971d9eb41bb5b8ccb6f24f1d95b9babbacef54713df07bd9a9e5a040e6`  
		Last Modified: Tue, 22 Apr 2025 21:49:34 GMT  
		Size: 3.0 MB (2993987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d54cb4b1bfea9c5fa7d9916df2115f09aa9267e2d727b69ac39374ea85c230c`  
		Last Modified: Tue, 22 Apr 2025 21:49:34 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20250418-alpine3.21` - unknown; unknown

```console
$ docker pull bash@sha256:a569f5b977c8dab5424b2796710469a633aaffffb8073f4ce25f36dad1045dd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.6 KB (132625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dc6d4b3bb45df0ed7e196328f587b4636cda5f60b4c73e89bd1ac037e8be3d3`

```dockerfile
```

-	Layers:
	-	`sha256:5cc55554679489abeabc37224dca6ee725589a9993c2b74100ad5855c0e96599`  
		Last Modified: Tue, 22 Apr 2025 21:49:34 GMT  
		Size: 114.9 KB (114928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad6c074e956cf1bb7b95e24bc05bd33ac30d433150b5c1601b1f976f21173c86`  
		Last Modified: Tue, 22 Apr 2025 21:49:34 GMT  
		Size: 17.7 KB (17697 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20250418-alpine3.21` - linux; arm variant v6

```console
$ docker pull bash@sha256:f7fb7db0b0ab346452252ea0fa5a8b1b220766542ef1d99c92e93e5b5dfe0df2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6295380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f760f9daef2716f845776b49048e2ed5ebca8f3f61fa487726914f02e4878b6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 22 Apr 2025 04:18:03 GMT
ENV _BASH_COMMIT=482872ed8b51408066c3275a18350436f4d0ee41
# Tue, 22 Apr 2025 04:18:03 GMT
ENV _BASH_VERSION=devel-20250418
# Tue, 22 Apr 2025 04:18:03 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 22 Apr 2025 04:18:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 22 Apr 2025 04:18:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Apr 2025 04:18:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Apr 2025 04:18:03 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38f71d03b79647836cd876f54899ad58fcddbbb6e8b09ec300fc132bd64af9c6`  
		Last Modified: Fri, 14 Feb 2025 19:17:59 GMT  
		Size: 459.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba5b36927344eddd3933b85cadbac6671bcc04cceaced9d23a4890a64066c875`  
		Last Modified: Tue, 22 Apr 2025 21:49:02 GMT  
		Size: 2.9 MB (2929859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3817733f336d911c7739127fb58788ea964c7852d5ba3dfa86cc47134042e9b`  
		Last Modified: Tue, 22 Apr 2025 21:49:02 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20250418-alpine3.21` - unknown; unknown

```console
$ docker pull bash@sha256:2cb09a711898e328ed8987345600b067ab193360620bd6c78117273def367f23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.6 KB (17558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e2cae86628a4ada6f32c9a8c49861204e1818a73362bf7e054aa887f563f647`

```dockerfile
```

-	Layers:
	-	`sha256:ca634c768f848c705ae0f2bd10c50716f01cd480d48c792c1912785cd4323203`  
		Last Modified: Tue, 22 Apr 2025 21:49:02 GMT  
		Size: 17.6 KB (17558 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20250418-alpine3.21` - linux; arm variant v7

```console
$ docker pull bash@sha256:085def094fefdb3dce83ed96edace987422a66dd0d250df0acf616b186465632
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5979911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a31c9cfda2e6875ee6b721031e7cb3389ad359af956c1ae1d305df8cca12fade`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 22 Apr 2025 04:18:03 GMT
ENV _BASH_COMMIT=482872ed8b51408066c3275a18350436f4d0ee41
# Tue, 22 Apr 2025 04:18:03 GMT
ENV _BASH_VERSION=devel-20250418
# Tue, 22 Apr 2025 04:18:03 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 22 Apr 2025 04:18:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 22 Apr 2025 04:18:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Apr 2025 04:18:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Apr 2025 04:18:03 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77b71f74feee41903055522dcbbe45229fc23ca960d7e80c99f2747b60a0a3b1`  
		Last Modified: Tue, 25 Mar 2025 20:46:21 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f26b098cb06f1b6c4f1b686f771a5f2073937fde06fac848002c83487f2e1e71`  
		Last Modified: Tue, 22 Apr 2025 21:49:16 GMT  
		Size: 2.9 MB (2880994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d77a80b4e18d5d26bd5066102e9efbddc8ebb8c08396e4de148f2621f755b814`  
		Last Modified: Tue, 22 Apr 2025 21:49:16 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20250418-alpine3.21` - unknown; unknown

```console
$ docker pull bash@sha256:290341722b07e4f7a72b8845ea1b84132517a68c64927924c46469a9cfcb3a12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.7 KB (132737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20b3b6c6373339ad7ed41b691648df88112ac1c1400d33404975c6718a569a64`

```dockerfile
```

-	Layers:
	-	`sha256:bc211794d47c30ab2c3f84c8983890eccb25916cddfe4a7d176b00601393b8ad`  
		Last Modified: Tue, 22 Apr 2025 21:49:16 GMT  
		Size: 115.0 KB (114964 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4c23b296ebd186317937f134a0f892fc0427f2e9b4741784f6f3be60457ce8c`  
		Last Modified: Tue, 22 Apr 2025 21:49:16 GMT  
		Size: 17.8 KB (17773 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20250418-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull bash@sha256:604d1cbe2edbf90a4a3861c534397ebda655d050b4247f936427b8918ff17248
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7074461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5e7e455d8b86b0b4e790b84d6202f03e5b3811db0cdd885adc17da1297013a2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 22 Apr 2025 04:18:03 GMT
ENV _BASH_COMMIT=482872ed8b51408066c3275a18350436f4d0ee41
# Tue, 22 Apr 2025 04:18:03 GMT
ENV _BASH_VERSION=devel-20250418
# Tue, 22 Apr 2025 04:18:03 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 22 Apr 2025 04:18:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 22 Apr 2025 04:18:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Apr 2025 04:18:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Apr 2025 04:18:03 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5af32faa015356c0b2cd3b227fa97838bd58739b580d1b55a7c84292ea848464`  
		Last Modified: Tue, 08 Apr 2025 21:41:10 GMT  
		Size: 460.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64849233ee57cc260c86c303c5349f63d3162f5ea465ace175d0def739ffe67f`  
		Last Modified: Tue, 22 Apr 2025 21:48:58 GMT  
		Size: 3.1 MB (3080642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e670c07a0e58c73c358d82047d63b76d5917a2827f5a15d57ffd733920907aa3`  
		Last Modified: Tue, 22 Apr 2025 21:48:58 GMT  
		Size: 330.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20250418-alpine3.21` - unknown; unknown

```console
$ docker pull bash@sha256:5ae7b217a828f47dcd192d58b8cd4789fc9e52818d3e7d568dbff2150a1b16b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.8 KB (132785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b6a9ebf8fd4d3271af55772b8b1ab6477621ddf7d75292af3f4c6ab1924fa32`

```dockerfile
```

-	Layers:
	-	`sha256:3cf1695d4b80baf7cb941e8a5ae188fd152a8129075cd3d97f7b820335141d37`  
		Last Modified: Tue, 22 Apr 2025 21:48:58 GMT  
		Size: 115.0 KB (114984 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b034d81cf705d58130af1f477a25d8b60039af7fe727aaa9e6fbe1770cf9000`  
		Last Modified: Tue, 22 Apr 2025 21:48:58 GMT  
		Size: 17.8 KB (17801 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20250418-alpine3.21` - linux; 386

```console
$ docker pull bash@sha256:374652f207841c8b46ce4ec5f0a184b42aecf237aebc6f8e87c6e723f64b4d80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6385125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:822b5f868fbdb06ff670edc1c625e7ed187af18781576f58b5bd2984a9a36769`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 22 Apr 2025 04:18:03 GMT
ENV _BASH_COMMIT=482872ed8b51408066c3275a18350436f4d0ee41
# Tue, 22 Apr 2025 04:18:03 GMT
ENV _BASH_VERSION=devel-20250418
# Tue, 22 Apr 2025 04:18:03 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 22 Apr 2025 04:18:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 22 Apr 2025 04:18:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Apr 2025 04:18:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Apr 2025 04:18:03 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff97a83e6b2da939812ba7896bfb0138720c56687c97a954463733ef82ff076e`  
		Last Modified: Tue, 22 Apr 2025 21:49:44 GMT  
		Size: 459.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c1bfcf7775e480e913ee2c53d53a8cefc1212016352aea407b241a8b417cea0`  
		Last Modified: Tue, 22 Apr 2025 21:49:45 GMT  
		Size: 2.9 MB (2920713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcc6efa7f6072340162b6ba90626d76c8c9e1aa570fcf54d89305ac5bbf96482`  
		Last Modified: Tue, 22 Apr 2025 21:49:44 GMT  
		Size: 330.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20250418-alpine3.21` - unknown; unknown

```console
$ docker pull bash@sha256:518e912f22bbc1d15c1070b475bde119e4bbf632711d9a4b1c8ced57cc88b1d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.6 KB (132566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:359db505cbaf4f08d4ec9b749f76dc8e3d6851380a17aaf76c97845fc73e78ed`

```dockerfile
```

-	Layers:
	-	`sha256:22c5babbb1b418497240aa63b50ad97da5e3fd8ad6afa56a5ef371d54ac50c8c`  
		Last Modified: Tue, 22 Apr 2025 21:49:44 GMT  
		Size: 114.9 KB (114903 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10029bda0793aca8427dc13e659c3068610e130d842a5ee3579f47ace15a2f80`  
		Last Modified: Tue, 22 Apr 2025 21:49:44 GMT  
		Size: 17.7 KB (17663 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20250418-alpine3.21` - linux; ppc64le

```console
$ docker pull bash@sha256:b8212455fd2552ebb333d7ba7c277c3a198524987da401b85cc36aaaa921df6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6844778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9c6e18c087c6e86def3fa997fff9e43314e043ab8564f43bb7a747ed3865a73`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 22 Apr 2025 04:18:03 GMT
ENV _BASH_COMMIT=482872ed8b51408066c3275a18350436f4d0ee41
# Tue, 22 Apr 2025 04:18:03 GMT
ENV _BASH_VERSION=devel-20250418
# Tue, 22 Apr 2025 04:18:03 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 22 Apr 2025 04:18:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 22 Apr 2025 04:18:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Apr 2025 04:18:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Apr 2025 04:18:03 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e36049ca8d20b61234d6959e293fa53a0267e9cfd98d7f17f6c24ae271b006d4`  
		Last Modified: Tue, 08 Apr 2025 19:29:49 GMT  
		Size: 458.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03b64c2e2bbce143796cc57f7e433fd0ae0a57ffa90168b8fc472b8ded597336`  
		Last Modified: Tue, 22 Apr 2025 21:56:24 GMT  
		Size: 3.3 MB (3269640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b1552416b8bd4d67455d5c70b1531242352e041925e8cc36886b07f1fb52e0`  
		Last Modified: Tue, 22 Apr 2025 21:56:24 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20250418-alpine3.21` - unknown; unknown

```console
$ docker pull bash@sha256:bc71168801ea099e2b0c9e468caadbafba05ca353783ed471330db3f8e4a2f15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.8 KB (130752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf6c03653aed75063a7b2f56e9d70a787e4aa42d217f276f31c3f19ac7896a7d`

```dockerfile
```

-	Layers:
	-	`sha256:eea81c6eefaf3d6b18c9f9a006dd5e69fb896887211c578fea3a52a5c0d86674`  
		Last Modified: Tue, 22 Apr 2025 21:56:24 GMT  
		Size: 113.0 KB (113011 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6537c8e07d6b6a936198eea40433aebd27abcb6e266611046945b4670dcc768d`  
		Last Modified: Tue, 22 Apr 2025 21:56:24 GMT  
		Size: 17.7 KB (17741 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20250418-alpine3.21` - linux; riscv64

```console
$ docker pull bash@sha256:b6a225055c943a28948b9c4e06e28040243a0aa1ea0e9e00f4ab2d3ac3c52bd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6295646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7800ab808ffb176ae9c13b46854f282db16e7c0edd5d351a8137cbb9ed462145`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 22 Apr 2025 04:18:03 GMT
ENV _BASH_COMMIT=482872ed8b51408066c3275a18350436f4d0ee41
# Tue, 22 Apr 2025 04:18:03 GMT
ENV _BASH_VERSION=devel-20250418
# Tue, 22 Apr 2025 04:18:03 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 22 Apr 2025 04:18:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 22 Apr 2025 04:18:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Apr 2025 04:18:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Apr 2025 04:18:03 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:7df33f7ad8beb367ac09bdd1b2f220db3ee2bbdda14a6310d1340e5628b5ba88`  
		Last Modified: Fri, 14 Feb 2025 18:56:36 GMT  
		Size: 3.4 MB (3351439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03589e78b235e506dafea1c4a2d73b5326f0580bc335cad463e8b5863a7e527d`  
		Last Modified: Fri, 14 Feb 2025 19:22:45 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d626e89e421ad4ca46262787a84a2d96697aa16e67c4dfcb5e7b6be6f1d18de8`  
		Last Modified: Tue, 22 Apr 2025 21:57:42 GMT  
		Size: 2.9 MB (2943414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:947d6656ffc94fe7d7b94ed366230f628af90e00b317e19c066d82064ccce19e`  
		Last Modified: Tue, 22 Apr 2025 21:57:41 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20250418-alpine3.21` - unknown; unknown

```console
$ docker pull bash@sha256:52ea489159c9581b48b8d3f1347ca160ee0ff7374501f2777a633209f299ac37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.7 KB (130748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a27c3c02784617a346187d3825f7fa1d71785a69e72e7e0b805aa729595248f`

```dockerfile
```

-	Layers:
	-	`sha256:d0143a54d160a6f4bac1d635d9a995e1e5c79fd0e9bc5b1318056bb20e523ee1`  
		Last Modified: Tue, 22 Apr 2025 21:57:41 GMT  
		Size: 113.0 KB (113007 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc8676abe91122b3744666e925cd7bd7d91d4a196d4d429b58e346374705cc7d`  
		Last Modified: Tue, 22 Apr 2025 21:57:41 GMT  
		Size: 17.7 KB (17741 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20250418-alpine3.21` - linux; s390x

```console
$ docker pull bash@sha256:88f50fde67e7b33b83f9eabfe52849b0f63386d4e504a779810999cdb10f1a69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6558730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3204e07516a3101222ab0bcf24d4704b5f67a4247a304e92c89a4b33da798024`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 22 Apr 2025 04:18:03 GMT
ENV _BASH_COMMIT=482872ed8b51408066c3275a18350436f4d0ee41
# Tue, 22 Apr 2025 04:18:03 GMT
ENV _BASH_VERSION=devel-20250418
# Tue, 22 Apr 2025 04:18:03 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 22 Apr 2025 04:18:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 22 Apr 2025 04:18:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Apr 2025 04:18:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Apr 2025 04:18:03 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e20ebcc118aee9f69754c83c44c7e1446bc00d1974545eb0c3248776bc32cd0d`  
		Last Modified: Tue, 15 Apr 2025 22:40:50 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2466f8f78772347375e0daefde3b45eb0d7f66eadf725b553b3717c66d667042`  
		Last Modified: Tue, 22 Apr 2025 21:50:04 GMT  
		Size: 3.1 MB (3090372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ea9c4e056a85444976e1fffa012cd191509afd09d8fcf6964d90ab2ad3596b3`  
		Last Modified: Tue, 22 Apr 2025 21:50:04 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20250418-alpine3.21` - unknown; unknown

```console
$ docker pull bash@sha256:c3ad571fb635d3e42da68ed79a4c07559dd91fbbeb9b065abd62a58dd2925fee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.7 KB (130674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd8205e99b137cf24bb16730853bc65fb3752d29064ddac0e636da7cd5e04f9f`

```dockerfile
```

-	Layers:
	-	`sha256:f6b4dd930da6f89a7392d1d10f76eb5cb742449f24510855ac3154ae6ee06555`  
		Last Modified: Tue, 22 Apr 2025 21:50:04 GMT  
		Size: 113.0 KB (112977 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1cf4b845514fd660b4d0ca5f6ac9b19aab9c246df7bd88c104504ebb3b8f2b92`  
		Last Modified: Tue, 22 Apr 2025 21:50:04 GMT  
		Size: 17.7 KB (17697 bytes)  
		MIME: application/vnd.in-toto+json
