## `bash:devel-alpine3.20`

```console
$ docker pull bash@sha256:715823839f7800815b1216ea69dd8992f12c1bdb5f313fda0e8aa27ecaa1502b
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
$ docker pull bash@sha256:ea8f721fc9fd57fd061f621f0564405fcdc51eb2627807e47ae02da82e7040dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6520318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9eccfa5c0de0a100ef8f65b59f9df29f039c95a7cd86688f09d30f1842f1e96`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 16 Jul 2024 04:18:07 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Tue, 16 Jul 2024 04:18:07 GMT
CMD ["/bin/sh"]
# Tue, 16 Jul 2024 04:18:07 GMT
ENV _BASH_COMMIT=d3e86e66ce857a8dc02e3116fd98b6e5b34d6364
# Tue, 16 Jul 2024 04:18:07 GMT
ENV _BASH_VERSION=devel-20240711
# Tue, 16 Jul 2024 04:18:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 16 Jul 2024 04:18:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jul 2024 04:18:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jul 2024 04:18:07 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7c4e907f0ef8a077c604ec0beeb60e842766a6ca44aa77ef7a6e62a104d3215`  
		Last Modified: Mon, 22 Jul 2024 23:03:51 GMT  
		Size: 2.9 MB (2897088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:163c88c95a4a6d85e331014addbc425991fc495770634d03bd60c44e8e28b402`  
		Last Modified: Mon, 22 Jul 2024 23:03:51 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.20` - unknown; unknown

```console
$ docker pull bash@sha256:2e8706214b16e60b77f7ce88f3691f01b1cff9a5b0d9ee72dd09e27471493c84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.2 KB (126158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90ec763d24881d040d1de48e00297a30b5ae39754dbff02a799295d43f209f31`

```dockerfile
```

-	Layers:
	-	`sha256:8d56e1244421faa4b86ef933d88dd5c7f61f7aad50ad6ea4312f0dc13ad638a5`  
		Last Modified: Mon, 22 Jul 2024 23:03:51 GMT  
		Size: 109.9 KB (109883 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:045148cfbe9532c41cdc7b5b2cb0a2e92311ba2d4b6c5a83f2fdc93265a5a5a8`  
		Last Modified: Mon, 22 Jul 2024 23:03:51 GMT  
		Size: 16.3 KB (16275 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.20` - linux; arm variant v6

```console
$ docker pull bash@sha256:b7246d822b2ae936b1d5a2af14335f4291841e4a7a72d87de370ba0d12fda7b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6211980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aa12bcc05863cd5eb28890e9d20da6bcb419924163051e39088e1e37449fe89`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 16 Jul 2024 04:18:07 GMT
ADD file:85f927c1895bee1d0b095b2905c8d47ada8773f13e03fd4a201f718103ef7958 in / 
# Tue, 16 Jul 2024 04:18:07 GMT
CMD ["/bin/sh"]
# Tue, 16 Jul 2024 04:18:07 GMT
ENV _BASH_COMMIT=d3e86e66ce857a8dc02e3116fd98b6e5b34d6364
# Tue, 16 Jul 2024 04:18:07 GMT
ENV _BASH_VERSION=devel-20240711
# Tue, 16 Jul 2024 04:18:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 16 Jul 2024 04:18:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jul 2024 04:18:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jul 2024 04:18:07 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:ae2458422e4465e718700cd0c5970c709804ded4caa7b7f317eada5d16878e29`  
		Last Modified: Mon, 22 Jul 2024 21:49:42 GMT  
		Size: 3.4 MB (3365189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f460215ab39881660e195c32e3c2838bf52c3cfd3f6d7a8577983802d872f7c0`  
		Last Modified: Tue, 23 Jul 2024 01:21:04 GMT  
		Size: 2.8 MB (2846459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6314e6baebbc1764fb7227b9e8d937cf7a45612dde2ed849097dddc460ae338c`  
		Last Modified: Tue, 23 Jul 2024 01:21:04 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.20` - unknown; unknown

```console
$ docker pull bash@sha256:ecba8a75ccdcb7a4d1faebdfbc22ff11533397c0dc6e4eed0834ff550ac47f69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.1 KB (16126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d5ab6b78cfa124539db62385b67fbf49eaf656837bb34d45cd58091759e3cf4`

```dockerfile
```

-	Layers:
	-	`sha256:b4d02799bd69b17b74565ce7a820b28ae84287b7d756ea1f0399eb336860d782`  
		Last Modified: Tue, 23 Jul 2024 01:21:04 GMT  
		Size: 16.1 KB (16126 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.20` - linux; arm variant v7

```console
$ docker pull bash@sha256:18a9227d72bd1f615c3c2958cf41222e184510b0b0571acbe0562ae161a49e70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5888589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edd73ae5169809c8a2b19e1aed3eb221d4e25399ec8fcb45e47c57d40c7e7402`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 20 Jun 2024 18:00:28 GMT
ADD file:4d58f44e3cedeba6fad741c79bc5acab1a9f2a2f597c854dc3bb8b8595ebf3e1 in / 
# Thu, 20 Jun 2024 18:00:28 GMT
CMD ["/bin/sh"]
# Tue, 16 Jul 2024 04:18:07 GMT
ENV _BASH_COMMIT=d3e86e66ce857a8dc02e3116fd98b6e5b34d6364
# Tue, 16 Jul 2024 04:18:07 GMT
ENV _BASH_VERSION=devel-20240711
# Tue, 16 Jul 2024 04:18:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 16 Jul 2024 04:18:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jul 2024 04:18:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jul 2024 04:18:07 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:3fb467f9cb36e54d3cb8806db734a6c640048f3dc270b506ec1f111640905b79`  
		Last Modified: Thu, 20 Jun 2024 18:00:55 GMT  
		Size: 3.1 MB (3094856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b292cdff893c4ecb0ee3e458ff3504c5d0a39af3e3bc87d3426a6f5d54aad6ab`  
		Last Modified: Tue, 16 Jul 2024 21:59:00 GMT  
		Size: 2.8 MB (2793397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1148f312c981a623c772ff4fac7d0e4d07e7d4f66eda7de3ff78a0c46aba1db4`  
		Last Modified: Tue, 16 Jul 2024 21:58:59 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.20` - unknown; unknown

```console
$ docker pull bash@sha256:9085ca4e99c3f9596b487a06ef33916cb93101b1182b68ff09e63cb54e6b86e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.3 KB (126264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78276efe049cd8ea44d32ab204b38d2555c448115226e96b45b521e8d741dc6e`

```dockerfile
```

-	Layers:
	-	`sha256:a3e3dd8b801312aca457bbdd35e1b106f005f460fcca94da9aa3977864734963`  
		Last Modified: Tue, 16 Jul 2024 21:58:59 GMT  
		Size: 109.9 KB (109919 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:941dd2899bafd23291411a305a31b7fb9ade61b428342298c0549b78f16c7641`  
		Last Modified: Tue, 16 Jul 2024 21:58:59 GMT  
		Size: 16.3 KB (16345 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull bash@sha256:5955c4976ca06e6eedac53a5be9d974df1487df0ff81cb1710b68d4c0f5d2448
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7087634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a20a9c07fd803f10fc2860b80f9853023515c9e1bf28676570b83a3a2a08a66`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:35 GMT
ADD file:033626ac44156f3d5800a602c46870486b1492b9ba26096eaa66cceb6fcead77 in / 
# Thu, 20 Jun 2024 17:40:35 GMT
CMD ["/bin/sh"]
# Tue, 16 Jul 2024 04:18:07 GMT
ENV _BASH_COMMIT=d3e86e66ce857a8dc02e3116fd98b6e5b34d6364
# Tue, 16 Jul 2024 04:18:07 GMT
ENV _BASH_VERSION=devel-20240711
# Tue, 16 Jul 2024 04:18:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 16 Jul 2024 04:18:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jul 2024 04:18:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jul 2024 04:18:07 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:a258b2a6b59a7aa244d8ceab095c7f8df726f27075a69fca7ad8490f3f63148a`  
		Last Modified: Thu, 20 Jun 2024 17:40:58 GMT  
		Size: 4.1 MB (4088800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a497476a6dfa249d1ce4d0ef97af41c30c05f2411305eef40eaa5310b714aaa`  
		Last Modified: Tue, 16 Jul 2024 21:58:18 GMT  
		Size: 3.0 MB (2998498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ec6c68081c295a2af5c74c606edc7df2bf5335f79471842dcaaed054225ed81`  
		Last Modified: Tue, 16 Jul 2024 21:58:17 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.20` - unknown; unknown

```console
$ docker pull bash@sha256:6d685e6705ff7238785fc525e26a16eba9f8f9f695854961281759caff793e6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.5 KB (126514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f72d86a8513774b0f2c6cbdceb0a601e02134955afb487c5c101117d40d4cf9`

```dockerfile
```

-	Layers:
	-	`sha256:44d80a945736f4fbd7d966fc37abeab82b9aa48810b1504137853f61582ecc80`  
		Last Modified: Tue, 16 Jul 2024 21:58:17 GMT  
		Size: 109.9 KB (109939 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68935744fffef046ac1651fdb063a7a810679f5809bae766277ae185d6774377`  
		Last Modified: Tue, 16 Jul 2024 21:58:17 GMT  
		Size: 16.6 KB (16575 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.20` - linux; 386

```console
$ docker pull bash@sha256:167997275b69edc547e9adc0f383694b3dbac96e431a3837d2ea2ac1852bf715
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6309736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:016684c72a5ad1bf8a2f20b1a4400703efaf5a7ea45a97fc1073413816e60d3a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 16 Jul 2024 04:18:07 GMT
ADD file:e5b77b9337c5f89df9a65f8c439736a6d79e68274100ab1a1d7d61359a9abf5d in / 
# Tue, 16 Jul 2024 04:18:07 GMT
CMD ["/bin/sh"]
# Tue, 16 Jul 2024 04:18:07 GMT
ENV _BASH_COMMIT=d3e86e66ce857a8dc02e3116fd98b6e5b34d6364
# Tue, 16 Jul 2024 04:18:07 GMT
ENV _BASH_VERSION=devel-20240711
# Tue, 16 Jul 2024 04:18:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 16 Jul 2024 04:18:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jul 2024 04:18:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jul 2024 04:18:07 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:2585500d54afa42a6b579f9ed6f62b49c5fb21c2653f79194342804bde8770fe`  
		Last Modified: Mon, 22 Jul 2024 21:38:55 GMT  
		Size: 3.5 MB (3468071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d38fd8cc5762d899025b9f5b4c8bcab260f2095a4faf0895d1e5ab4a6cef2d14`  
		Last Modified: Mon, 22 Jul 2024 22:07:17 GMT  
		Size: 2.8 MB (2841328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e5d365812b4440e9ab62b262c10166ce394807d6ce478fe8d4a27de7ab8f2d4`  
		Last Modified: Mon, 22 Jul 2024 22:07:16 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.20` - unknown; unknown

```console
$ docker pull bash@sha256:39a5b308d3a9bd94806b5c052ff258f50df5a502644b5bf280cf86765373af61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.1 KB (126104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a299cd000a38c74d4643ddfb1693dee293aa7bece1f724efda1448264ef3db5`

```dockerfile
```

-	Layers:
	-	`sha256:dd1d6e99fd7cfc94810af8ea2ea1d51de790b7b1ba90d381a35ce9a28694d400`  
		Last Modified: Mon, 22 Jul 2024 22:07:16 GMT  
		Size: 109.9 KB (109858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e517960bdfc3aaa780c2339216c93a0ae624870d47c3647f87eb9dd103df353`  
		Last Modified: Mon, 22 Jul 2024 22:07:16 GMT  
		Size: 16.2 KB (16246 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.20` - linux; ppc64le

```console
$ docker pull bash@sha256:7150c29000c054337a266ef932fd69940feac55f5a2dc4fc905d8692eef06f84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6741583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a72129d688b8a81919c2d8d48b808ad641afc44ed184c5d36faaa6208e2a810d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 20 Jun 2024 18:18:21 GMT
ADD file:c98fdd4075ec8eb66a469bd36f2d1369030638ad4b76778b5ad9c787b9f63c8b in / 
# Thu, 20 Jun 2024 18:18:22 GMT
CMD ["/bin/sh"]
# Tue, 16 Jul 2024 04:18:07 GMT
ENV _BASH_COMMIT=d3e86e66ce857a8dc02e3116fd98b6e5b34d6364
# Tue, 16 Jul 2024 04:18:07 GMT
ENV _BASH_VERSION=devel-20240711
# Tue, 16 Jul 2024 04:18:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 16 Jul 2024 04:18:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jul 2024 04:18:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jul 2024 04:18:07 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:b02dcd5eb44e382ea711bca074a007403db63dacf55f888b3a87214d1052dd50`  
		Last Modified: Thu, 20 Jun 2024 18:18:55 GMT  
		Size: 3.6 MB (3571699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33cc5bc0cc99be8020a49551f13aad72c662eab1f04ca03c97c57ef0c54cf604`  
		Last Modified: Tue, 16 Jul 2024 21:58:28 GMT  
		Size: 3.2 MB (3169550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6459b6aa8afe4e2882302299ab2026f63d2942f8b9d36a03cee2acee05d1bc9a`  
		Last Modified: Tue, 16 Jul 2024 21:58:27 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.20` - unknown; unknown

```console
$ docker pull bash@sha256:551ef8cfe766cdf81c32f7309ef59475a85ca67b950e952592efdd669b2e7a44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 KB (124276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76a7ee9f93c5357fde9ade6fa16c632e1432e233a6ba0723fa4060f70b2d6326`

```dockerfile
```

-	Layers:
	-	`sha256:12ebc2ee047284b7956d225ebc12b71f95e3b9e2a655427489ebbbf63a0f564c`  
		Last Modified: Tue, 16 Jul 2024 21:58:28 GMT  
		Size: 108.0 KB (107963 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81a2039b5d629d5b5d7027acf8b92bc372fef06f4320111adf201ae43e28267d`  
		Last Modified: Tue, 16 Jul 2024 21:58:27 GMT  
		Size: 16.3 KB (16313 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.20` - linux; riscv64

```console
$ docker pull bash@sha256:91e3b51adb8d5fb59af196f4c4eabe6f9507125d529eaac8e3f69d0b4f04e08f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6219435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bb23518ba60005a5bcb5390f5e96c863a402e74b61e59641efd4bc1dade0461`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 20 Jun 2024 18:18:03 GMT
ADD file:851dbd05bad08468ee2a960e5f9f0aa9b19f1114ec52c39d1a28cd427344d0ef in / 
# Thu, 20 Jun 2024 18:18:04 GMT
CMD ["/bin/sh"]
# Tue, 16 Jul 2024 04:18:07 GMT
ENV _BASH_COMMIT=d3e86e66ce857a8dc02e3116fd98b6e5b34d6364
# Tue, 16 Jul 2024 04:18:07 GMT
ENV _BASH_VERSION=devel-20240711
# Tue, 16 Jul 2024 04:18:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 16 Jul 2024 04:18:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jul 2024 04:18:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jul 2024 04:18:07 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:d4714cc4c8bb5ceda619fceb44b088091082a8d2407d2008123fe93478722d1a`  
		Last Modified: Thu, 20 Jun 2024 18:18:22 GMT  
		Size: 3.4 MB (3371037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e8aec333df526ba42c7b1032f83bd7a9cc693ad69044549c06204e13a096156`  
		Last Modified: Tue, 16 Jul 2024 22:04:57 GMT  
		Size: 2.8 MB (2848061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc1a666617f595941ee4365634c4c02621fd0a7c3bd413af14dc5ac678b968bc`  
		Last Modified: Tue, 16 Jul 2024 22:04:56 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.20` - unknown; unknown

```console
$ docker pull bash@sha256:4fec2a681079423a867adbeb6968c6b1413797ebc147e68c335d8fe1d28c7f8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 KB (124272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a882284f827b6383e9aa8eab2ecad5b7a5405db8e3d26b8115ae652f28842320`

```dockerfile
```

-	Layers:
	-	`sha256:295a0b5c66ac82687aa9a67407271f760dd296e6c2f7de05e64ef1e63de43ffc`  
		Last Modified: Tue, 16 Jul 2024 22:04:57 GMT  
		Size: 108.0 KB (107959 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6cdd68aa0eb21022516bfd7818b402aeae66f18740bcb3500b99464a621c6c7d`  
		Last Modified: Tue, 16 Jul 2024 22:04:57 GMT  
		Size: 16.3 KB (16313 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.20` - linux; s390x

```console
$ docker pull bash@sha256:0742aabbe2df1d07f1d65033abdb9b7ac8cd75893c298fbafced944921ce0dad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6458576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03ddd6a5917fdbfb087e857cc7c966b476ed183e9be7c17e88d15c2baded25c7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 16 Jul 2024 04:18:07 GMT
ADD file:63d382fb7a431c57868274a368a659bde32a60ae0cd05c8af34c3d6a57066a77 in / 
# Tue, 16 Jul 2024 04:18:07 GMT
CMD ["/bin/sh"]
# Tue, 16 Jul 2024 04:18:07 GMT
ENV _BASH_COMMIT=d3e86e66ce857a8dc02e3116fd98b6e5b34d6364
# Tue, 16 Jul 2024 04:18:07 GMT
ENV _BASH_VERSION=devel-20240711
# Tue, 16 Jul 2024 04:18:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 16 Jul 2024 04:18:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jul 2024 04:18:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jul 2024 04:18:07 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:834c666d55eae0e308600077be061a01680e7cd02b579be887d9469075f0d943`  
		Last Modified: Mon, 22 Jul 2024 21:51:06 GMT  
		Size: 3.5 MB (3461066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a80b2b74b93cd83e98b38e8af5a3e0dc2c64945e21325d7321340b70ed9eb4e3`  
		Last Modified: Tue, 23 Jul 2024 06:34:20 GMT  
		Size: 3.0 MB (2997173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c184d3dcc74206e39a28e782c25d583b973f6563895d9d83f5cefbc42182c5aa`  
		Last Modified: Tue, 23 Jul 2024 06:34:20 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.20` - unknown; unknown

```console
$ docker pull bash@sha256:3a81d3a199a2982d82abccaa9ae53493d5c11dab38b35514d795ddcfb9e19459
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.2 KB (124204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7418534919a94222201993aa7e8f6fe57582f23ee33f28493cb2ca77ff5f7bdb`

```dockerfile
```

-	Layers:
	-	`sha256:644ce3219ab08196dcf80fe67694d66dda2ca5b842b12e37f891be68d42a8f60`  
		Last Modified: Tue, 23 Jul 2024 06:34:20 GMT  
		Size: 107.9 KB (107929 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d7910d7d669c01aa3da8d7df0f4f184eb1a9e66f26d4197af06419c1255f9e3`  
		Last Modified: Tue, 23 Jul 2024 06:34:20 GMT  
		Size: 16.3 KB (16275 bytes)  
		MIME: application/vnd.in-toto+json
