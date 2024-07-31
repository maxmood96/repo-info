## `bash:devel-alpine3.20`

```console
$ docker pull bash@sha256:2374c261ce12b18b2328e1780f02b2dc7818b3d514a830d66c9cbdc05cc0dfd9
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

### `bash:devel-alpine3.20` - linux; amd64

```console
$ docker pull bash@sha256:1125fead3564df008b3457af470967583405319897240bf7f8db846d0f038c08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6524614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e76f09db2a0a6d89901aa6b17b18fc9a3c1a70dff761b183a0e79e4a75e751fc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:43 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Mon, 22 Jul 2024 22:26:43 GMT
CMD ["/bin/sh"]
# Tue, 30 Jul 2024 02:00:38 GMT
ENV _BASH_COMMIT=d5ef283cbdd08217efdc55974a6a8a2c52a7562f
# Tue, 30 Jul 2024 02:00:38 GMT
ENV _BASH_VERSION=devel-20240726
# Tue, 30 Jul 2024 02:00:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 30 Jul 2024 02:00:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 Jul 2024 02:00:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Jul 2024 02:00:38 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45c8b317578096d19536d9db9f5e26a29fc80a5008db7436ff943b4effb1b9b2`  
		Last Modified: Tue, 30 Jul 2024 23:55:58 GMT  
		Size: 2.9 MB (2901388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b27a20db0e9a85e3ca5a17b52521dc3699fd7fad40c2fdf670aefca80c8bb3e`  
		Last Modified: Tue, 30 Jul 2024 23:55:58 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.20` - unknown; unknown

```console
$ docker pull bash@sha256:761ac97436d5657a8e60891ce12a6ebff57c04a07d0bd0f32c71320393922c0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.0 KB (125970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f017672d8e7cfd73af8105c96c6f44a9bf9835c2118e7c21ca5d0d4418bb637b`

```dockerfile
```

-	Layers:
	-	`sha256:6fc3d4bb1aa2ba503c1affbaf120d96d45d8d3ea7993fc14461fb9e54e76d571`  
		Last Modified: Tue, 30 Jul 2024 23:55:58 GMT  
		Size: 109.9 KB (109883 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e79d52fc16bd67e46e1673219ca6b18cc7b590e551bc1348ea02aea81090b853`  
		Last Modified: Tue, 30 Jul 2024 23:55:58 GMT  
		Size: 16.1 KB (16087 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.20` - linux; arm variant v6

```console
$ docker pull bash@sha256:659b7dd7f49e622a53f93dccd7196defe4cf79ea52c5b0449f7f458890a0ba34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6217415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6fb4e0e820a014e76130d715581635d0ed07953328abeafae24f97d11a05f6f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 22 Jul 2024 21:49:18 GMT
ADD file:85f927c1895bee1d0b095b2905c8d47ada8773f13e03fd4a201f718103ef7958 in / 
# Mon, 22 Jul 2024 21:49:19 GMT
CMD ["/bin/sh"]
# Tue, 30 Jul 2024 02:00:38 GMT
ENV _BASH_COMMIT=d5ef283cbdd08217efdc55974a6a8a2c52a7562f
# Tue, 30 Jul 2024 02:00:38 GMT
ENV _BASH_VERSION=devel-20240726
# Tue, 30 Jul 2024 02:00:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 30 Jul 2024 02:00:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 Jul 2024 02:00:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Jul 2024 02:00:38 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:ae2458422e4465e718700cd0c5970c709804ded4caa7b7f317eada5d16878e29`  
		Last Modified: Mon, 22 Jul 2024 21:49:42 GMT  
		Size: 3.4 MB (3365189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c51ed38ac5900548e9af8dbf9b59e63995215ed09616fb91db1bdd5294da966`  
		Last Modified: Tue, 30 Jul 2024 23:55:43 GMT  
		Size: 2.9 MB (2851889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fa854fa3906059ef8fb80638daef9665415ef3f45a86eb943c065c3e0caef45`  
		Last Modified: Tue, 30 Jul 2024 23:55:42 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.20` - unknown; unknown

```console
$ docker pull bash@sha256:d37520ffdd6e24091efdac670c39172492dd705b08e38aaa479f0fbbc1b272a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 KB (15937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb5a28c40563763ef7568e956679d7e639b6e274d84a41c87286eba3ea265f3c`

```dockerfile
```

-	Layers:
	-	`sha256:6d8b7bb13e22c68edac816546e93e8508c32597353cee70aaf0b83330b1a93a5`  
		Last Modified: Tue, 30 Jul 2024 23:55:42 GMT  
		Size: 15.9 KB (15937 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.20` - linux; arm variant v7

```console
$ docker pull bash@sha256:b2f31ba99665880b31425e2679ef486f34fc0bc615b961cae63457c69ebb7b14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5890902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4653c7f21c1a68d8acac30ec4495d3f06087240fd87f2f7454faeb93b3d960d3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 22 Jul 2024 21:59:47 GMT
ADD file:816da1ff7b962e1f52c650dfd66caeb2b88f3ab9fadc249c30f86ebe5372538c in / 
# Mon, 22 Jul 2024 21:59:47 GMT
CMD ["/bin/sh"]
# Tue, 30 Jul 2024 02:00:38 GMT
ENV _BASH_COMMIT=d5ef283cbdd08217efdc55974a6a8a2c52a7562f
# Tue, 30 Jul 2024 02:00:38 GMT
ENV _BASH_VERSION=devel-20240726
# Tue, 30 Jul 2024 02:00:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 30 Jul 2024 02:00:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 Jul 2024 02:00:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Jul 2024 02:00:38 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:9c6652a37da7fb600faac56897745bdde89a4f9bd260a082b6bf4a0d173b5906`  
		Last Modified: Mon, 22 Jul 2024 22:00:23 GMT  
		Size: 3.1 MB (3094960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d37b674ce1b0a02522b90e7ca8086ba16736b3c0cfb7f7c4a3974b3a726b20a`  
		Last Modified: Tue, 30 Jul 2024 23:55:38 GMT  
		Size: 2.8 MB (2795613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf04484953e8212fa37e16a825859ce4bcdb6fb193ab17fa645a6a36d9de0aeb`  
		Last Modified: Tue, 30 Jul 2024 23:55:38 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.20` - unknown; unknown

```console
$ docker pull bash@sha256:7f9c1b4ee7265d136342e87d4fecb5876df100d38622a0b201efd4da1ac2ff7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.1 KB (126076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fecd865822f3da9f42fba8ed7c0841589573acf0864af2a44706b2c8b297a2e9`

```dockerfile
```

-	Layers:
	-	`sha256:fbff8c74638368d2d8091e837524b9b539d51098f95603b555596adc61549a28`  
		Last Modified: Tue, 30 Jul 2024 23:55:38 GMT  
		Size: 109.9 KB (109919 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:258d528d2e8017d99fd10f9a725556f836f976cbdbd7859e5c92026fa92f6ee8`  
		Last Modified: Tue, 30 Jul 2024 23:55:38 GMT  
		Size: 16.2 KB (16157 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull bash@sha256:075f6b3abeaee7887d6864d4f06e141f952f9585d9c311bb8199e0ebb7a64734
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7089564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da9f52d50afb2793a9ee33a527acffedba82ba1f30758a47b62b02f6803e3dca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:13 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 22 Jul 2024 21:44:13 GMT
CMD ["/bin/sh"]
# Tue, 30 Jul 2024 02:00:38 GMT
ENV _BASH_COMMIT=d5ef283cbdd08217efdc55974a6a8a2c52a7562f
# Tue, 30 Jul 2024 02:00:38 GMT
ENV _BASH_VERSION=devel-20240726
# Tue, 30 Jul 2024 02:00:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 30 Jul 2024 02:00:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 Jul 2024 02:00:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Jul 2024 02:00:38 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d48d901422a2ccfcb37921b7794c2bde79d74f7f74d5c74034bffba93faefd70`  
		Last Modified: Tue, 30 Jul 2024 23:55:33 GMT  
		Size: 3.0 MB (3002298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43649e6b98e2655919b326c9ba2b4585e14045e354cfac6f3bf0393a4e5ea7bd`  
		Last Modified: Tue, 30 Jul 2024 23:55:32 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.20` - unknown; unknown

```console
$ docker pull bash@sha256:4a01dbe1a748ca2ec4f919d14509ed38418fada823025d8544e84b3dd4b0b24b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.3 KB (126326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d944fbc3942917e01678d89ccbb30c838f30831fcd30d7005735a1c8f416b152`

```dockerfile
```

-	Layers:
	-	`sha256:46940e1e43013edcf3cf11e17cfcfb0a724dde478d5be61f48f470dc30646aa3`  
		Last Modified: Tue, 30 Jul 2024 23:55:33 GMT  
		Size: 109.9 KB (109939 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7b21ddede31de824eea35243eba2c97384d543c16c0f7fbb3bcc9ec8b3e26ad`  
		Last Modified: Tue, 30 Jul 2024 23:55:32 GMT  
		Size: 16.4 KB (16387 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.20` - linux; 386

```console
$ docker pull bash@sha256:da98144be26ba6362c3c47001190281d9cdd7b3c7dc293cdeb6d3af069315d99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6313115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:100648a63a093890f7039060e44729011a9b006b1ff5a8c321bc9159f9223ff0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 22 Jul 2024 21:38:29 GMT
ADD file:e5b77b9337c5f89df9a65f8c439736a6d79e68274100ab1a1d7d61359a9abf5d in / 
# Mon, 22 Jul 2024 21:38:30 GMT
CMD ["/bin/sh"]
# Tue, 30 Jul 2024 02:00:38 GMT
ENV _BASH_COMMIT=d5ef283cbdd08217efdc55974a6a8a2c52a7562f
# Tue, 30 Jul 2024 02:00:38 GMT
ENV _BASH_VERSION=devel-20240726
# Tue, 30 Jul 2024 02:00:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 30 Jul 2024 02:00:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 Jul 2024 02:00:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Jul 2024 02:00:38 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:2585500d54afa42a6b579f9ed6f62b49c5fb21c2653f79194342804bde8770fe`  
		Last Modified: Mon, 22 Jul 2024 21:38:55 GMT  
		Size: 3.5 MB (3468071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9126298cf4b283aaf6d4de9c17097f033db7621327ba2427dd3212c47d5634b`  
		Last Modified: Tue, 30 Jul 2024 23:55:53 GMT  
		Size: 2.8 MB (2844707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:427bb522ae261c1a6c6bae3c20eb27a3f2c369b95286987f83ffbe7f75b2832a`  
		Last Modified: Tue, 30 Jul 2024 23:55:53 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.20` - unknown; unknown

```console
$ docker pull bash@sha256:672572c3df918df24494973c454a24389c12987860983af9d5df04e52b9b4aeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.9 KB (125916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94ca8a5c4a0a3961db17954add4cac5fab2ac7e82858a0503982278dc499ee2d`

```dockerfile
```

-	Layers:
	-	`sha256:aa6d90e814cba1d2bc0a7d6d460a49dade864caf48c36f37571532fdb292bd02`  
		Last Modified: Tue, 30 Jul 2024 23:55:53 GMT  
		Size: 109.9 KB (109858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38b026ef971ed320b25da514630e72e1754df276ab2a72089ced461621829de2`  
		Last Modified: Tue, 30 Jul 2024 23:55:53 GMT  
		Size: 16.1 KB (16058 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.20` - linux; ppc64le

```console
$ docker pull bash@sha256:952c2e2f5a74f3ae7a058c6f2729913a23b9425364ff70ac400226300d52bb14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6746308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6da01a2b729370d0bb1dff288e92e6a256c83be3983b9e0c43eb57d5bb67d009`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 22 Jul 2024 21:26:21 GMT
ADD file:9fcad21b83b7efd6ef267ba714c3ef5a8d4d2064a0bdf528cbb17d0c3388f03f in / 
# Mon, 22 Jul 2024 21:26:22 GMT
CMD ["/bin/sh"]
# Tue, 30 Jul 2024 02:00:38 GMT
ENV _BASH_COMMIT=d5ef283cbdd08217efdc55974a6a8a2c52a7562f
# Tue, 30 Jul 2024 02:00:38 GMT
ENV _BASH_VERSION=devel-20240726
# Tue, 30 Jul 2024 02:00:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 30 Jul 2024 02:00:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 Jul 2024 02:00:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Jul 2024 02:00:38 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:6e59b4988c495782a5b0c8f8d6698931851c16c5c0fc5ef09cbb0637ade56e36`  
		Last Modified: Mon, 22 Jul 2024 21:26:52 GMT  
		Size: 3.6 MB (3571555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbf5f92cafc5fcd5e7796dd846874e58153e7f025aa0b208d92294e8057cc793`  
		Last Modified: Tue, 30 Jul 2024 23:55:46 GMT  
		Size: 3.2 MB (3174418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f3b3f961b08906e53ee5016456d025eb866a06ccbd174c5a86ce83c8a85ac96`  
		Last Modified: Tue, 30 Jul 2024 23:55:45 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.20` - unknown; unknown

```console
$ docker pull bash@sha256:ecf7364533432cc2603dbbd8f37b353f1c1f45b3d82b0ad88e7f70cccdd95d7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.1 KB (124087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20fc68d73a4a84f65d93dcc9f943ae0cdb3f20a79047be5ae591dab246609dc7`

```dockerfile
```

-	Layers:
	-	`sha256:be1dbf738757456714a4458387aae0db9f4368589532ac9742332beca10bedb3`  
		Last Modified: Tue, 30 Jul 2024 23:55:46 GMT  
		Size: 108.0 KB (107963 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e72c9ed088556aeaa9a33c5e2a8bcfac7f14e564b2283770c22558f26d39ba38`  
		Last Modified: Tue, 30 Jul 2024 23:55:46 GMT  
		Size: 16.1 KB (16124 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.20` - linux; riscv64

```console
$ docker pull bash@sha256:92218af7b17a8619ec068df68ac7f6642f3115b1d95da4e47fbdf8fc9704079e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6223687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b5d10ba99053cffaabb73d77511ca0e4b738c575037314e8ff8357d56fb5f41`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 22 Jul 2024 22:21:00 GMT
ADD file:cdf7088bbd70519f0f5d7b4249df34386e40f0194752f45842b3d85f2d331cf5 in / 
# Mon, 22 Jul 2024 22:21:00 GMT
CMD ["/bin/sh"]
# Tue, 30 Jul 2024 02:00:38 GMT
ENV _BASH_COMMIT=d5ef283cbdd08217efdc55974a6a8a2c52a7562f
# Tue, 30 Jul 2024 02:00:38 GMT
ENV _BASH_VERSION=devel-20240726
# Tue, 30 Jul 2024 02:00:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 30 Jul 2024 02:00:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 Jul 2024 02:00:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Jul 2024 02:00:38 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:faf447acae27573624c0613a79c4bcf1f9bc46d29f523140352abfd3f7691282`  
		Last Modified: Mon, 22 Jul 2024 22:21:18 GMT  
		Size: 3.4 MB (3370673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc12588cdb6c5c75e0a1ae9054eab9de4c282ec5dafa8fddeb51288fb65906dd`  
		Last Modified: Wed, 31 Jul 2024 00:02:36 GMT  
		Size: 2.9 MB (2852676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55138fbb62e66b9cd541ac7d446efaf628d60f22c0013c26b1d462cd02cc3f52`  
		Last Modified: Wed, 31 Jul 2024 00:02:35 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.20` - unknown; unknown

```console
$ docker pull bash@sha256:67b563aa90c5371d32894d6514ee7f13fb7307f7d441bb4683a333b298a77c62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.1 KB (124084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e30b0ca0cf6d72518788c78032387ce56193bbb6d81ebdc3d6e2b4dcb8c9e33f`

```dockerfile
```

-	Layers:
	-	`sha256:9ea4aa55c7aa3d9451e63a3cd7e5daba68b26c7ae11997e20ac9e63f9b91badd`  
		Last Modified: Wed, 31 Jul 2024 00:02:36 GMT  
		Size: 108.0 KB (107959 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43a752f6cdc01a298b9c447ea62e05f631994603a53464539f455415510d266c`  
		Last Modified: Wed, 31 Jul 2024 00:02:35 GMT  
		Size: 16.1 KB (16125 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.20` - linux; s390x

```console
$ docker pull bash@sha256:f6737f5d081ab85ae015cf69672fc4f6d328fe8689a5647576a1e4179914bcbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6463643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d87e9f95d2f7130dc6e137623a077dcfcae49b6c6d0aeac435ac65490badc591`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 22 Jul 2024 21:50:06 GMT
ADD file:63d382fb7a431c57868274a368a659bde32a60ae0cd05c8af34c3d6a57066a77 in / 
# Mon, 22 Jul 2024 21:50:07 GMT
CMD ["/bin/sh"]
# Tue, 30 Jul 2024 02:00:38 GMT
ENV _BASH_COMMIT=d5ef283cbdd08217efdc55974a6a8a2c52a7562f
# Tue, 30 Jul 2024 02:00:38 GMT
ENV _BASH_VERSION=devel-20240726
# Tue, 30 Jul 2024 02:00:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 30 Jul 2024 02:00:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 Jul 2024 02:00:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Jul 2024 02:00:38 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:834c666d55eae0e308600077be061a01680e7cd02b579be887d9469075f0d943`  
		Last Modified: Mon, 22 Jul 2024 21:51:06 GMT  
		Size: 3.5 MB (3461066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ceaa5b8552a78945c8923cc641f6fe732a2e4c69025519d51f57930aceb8d54`  
		Last Modified: Tue, 30 Jul 2024 23:55:46 GMT  
		Size: 3.0 MB (3002240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82186d5e78ea2f1a704e53e7bb88f36c4e3cceb18074ce0502fba3a0d6821a00`  
		Last Modified: Tue, 30 Jul 2024 23:55:46 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.20` - unknown; unknown

```console
$ docker pull bash@sha256:3c2ca21f01a1b7d0e6ace8b60da2f4f780f20a44e220f69c36228fc8de9700e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.0 KB (124016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94ff704e4f39d6285e02751da71093be50455f0c365c0ba3c297d8f42afb1431`

```dockerfile
```

-	Layers:
	-	`sha256:1de2eb7edd6a845045089b34daa93e378e4d1ee85166e0410c8a84f5927e5f83`  
		Last Modified: Tue, 30 Jul 2024 23:55:46 GMT  
		Size: 107.9 KB (107929 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e03779516ada7d24d6e671d6549aeb1315b37b08732bb00bd31344d394bb575e`  
		Last Modified: Tue, 30 Jul 2024 23:55:46 GMT  
		Size: 16.1 KB (16087 bytes)  
		MIME: application/vnd.in-toto+json
