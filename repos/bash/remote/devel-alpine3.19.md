## `bash:devel-alpine3.19`

```console
$ docker pull bash@sha256:2a099acaba0218682fdfc69472778f3ece9ebee17be18ba787847ca3c4024f04
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
$ docker pull bash@sha256:803346c94e8c7d5badecd98a56e84a934e2c11ac0cad2711912b112632b7cb5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6265943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5949b60deb66ca4257c605340616665d99ec2a1aad1fc2477d15b5d9ac7c3172`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 08 Dec 2023 01:20:49 GMT
ADD file:1f4eb46669b5b6275af19eb7471a6899a61c276aa7d925b8ae99310b14b75b92 in / 
# Fri, 08 Dec 2023 01:20:49 GMT
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
	-	`sha256:661ff4d9561e3fd050929ee5097067c34bafc523ee60f5294a37fd08056a73ca`  
		Last Modified: Fri, 08 Dec 2023 01:21:10 GMT  
		Size: 3.4 MB (3408480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8e5e313dcd7eda03a85730540f478c513759d945248c7ee370be90d4fc19d49`  
		Last Modified: Wed, 24 Jan 2024 20:50:23 GMT  
		Size: 2.9 MB (2857125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9a314a295f95f2e926753f7954e03f47962da0ffae256da1c9be26f2553f38c`  
		Last Modified: Wed, 24 Jan 2024 20:50:23 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.19` - unknown; unknown

```console
$ docker pull bash@sha256:95e6a32daa48fbbfca7dc7964460e14e2efad0979393db6c952c71466262c219
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.9 KB (113948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdc5fbb0a17b147a6a9e651b2712ab03b5ccf0d35f3b04d8598d4468ee58e3dd`

```dockerfile
```

-	Layers:
	-	`sha256:832082dcf6e9596e264fe6290eb57b1a9435ac9781b2915673375122953e7d4e`  
		Last Modified: Wed, 24 Jan 2024 20:50:23 GMT  
		Size: 97.7 KB (97732 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc6397e81e8cc0a0a90b6dfc50ed36089059e73f8b554a311667ab6680459a4b`  
		Last Modified: Wed, 24 Jan 2024 20:50:23 GMT  
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
$ docker pull bash@sha256:8feaeae3e581e99d8d7d03117845ab88e6dfb5344606e762aa35247ba39f3cf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5671990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d3814997d74fda48b72e3c25debe04e2e1205a007216b1497b6e044931d7bfb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 08 Dec 2023 01:57:20 GMT
ADD file:13b9291053208eec61cd7c97bac2fa154380ad8d10182567763eea3e10c5882f in / 
# Fri, 08 Dec 2023 01:57:20 GMT
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
	-	`sha256:1086c24c41097f090ce847d192c11307e1715eeb563a2cf4f410b2a199ae1942`  
		Last Modified: Fri, 08 Dec 2023 01:57:36 GMT  
		Size: 2.9 MB (2918701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e36a21ab9c3a658140da614b8e19745781117898e636ff79b16659dd1ec1f17`  
		Last Modified: Wed, 24 Jan 2024 21:10:24 GMT  
		Size: 2.8 MB (2752954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed2c6fde30d1c953fbb6727c9bd1c914e19f7d55b025657ba0ad5ef517f64380`  
		Last Modified: Wed, 24 Jan 2024 21:10:24 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.19` - unknown; unknown

```console
$ docker pull bash@sha256:60756b64d244f4f142b0278f51f133d9429ce7d34ab3837ad9980399ea63588f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.9 KB (113888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a6bd58b98b924c1fb903048d9e5e935144a30887e31e63b822d4cddc740fdd0`

```dockerfile
```

-	Layers:
	-	`sha256:d97cd963d83b88c94c50d88016a9954212adcdcd8029c252ea935ff279b55481`  
		Last Modified: Wed, 24 Jan 2024 21:10:25 GMT  
		Size: 97.8 KB (97768 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a87878ef85afdd4e1a389470ce397b4a8cda61ed1ced5e6e8128a06316f364e9`  
		Last Modified: Wed, 24 Jan 2024 21:10:24 GMT  
		Size: 16.1 KB (16120 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull bash@sha256:15eca162c2013f5672734e3eda8e4071bcbe6934980e661a71b63a6ddaaaa5ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6308738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3366b97211ffad088d9fa9a15cc47bbfb9585ea6950de5ba0c59c0f60af5601a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 08 Dec 2023 01:39:30 GMT
ADD file:8182c73f869a899cf624a59c400acb8226776d15e4d3a0d240a94e65340540d0 in / 
# Fri, 08 Dec 2023 01:39:30 GMT
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
	-	`sha256:c303524923177661067f7eb378c3dd5277088c2676ebd1cd78e68397bb80fdbf`  
		Last Modified: Fri, 08 Dec 2023 01:39:48 GMT  
		Size: 3.3 MB (3347794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5010f3ed4b33eb233329dbfbdd4a07c8cc79cf0081f7df733e69d9d043fe30a9`  
		Last Modified: Wed, 24 Jan 2024 22:05:37 GMT  
		Size: 3.0 MB (2960614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48cfbc0f484a236824f955fb87f56598d55cfe7f575ffa13766dcec11249372b`  
		Last Modified: Wed, 24 Jan 2024 22:05:36 GMT  
		Size: 330.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.19` - unknown; unknown

```console
$ docker pull bash@sha256:349de10f99f72fdc43caefe7079c0666fd78b649e4a347f7f199e44e9cb489cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.8 KB (113803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fffc89f23e755e2dfa07d7324d6fc024d4a467d53e3fd3c2d93f6972ec19bcf`

```dockerfile
```

-	Layers:
	-	`sha256:260f6a7fd7ace3ce2d4e588120b631b391895275c51fec801ac9b683ead63112`  
		Last Modified: Wed, 24 Jan 2024 22:05:36 GMT  
		Size: 97.7 KB (97743 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e44d8e039a9765c879188984ef302073a112d5a792a972b213aea9eaf146840`  
		Last Modified: Wed, 24 Jan 2024 22:05:36 GMT  
		Size: 16.1 KB (16060 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.19` - linux; 386

```console
$ docker pull bash@sha256:6b9b1befeb60d6ea7f1987577ae396793ca1b3da98521e29278c4f9aac48f121
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6049070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fa81cc7c125a67bb7311b02d90f0590991a36e6cf746f18dc3c59ab0e0df5d6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 08 Dec 2023 01:38:25 GMT
ADD file:bd52540f209ba362654d795d7893669c819d35011a16f9f319301727a33b3bd9 in / 
# Fri, 08 Dec 2023 01:38:25 GMT
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
	-	`sha256:9acd8b4c9d4385585f74dabb4bc6b3351888710ae37ec5dbd9ea950281b8f9bb`  
		Last Modified: Fri, 08 Dec 2023 01:38:43 GMT  
		Size: 3.2 MB (3244115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d4b7fb6dbc104c0af2dabb1d9635843612091d701ea05c0a045f2d978310078`  
		Last Modified: Wed, 24 Jan 2024 20:50:22 GMT  
		Size: 2.8 MB (2804622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91a3368bf1e2c72bb5c2e339e229a816ec20a58e97c33405e3fea5a9420f69ef`  
		Last Modified: Wed, 24 Jan 2024 20:50:22 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.19` - unknown; unknown

```console
$ docker pull bash@sha256:5cc3905316c044dc288ff55ab11e9e8f200bbb24598485ada9273dac21697f62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.9 KB (113894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5eae7c79aed8519ca9e6200f0c691a0bf737b5f33a996aee7497141ed7b541b`

```dockerfile
```

-	Layers:
	-	`sha256:a2b473636420e7e59a37c64eced4a28feba5205302aba8bd46e8e4ab23d46f02`  
		Last Modified: Wed, 24 Jan 2024 20:50:22 GMT  
		Size: 97.7 KB (97707 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6e5976dbdc763694b995b861961a14f863fe53d50d84d6ee34186b91ac83eb8`  
		Last Modified: Wed, 24 Jan 2024 20:50:22 GMT  
		Size: 16.2 KB (16187 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.19` - linux; ppc64le

```console
$ docker pull bash@sha256:bb81a7a3862fc0bddf9a4c4944d0c24cd0bde792c7f4a147797fcc81fd85fa48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6488992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67c4415574d9140a1920cb5974d09528b7faaf70033da9d53ea4404b4585721e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 08 Dec 2023 01:22:51 GMT
ADD file:052421189f8d269382daaaa8beb63c687e4d8ca908c421abdce53bcc627a40b4 in / 
# Fri, 08 Dec 2023 01:22:51 GMT
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
	-	`sha256:243ac51c334a47917a84be93e972ee6378987e9b3b917a5a8df29025e161c1f3`  
		Last Modified: Fri, 08 Dec 2023 01:23:14 GMT  
		Size: 3.4 MB (3358233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b068dc7fc2ccee255f2b3a888c0cce07b0a83d710ce7ce7bd7adc469b89d7580`  
		Last Modified: Wed, 24 Jan 2024 21:26:09 GMT  
		Size: 3.1 MB (3130421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea955084db8e662ae5bdd76791a0c51909300cf27b0437216dd416b33e5e3b3b`  
		Last Modified: Wed, 24 Jan 2024 21:26:08 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.19` - unknown; unknown

```console
$ docker pull bash@sha256:5097c7ebf7cbc4c405b871b2f7201de8e0e5308d95e2d4270c949e4adf299e16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.2 KB (112218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2aab4f4f67fa01a6c85c9db64c57f05c9065ffe39f3a7543028597124327340`

```dockerfile
```

-	Layers:
	-	`sha256:a0c00799094f35c613f76382194a518988018f3374dc66b94e18a627a41fdf44`  
		Last Modified: Wed, 24 Jan 2024 21:26:08 GMT  
		Size: 96.1 KB (96130 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7fa6f97563407e311859da5521ecd310b5ee04d5cd6912d08cc6ff3ba751f177`  
		Last Modified: Wed, 24 Jan 2024 21:26:08 GMT  
		Size: 16.1 KB (16088 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.19` - linux; s390x

```console
$ docker pull bash@sha256:61f88e30ae1bee2572bb3c89b3882b06615cd70ad44e4f77551ae10c28f0f37d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6200145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9806744f06b474bebe8cf50d493531ff760d3b1637898a9900bdbd7cff5f954c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 08 Dec 2023 01:41:50 GMT
ADD file:47e0982fc3ae485c06d46f3c0022afd39ed7ec95fe755c2391e6b0cfcae65dfc in / 
# Fri, 08 Dec 2023 01:41:51 GMT
CMD ["/bin/sh"]
# Tue, 16 Jan 2024 05:18:09 GMT
ENV _BASH_COMMIT=f2fdb5e31317bf5199814ae9866debe1c20cd3a4
# Tue, 16 Jan 2024 05:18:09 GMT
ENV _BASH_VERSION=devel-20240114
# Tue, 16 Jan 2024 05:18:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 16 Jan 2024 05:18:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jan 2024 05:18:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jan 2024 05:18:09 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:0fca3ee44ced87b7184bc23390283fdf10cfae0e844a25b785dd11c463815227`  
		Last Modified: Fri, 08 Dec 2023 01:42:30 GMT  
		Size: 3.2 MB (3242332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e364b15b899ebccd5a4e4c6588cea851d532fc3a9106fae7fa94281397f97cd`  
		Last Modified: Wed, 17 Jan 2024 03:06:29 GMT  
		Size: 3.0 MB (2957477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:813e881bcdde0699bf5c0205fc3afe69b3d73de3e558d02c8160a6633cd2a369`  
		Last Modified: Wed, 17 Jan 2024 03:06:29 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.19` - unknown; unknown

```console
$ docker pull bash@sha256:b527ed7c8a5fe3745a232367d6d18e8f86fa3b357f66b9f90b8ada24e5b8b724
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.2 KB (112194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b8cef751df290f1379f312d095dca9683a5d5b8bfe22d051b19e915c4226ad7`

```dockerfile
```

-	Layers:
	-	`sha256:792c5922f7c945fa8395f9b25d0f4e76d25420cc53462503e673a137c92880ca`  
		Last Modified: Wed, 17 Jan 2024 03:06:29 GMT  
		Size: 96.1 KB (96096 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f4242fe4db6ac8bdef44ce1d1104af265453e0e1e02387d9ac965333e6153b2`  
		Last Modified: Wed, 17 Jan 2024 03:06:29 GMT  
		Size: 16.1 KB (16098 bytes)  
		MIME: application/vnd.in-toto+json
