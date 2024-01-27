## `bash:devel-alpine3.19`

```console
$ docker pull bash@sha256:90011585f2e1fbe0ee0865396d04ffd274190faec60b3975c2e649e20102db4f
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

### `bash:devel-alpine3.19` - linux; amd64

```console
$ docker pull bash@sha256:8311bb33e68415a0ab6936f1c6bfa10ca1aebb0b6b8ecb7ff28793338a83e981
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6266205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c394f552cc1bac6d0717308ff1153bfba79205381a06b2f7435e571f0761b541`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jan 2024 05:18:01 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Tue, 23 Jan 2024 05:18:01 GMT
CMD ["/bin/sh"]
# Tue, 23 Jan 2024 05:18:01 GMT
ENV _BASH_COMMIT=a4f44b7a11af874556529209fae7e8d261d51293
# Tue, 23 Jan 2024 05:18:01 GMT
ENV _BASH_VERSION=devel-20240119
# Tue, 23 Jan 2024 05:18:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 23 Jan 2024 05:18:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 23 Jan 2024 05:18:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Jan 2024 05:18:01 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64a8c4f4b2f8d08f1c6f1e3b6507927db4988432f0fbe62dd65d82654b23480c`  
		Last Modified: Sat, 27 Jan 2024 00:53:31 GMT  
		Size: 2.9 MB (2857145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d15de07990cbadb028ebc69dbf63873f81240f12c7c66e2cc9fa42d501666670`  
		Last Modified: Sat, 27 Jan 2024 00:53:31 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.19` - unknown; unknown

```console
$ docker pull bash@sha256:7ef92c47f5972be6769cef96e1a4dadb6b93def7ee4f351d7f18876981441b0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.0 KB (113954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d47aa39c0a4e1b14e7c141a64d7dc217457246b3d93dacf817f81900de34c23`

```dockerfile
```

-	Layers:
	-	`sha256:45d5413d392e026ea5f971b0e42c68033e3bc3be6df53e5ceede0d5e3541c306`  
		Last Modified: Sat, 27 Jan 2024 00:53:31 GMT  
		Size: 97.7 KB (97738 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42bf44e96cd9885d6cf468e2fcd69dc0e5a5717d71749ddb69893d5346a95cb0`  
		Last Modified: Sat, 27 Jan 2024 00:53:31 GMT  
		Size: 16.2 KB (16216 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.19` - linux; arm variant v6

```console
$ docker pull bash@sha256:994a55c0d52deb0950212e1fc9a78b584f9dcc0b11f0a154992e8d04813666ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5971329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb94a1870bb8d0fb943efc5b0c4b0768e23d0b925a045e510baeb3ee4c716b91`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 08 Dec 2023 01:49:15 GMT
ADD file:d43ed267a41631ce0e5a4ef5aac821a75300a83f85ecb6259f5616852f89e989 in / 
# Fri, 08 Dec 2023 01:49:15 GMT
CMD ["/bin/sh"]
# Tue, 23 Jan 2024 05:18:01 GMT
ENV _BASH_COMMIT=a4f44b7a11af874556529209fae7e8d261d51293
# Tue, 23 Jan 2024 05:18:01 GMT
ENV _BASH_VERSION=devel-20240119
# Tue, 23 Jan 2024 05:18:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 23 Jan 2024 05:18:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 23 Jan 2024 05:18:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Jan 2024 05:18:01 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:0803c38384d9fd0f9afaec8fd13d267547b660dcd46bb92a3d63c5d76e78b04c`  
		Last Modified: Fri, 08 Dec 2023 01:49:33 GMT  
		Size: 3.2 MB (3165143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0422bcfc00f13984c86ab0641a8ad2f9eca707a1fb62dca019e9388546cde479`  
		Last Modified: Wed, 24 Jan 2024 20:56:48 GMT  
		Size: 2.8 MB (2805849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdc819627c2d5a54128d2101447b7dbfcdb39bf855db8659edc0f2e80476bab9`  
		Last Modified: Wed, 24 Jan 2024 20:56:48 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.19` - unknown; unknown

```console
$ docker pull bash@sha256:6b515a86de745db8e841490a61238fe25ff7509f4ec34c984f37a2f8e3dd125c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 KB (15905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6600266ef7c277e9d91d6f815bd69c87c71942fb7c99b089d79ff3115c83000`

```dockerfile
```

-	Layers:
	-	`sha256:30cda76b483b980c19e911b6012721b5bcf9c72820819a9f259cc107cf60a34f`  
		Last Modified: Wed, 24 Jan 2024 20:56:48 GMT  
		Size: 15.9 KB (15905 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.19` - linux; arm variant v7

```console
$ docker pull bash@sha256:7c908475557cef433de90759fa3eb019bd737a2b93d0da0776943774ea8686c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5672184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15be28d8e95f5941a56446eec5fedaf01784615f59a1755518d56d24410dc80c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jan 2024 05:18:01 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Tue, 23 Jan 2024 05:18:01 GMT
CMD ["/bin/sh"]
# Tue, 23 Jan 2024 05:18:01 GMT
ENV _BASH_COMMIT=a4f44b7a11af874556529209fae7e8d261d51293
# Tue, 23 Jan 2024 05:18:01 GMT
ENV _BASH_VERSION=devel-20240119
# Tue, 23 Jan 2024 05:18:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 23 Jan 2024 05:18:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 23 Jan 2024 05:18:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Jan 2024 05:18:01 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28e2e4e9acf84d2fc2fb7befad937ce58df8ce3c8dd486f749e5fcc76a974729`  
		Last Modified: Sat, 27 Jan 2024 10:24:05 GMT  
		Size: 2.8 MB (2752945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27d00e5751da8991ae73626167058cc340f860d6a91e8a400c894c14cb4be2de`  
		Last Modified: Sat, 27 Jan 2024 10:24:04 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.19` - unknown; unknown

```console
$ docker pull bash@sha256:195a6409606950b190dc8d2a4854180b5ff947bf69ce0646a559365152cd6b9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.1 KB (114060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65a6fcf5f18cb015f4115beb887b446cf906e72105598d431d98c254800bfcba`

```dockerfile
```

-	Layers:
	-	`sha256:7f50d0b9194833b5e541bd80ae4c2b4cb24e5b48e1d6ac8fcfcae35cb0ab3395`  
		Last Modified: Sat, 27 Jan 2024 10:24:04 GMT  
		Size: 97.8 KB (97774 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0faf4fe742f490fb8e899a7c405c4f0921d7b227671211552f5e4e7be0f72030`  
		Last Modified: Sat, 27 Jan 2024 10:24:04 GMT  
		Size: 16.3 KB (16286 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull bash@sha256:ac619ec34fefa12b409eeec231e13733745063a34bc4c1560bee5f4d345c055b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6308699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe43917ea10aa3ef113f6e776116860f2c6aac86f05b05de84fd7aff659eef7f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jan 2024 05:18:01 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Tue, 23 Jan 2024 05:18:01 GMT
CMD ["/bin/sh"]
# Tue, 23 Jan 2024 05:18:01 GMT
ENV _BASH_COMMIT=a4f44b7a11af874556529209fae7e8d261d51293
# Tue, 23 Jan 2024 05:18:01 GMT
ENV _BASH_VERSION=devel-20240119
# Tue, 23 Jan 2024 05:18:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 23 Jan 2024 05:18:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 23 Jan 2024 05:18:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Jan 2024 05:18:01 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81235cdf84035236153765fd79d85d7560ee459fbb280a6f51b21f86b40596de`  
		Last Modified: Sat, 27 Jan 2024 17:36:24 GMT  
		Size: 3.0 MB (2960647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76581886dfe556da032ea9edf8e7b4f5d74fd24b9e0d2cd826ca37e92a4226fe`  
		Last Modified: Sat, 27 Jan 2024 17:36:24 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.19` - unknown; unknown

```console
$ docker pull bash@sha256:3ef15b98c099e3ba65822e6214f941023d581bfb9de500d8c53a904e278b2b89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.0 KB (113975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8294e7fbf703d9ed108e24ea8ab7e8ab549f4f8a0947cdf97c7d0470bd5953a`

```dockerfile
```

-	Layers:
	-	`sha256:1495b592eb8a80a24bfe54de9dffd543b79607ec9f767d0a53787251d59e0b79`  
		Last Modified: Sat, 27 Jan 2024 17:36:24 GMT  
		Size: 97.7 KB (97749 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4410db89412fbc0f816c1312aa0691bae5abdcac56b013a3f8932ed6d1dda2a`  
		Last Modified: Sat, 27 Jan 2024 17:36:24 GMT  
		Size: 16.2 KB (16226 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.19` - linux; 386

```console
$ docker pull bash@sha256:90ea8e4ad7522fc88950c42820a9e08e60076a44b484048249b3e6ba74285db8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6049073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ded1ed7a8c0745d8ea7f2216245b0b1fee534752b0b2496379495814fc8ec610`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jan 2024 05:18:01 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Tue, 23 Jan 2024 05:18:01 GMT
CMD ["/bin/sh"]
# Tue, 23 Jan 2024 05:18:01 GMT
ENV _BASH_COMMIT=a4f44b7a11af874556529209fae7e8d261d51293
# Tue, 23 Jan 2024 05:18:01 GMT
ENV _BASH_VERSION=devel-20240119
# Tue, 23 Jan 2024 05:18:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 23 Jan 2024 05:18:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 23 Jan 2024 05:18:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Jan 2024 05:18:01 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:629e2ae0237fc3eb9abee4600e3a154772d77b674fbf145b9426a1b22b1798d5`  
		Last Modified: Sat, 27 Jan 2024 01:54:18 GMT  
		Size: 2.8 MB (2804649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e6e33767ece45c2cd6a0d051532f2b3b3e615253c4f8436dbba4cf2a347fe54`  
		Last Modified: Sat, 27 Jan 2024 01:54:17 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.19` - unknown; unknown

```console
$ docker pull bash@sha256:6987928077240f5bf3522b0b5879c3014a8dc29bb82dc147c33405c08bf847b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.9 KB (113898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fb5779827f60a36c8ff695631825856ef0c5efff2cbf0b4df83129dd4cab418`

```dockerfile
```

-	Layers:
	-	`sha256:ba9a943a854029f967803ce0ba93a7dccaa29b94f9038e46399a7d061e517e39`  
		Last Modified: Sat, 27 Jan 2024 01:54:17 GMT  
		Size: 97.7 KB (97713 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ec7690f764c87809e717c066b83364a308b10b628b9a51ef19b84f71abeaac6`  
		Last Modified: Sat, 27 Jan 2024 01:54:17 GMT  
		Size: 16.2 KB (16185 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.19` - linux; ppc64le

```console
$ docker pull bash@sha256:15420556b2ac7ed96e6220db58f394363825321fd421d231eefc12f6332f4668
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6489113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22d2d2b1204376066f783d83f797df4342073104c45932767abd21089cd38f3a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jan 2024 05:18:01 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Tue, 23 Jan 2024 05:18:01 GMT
CMD ["/bin/sh"]
# Tue, 23 Jan 2024 05:18:01 GMT
ENV _BASH_COMMIT=a4f44b7a11af874556529209fae7e8d261d51293
# Tue, 23 Jan 2024 05:18:01 GMT
ENV _BASH_VERSION=devel-20240119
# Tue, 23 Jan 2024 05:18:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 23 Jan 2024 05:18:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 23 Jan 2024 05:18:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Jan 2024 05:18:01 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7ce05f90a517c67b8bcff99a8a950a1416e4509231f4c52f9bf2764348de210`  
		Last Modified: Sat, 27 Jan 2024 07:22:33 GMT  
		Size: 3.1 MB (3130419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f56e50d7047f2766fae8ff90d3442778b32c665fc364c9a1f93277aa1e2e00a`  
		Last Modified: Sat, 27 Jan 2024 07:22:32 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.19` - unknown; unknown

```console
$ docker pull bash@sha256:58dbecd059a88fa9f645b1bcbe762c81606b47acd6397534f36c2d9ee401b2cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.4 KB (112388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0492de2a33b90b7fc92ca6a21d14cc01ca002df7af449c5ff75c9e3150078af9`

```dockerfile
```

-	Layers:
	-	`sha256:4c8d7d438a0496e0f82184539e8810258226846e840aa1a6594f9966b760edec`  
		Last Modified: Sat, 27 Jan 2024 07:22:32 GMT  
		Size: 96.1 KB (96136 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f5bdbc026b877717d1e564279424ec7ef094e5cedef7d577fbdc0cf914a0b5a`  
		Last Modified: Sat, 27 Jan 2024 07:22:32 GMT  
		Size: 16.3 KB (16252 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.19` - linux; s390x

```console
$ docker pull bash@sha256:dfce2942449bd1bbfe4f633474bd09fc15a33d18f7a51782a2f6875c7bda98ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6200648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae81673edbba862326431ee7d56b69a735702c68618e0565aeb70f1cec47bf3a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jan 2024 05:18:01 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Tue, 23 Jan 2024 05:18:01 GMT
CMD ["/bin/sh"]
# Tue, 23 Jan 2024 05:18:01 GMT
ENV _BASH_COMMIT=a4f44b7a11af874556529209fae7e8d261d51293
# Tue, 23 Jan 2024 05:18:01 GMT
ENV _BASH_VERSION=devel-20240119
# Tue, 23 Jan 2024 05:18:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 23 Jan 2024 05:18:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 23 Jan 2024 05:18:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Jan 2024 05:18:01 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41e3255187f9297a7a52a101090e51f49d5fb2978cbf1bf8b3ed86b21e8e7d22`  
		Last Modified: Sat, 27 Jan 2024 20:15:40 GMT  
		Size: 3.0 MB (2957680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af0735fe926777f71a38161b3a2de9abcbdf5295751105aec56e0bf8345c0848`  
		Last Modified: Sat, 27 Jan 2024 20:15:40 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.19` - unknown; unknown

```console
$ docker pull bash@sha256:82ec815364bfe304641c08ac8d70d2d9c6d0573bd9013f8538c1eb4294eed0c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.3 KB (112318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b09144c8493f36ac9cd716c4f7c1592bcb58657f402cf1a9a0e4d308c4c0a757`

```dockerfile
```

-	Layers:
	-	`sha256:220931802a47b7d10f58abb360fe6834105bbc9ba713b5d27d72aeb4dac1ff46`  
		Last Modified: Sat, 27 Jan 2024 20:15:40 GMT  
		Size: 96.1 KB (96102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75380c8442fa6d35b4c3e7b05b66b4ee40d1869ef242ca9da153b8eca0da252f`  
		Last Modified: Sat, 27 Jan 2024 20:15:41 GMT  
		Size: 16.2 KB (16216 bytes)  
		MIME: application/vnd.in-toto+json
