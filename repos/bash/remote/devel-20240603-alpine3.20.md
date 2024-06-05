## `bash:devel-20240603-alpine3.20`

```console
$ docker pull bash@sha256:c19ab953ce38e165da1539f87e36d5f01137450aff53d2a306e5846b7fdfb3cc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown

### `bash:devel-20240603-alpine3.20` - linux; amd64

```console
$ docker pull bash@sha256:54ef5b69b7058887d0f25c3df1d31274050c900016d383e01adef28dbdce5365
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6516833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64fd423e2c510fdaec4d6c896cb32aa9cba0e0c28ca992c059221bf0e2e8dad1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
CMD ["/bin/sh"]
# Tue, 04 Jun 2024 04:18:28 GMT
ENV _BASH_COMMIT=f65ed506d4dfecbc2667c34a9cb18175ada95cea
# Tue, 04 Jun 2024 04:18:28 GMT
ENV _BASH_VERSION=devel-20240603
# Tue, 04 Jun 2024 04:18:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 04 Jun 2024 04:18:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Jun 2024 04:18:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Jun 2024 04:18:28 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8c3af197ef105a46b45a41caeb20c6fc96474767776ce9abc9805c3ae8a404e`  
		Last Modified: Tue, 04 Jun 2024 22:54:23 GMT  
		Size: 2.9 MB (2894403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:542cac2d6a7a0affb50f9592273de9e4af7cc0fc2c677ff9752112b7910dbd40`  
		Last Modified: Tue, 04 Jun 2024 22:54:22 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20240603-alpine3.20` - unknown; unknown

```console
$ docker pull bash@sha256:964bd6c3bee4c9ce44e9b83476b5943f4008e5898771aa31cab4b56eb8accd03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.9 KB (122864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd03324c2ffe3a1fdf598bf297b303efcc6a2bbccdc28cccfb5dc4c0efe39689`

```dockerfile
```

-	Layers:
	-	`sha256:2bf25f349d6a70d4c3a9e8feca088322ff07c03de09602bac51d729faacfbc17`  
		Last Modified: Tue, 04 Jun 2024 22:54:22 GMT  
		Size: 106.5 KB (106508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23bb2a4e5f6b3ebb2951f0d4df435d85a65b106553394f14ade17606e7691838`  
		Last Modified: Tue, 04 Jun 2024 22:54:22 GMT  
		Size: 16.4 KB (16356 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20240603-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull bash@sha256:72a888ed289d33c0a6ded6f74cbfbf505ca14f84fc28dda7c6387d3ec6464efb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7083167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b73f280b729649a6b96c1889fd9f3325b9da9d6938e4f1924a47a9b1c8189f2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 May 2024 18:17:27 GMT
ADD file:ceadd994c6d8900884c4a44aa76cf187336921e29afeaa017c4a3d1fc066a6a3 in / 
# Wed, 22 May 2024 18:17:28 GMT
CMD ["/bin/sh"]
# Tue, 04 Jun 2024 04:18:28 GMT
ENV _BASH_COMMIT=f65ed506d4dfecbc2667c34a9cb18175ada95cea
# Tue, 04 Jun 2024 04:18:28 GMT
ENV _BASH_VERSION=devel-20240603
# Tue, 04 Jun 2024 04:18:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 04 Jun 2024 04:18:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Jun 2024 04:18:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Jun 2024 04:18:28 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:94747bd812346354fd5042870b6e44e5406880a4e6b5736a9cf9c753110df11b`  
		Last Modified: Wed, 22 May 2024 18:17:47 GMT  
		Size: 4.1 MB (4086776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7635fbe920a4f24aeed2f274fa22ff8140b390ec5466a100ed9d37c6d46f6f06`  
		Last Modified: Tue, 04 Jun 2024 23:33:56 GMT  
		Size: 3.0 MB (2996049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:149d62c065a1fcdd336f4aff26be40dd548b51bb47c213dda942213f8ba1aadc`  
		Last Modified: Tue, 04 Jun 2024 23:33:55 GMT  
		Size: 342.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20240603-alpine3.20` - unknown; unknown

```console
$ docker pull bash@sha256:93f8b8966a6d4702440052b52a25d016a704fabc488bd0644658888eb6152e82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.2 KB (123222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:909255c07233b49d2a970ae90d22b2410f53166f7f6d6628643e3f70408eb5c7`

```dockerfile
```

-	Layers:
	-	`sha256:18fc0962939a3f87e3c77183148b1050d4eb8977a2748fee2ec40ce61c71da03`  
		Last Modified: Tue, 04 Jun 2024 23:33:55 GMT  
		Size: 106.6 KB (106564 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:111d2c05a734873777805878682ef15e9f20715ccd00570c8ba2a74c6ab131e7`  
		Last Modified: Tue, 04 Jun 2024 23:33:55 GMT  
		Size: 16.7 KB (16658 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20240603-alpine3.20` - linux; 386

```console
$ docker pull bash@sha256:b69c24eac1ad9b5cdfcaa86f5bbd8c4cd35b464cbf65c520d9ea1073fa9ec1e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6306183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfd7d3d62435463b34af636fcb94a566a7eaaf70ce92af7454e50b841cda1729`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 May 2024 18:05:50 GMT
ADD file:6a4a5e48a600b064b83b954a55f1ddd3352780d69a6fb0ad816258011f5a3e47 in / 
# Wed, 22 May 2024 18:05:51 GMT
CMD ["/bin/sh"]
# Tue, 04 Jun 2024 04:18:28 GMT
ENV _BASH_COMMIT=f65ed506d4dfecbc2667c34a9cb18175ada95cea
# Tue, 04 Jun 2024 04:18:28 GMT
ENV _BASH_VERSION=devel-20240603
# Tue, 04 Jun 2024 04:18:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 04 Jun 2024 04:18:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Jun 2024 04:18:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Jun 2024 04:18:28 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:271acb68d2933b32dac564003959c5aea6d5d436c2779e253600ab35d7745465`  
		Last Modified: Wed, 22 May 2024 18:06:11 GMT  
		Size: 3.5 MB (3467181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:803d5fa214e59ba2a1ab5ab8b719d587074d6e949cb44aa5bab1f88dbc1754b4`  
		Last Modified: Tue, 04 Jun 2024 22:54:23 GMT  
		Size: 2.8 MB (2838666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e216f715d2b5d779eca5bb4c1e87ffd61309a839457a2568c9633c98263421e6`  
		Last Modified: Tue, 04 Jun 2024 22:54:23 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20240603-alpine3.20` - unknown; unknown

```console
$ docker pull bash@sha256:aadf8712edde1c1e92dc6b3f1e3dcbe8bba27622d20f64aecf2e34d7b7f6afbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.8 KB (122812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64f223c31ca8fab9db267d359a435bb0ccdaa5685bf8bfbb0c20d295356a30d6`

```dockerfile
```

-	Layers:
	-	`sha256:269287515cfd0d1e9355207fe95e3e00218be3a990071c6478958ede0a46137f`  
		Last Modified: Tue, 04 Jun 2024 22:54:24 GMT  
		Size: 106.5 KB (106483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81f20bce05b176d0580c284e8f181d4a96aaefaa1de66425afd350997d9fa576`  
		Last Modified: Tue, 04 Jun 2024 22:54:23 GMT  
		Size: 16.3 KB (16329 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20240603-alpine3.20` - linux; ppc64le

```console
$ docker pull bash@sha256:08737aeb89256130f7b92ad2ee8a80882a389b4140f740a88e03fb809a88f0ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6737130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcce88978c34578fa767411f99a477fd32f1d917df36535ae0f656f7a64ade18`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 May 2024 18:07:11 GMT
ADD file:023435caa2a1f2c4ffa6455de5b3dc6e19c43a35708671eeef36e0166c54eecd in / 
# Wed, 22 May 2024 18:07:12 GMT
CMD ["/bin/sh"]
# Tue, 04 Jun 2024 04:18:28 GMT
ENV _BASH_COMMIT=f65ed506d4dfecbc2667c34a9cb18175ada95cea
# Tue, 04 Jun 2024 04:18:28 GMT
ENV _BASH_VERSION=devel-20240603
# Tue, 04 Jun 2024 04:18:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 04 Jun 2024 04:18:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Jun 2024 04:18:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Jun 2024 04:18:28 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:fc0288db113f6df5dbde63eac62c59d28df80cd0602675f606e688d365d8bc6a`  
		Last Modified: Wed, 22 May 2024 18:07:33 GMT  
		Size: 3.6 MB (3569846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e948848503961f823abb05596fb12ebdd2e28c304d827698f1d391774e3e67c9`  
		Last Modified: Tue, 04 Jun 2024 23:08:07 GMT  
		Size: 3.2 MB (3166944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3266cb03801e7974445fc764ae8ef68d44692d9ac9704a6550ed8c66d943304`  
		Last Modified: Tue, 04 Jun 2024 23:08:07 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20240603-alpine3.20` - unknown; unknown

```console
$ docker pull bash@sha256:21e7f6a7f1a46a89a3edf4e9b8adba710f6d35e3c57b26c394db8735135caaa6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.0 KB (120984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f05e98907118e6a26709a3c9099fe79a1f41550ee322a6a50235a203c54836c`

```dockerfile
```

-	Layers:
	-	`sha256:adc27bfcca86cf6c38916b9fb0887e87fabec94a97d3fed9e6c3df5572c41352`  
		Last Modified: Tue, 04 Jun 2024 23:08:07 GMT  
		Size: 104.6 KB (104588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c681d24d4a4d982be03e617762ffbf5053617356909fb632aa2622adf995ef0f`  
		Last Modified: Tue, 04 Jun 2024 23:08:07 GMT  
		Size: 16.4 KB (16396 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20240603-alpine3.20` - linux; riscv64

```console
$ docker pull bash@sha256:4e377cbf64bda7879e53f4f1f2ab8e860eab4c1d7d9e15a1f9eb2c8e4b7e7a6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6215323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e816486a58d3a0bc63b87fd4c218933667459c02627faa494d7883f13e22d632`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 May 2024 17:57:29 GMT
ADD file:adedc612a3543e3a541be8e74c994fc3782e0f4a762ca77a1e29e6abfc81d7d8 in / 
# Wed, 22 May 2024 17:57:29 GMT
CMD ["/bin/sh"]
# Tue, 04 Jun 2024 04:18:28 GMT
ENV _BASH_COMMIT=f65ed506d4dfecbc2667c34a9cb18175ada95cea
# Tue, 04 Jun 2024 04:18:28 GMT
ENV _BASH_VERSION=devel-20240603
# Tue, 04 Jun 2024 04:18:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 04 Jun 2024 04:18:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Jun 2024 04:18:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Jun 2024 04:18:28 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:f280e85d15153a8f10f3fa47dd9d639e7a8fc6c1c8795d7123a32a0c36f16f55`  
		Last Modified: Wed, 22 May 2024 17:57:48 GMT  
		Size: 3.4 MB (3368560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b691a6e83a410385405ddbdaf8c53f82700ea3a272e8c911849d2d8c0eb85ed`  
		Last Modified: Tue, 04 Jun 2024 23:00:13 GMT  
		Size: 2.8 MB (2846420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4331bf43f398c39106a38b6374abf3ae3b3a0192c5c83967c1133d782e83ebfe`  
		Last Modified: Tue, 04 Jun 2024 23:00:12 GMT  
		Size: 343.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20240603-alpine3.20` - unknown; unknown

```console
$ docker pull bash@sha256:7c2aaf052ed90f37bf11cf814875b297404b54000bcbad219bccb470df2c3d6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.0 KB (120980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ae1073816fbedca39bd4c9dd9183d686494ed01b8c73f508c530b04b989303e`

```dockerfile
```

-	Layers:
	-	`sha256:4ef7779197f0b08d0d69056431eedea6a5750a325ffb983e716131af2b378ec5`  
		Last Modified: Tue, 04 Jun 2024 23:00:12 GMT  
		Size: 104.6 KB (104584 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:710d30e5e426b8e91987eb5781d7bdde774c92fbeb29e22b2e51585ac58ca0a1`  
		Last Modified: Tue, 04 Jun 2024 23:00:12 GMT  
		Size: 16.4 KB (16396 bytes)  
		MIME: application/vnd.in-toto+json
