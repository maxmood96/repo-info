## `bash:devel-20240711-alpine3.20`

```console
$ docker pull bash@sha256:71592690fd1c31f2caed98e14aaeb016fb99a69691e59cf5328cca98129ecb30
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

### `bash:devel-20240711-alpine3.20` - linux; amd64

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

### `bash:devel-20240711-alpine3.20` - unknown; unknown

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

### `bash:devel-20240711-alpine3.20` - linux; arm variant v6

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

### `bash:devel-20240711-alpine3.20` - unknown; unknown

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

### `bash:devel-20240711-alpine3.20` - linux; arm variant v7

```console
$ docker pull bash@sha256:4fb98733f6c115a5fdb825da0a1049841f4daf797f5e080ec5a4a7d557e78fb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5888716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32ec3ac45abf74cb9fcc17f88ce2e0dac4e52ac912be37f7295e300f03bcffa8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 16 Jul 2024 04:18:07 GMT
ADD file:816da1ff7b962e1f52c650dfd66caeb2b88f3ab9fadc249c30f86ebe5372538c in / 
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
	-	`sha256:9c6652a37da7fb600faac56897745bdde89a4f9bd260a082b6bf4a0d173b5906`  
		Last Modified: Mon, 22 Jul 2024 22:00:23 GMT  
		Size: 3.1 MB (3094960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5126a95889f936bfb1473525faf0e6122b517d923dcedf6f563c304637bca7d`  
		Last Modified: Tue, 23 Jul 2024 11:31:56 GMT  
		Size: 2.8 MB (2793417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89c25504cf0e5df59a666ed713dda44b27e2a08e215d5a6aa7b475ca6f3843e4`  
		Last Modified: Tue, 23 Jul 2024 11:31:56 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20240711-alpine3.20` - unknown; unknown

```console
$ docker pull bash@sha256:915ec899f3431fb7b22f7c06b3f838ac9a6384264c3e026a6cc6003e8b10a1cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.3 KB (126264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6e4c1dc4480079d0b0b63090c0546a4b976219991a0b3c8cace84cc362f0163`

```dockerfile
```

-	Layers:
	-	`sha256:d19e6d0eb0474286627e81e0a8985bfb87002cecdf42dc63b7c800de1e87be64`  
		Last Modified: Tue, 23 Jul 2024 11:31:56 GMT  
		Size: 109.9 KB (109919 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41beb1fe20d214c636c86b91f49f31146f3ca27452ee17d6e6874889aca96b2f`  
		Last Modified: Tue, 23 Jul 2024 11:31:55 GMT  
		Size: 16.3 KB (16345 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20240711-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull bash@sha256:c3dfd9d5f1c890c6f2d20050f495939800c070089107a82236715de52bdfdc45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7085736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c6bab96f7286603db64fb669db8bea14373e47351ad752a4d9aa368e55c77c4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 16 Jul 2024 04:18:07 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
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
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:897e4b23b30c14f6360789d10e8f8fee1482b9f3f55cf91941da3f04dca0cbff`  
		Last Modified: Tue, 23 Jul 2024 11:14:22 GMT  
		Size: 3.0 MB (2998472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18e290f201bf5f0ea749ee78dae17621a3f70ddc085c6b6c7f60c81c1290ab31`  
		Last Modified: Tue, 23 Jul 2024 11:14:22 GMT  
		Size: 330.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20240711-alpine3.20` - unknown; unknown

```console
$ docker pull bash@sha256:4331b4dfedae64f332119147f64895fa900c984dfab16fa11092632be9fd05bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.5 KB (126514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:469e2b8b068c6f6e6143879ac2fb525ca46b04330aeb7356fc9e852071da19a1`

```dockerfile
```

-	Layers:
	-	`sha256:9763915992d6398080b4de7f63a76184b677c4a480800ae2fc24bf5cf0138ce3`  
		Last Modified: Tue, 23 Jul 2024 11:14:22 GMT  
		Size: 109.9 KB (109939 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f19ddb31a1b08e3f1595d85bf94af02fa37f046918504caeafafcbf828512eb`  
		Last Modified: Tue, 23 Jul 2024 11:14:22 GMT  
		Size: 16.6 KB (16575 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20240711-alpine3.20` - linux; 386

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

### `bash:devel-20240711-alpine3.20` - unknown; unknown

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

### `bash:devel-20240711-alpine3.20` - linux; ppc64le

```console
$ docker pull bash@sha256:65a19b1bbdddc38a6f1cebf9cdad92d96738e6553104216f35f7863c2d3d2224
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6741488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59b30f67e0ce77eef63a6377c518a1332c68ebdb275e18a4d3defc3203ecdc34`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 16 Jul 2024 04:18:07 GMT
ADD file:9fcad21b83b7efd6ef267ba714c3ef5a8d4d2064a0bdf528cbb17d0c3388f03f in / 
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
	-	`sha256:6e59b4988c495782a5b0c8f8d6698931851c16c5c0fc5ef09cbb0637ade56e36`  
		Last Modified: Mon, 22 Jul 2024 21:26:52 GMT  
		Size: 3.6 MB (3571555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7129a10ac29338c9e016c03d68d15081027c4ed37ecf81eb6e4637b9011d6ec`  
		Last Modified: Tue, 23 Jul 2024 08:12:19 GMT  
		Size: 3.2 MB (3169597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4486620b8fdc0e7663342d2eab3018dbe493cf6b4fc78c722ea180b576063cf4`  
		Last Modified: Tue, 23 Jul 2024 08:12:19 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20240711-alpine3.20` - unknown; unknown

```console
$ docker pull bash@sha256:d6aa418ccaeae5cd1c4c03b248d3e0c26536680e71f7be2df8b570f9b7ce1d69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 KB (124275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81a1144bfd0de7bdb33f68a0e3044ec48a3340bc4e63bd03e30826ae061229f4`

```dockerfile
```

-	Layers:
	-	`sha256:5f9c58e4cae9cfd0b7d29db0f95f832a1c2d9428cdc28053418d469d11d95bf5`  
		Last Modified: Tue, 23 Jul 2024 08:12:19 GMT  
		Size: 108.0 KB (107963 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bbd197138d2a0c19a7c5c16bfddd0d101a73055ce3472fb9be27e5330edc6ab`  
		Last Modified: Tue, 23 Jul 2024 08:12:19 GMT  
		Size: 16.3 KB (16312 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20240711-alpine3.20` - linux; riscv64

```console
$ docker pull bash@sha256:36dd408e6fc926af19a864791e23acc5c687880abe10152bd3edfc55c8046cba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6218994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e87dd04a8afc753c046b99e1c9e9c3908f36dd25f455d30cdc3516c38930c9f6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 16 Jul 2024 04:18:07 GMT
ADD file:cdf7088bbd70519f0f5d7b4249df34386e40f0194752f45842b3d85f2d331cf5 in / 
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
	-	`sha256:faf447acae27573624c0613a79c4bcf1f9bc46d29f523140352abfd3f7691282`  
		Last Modified: Mon, 22 Jul 2024 22:21:18 GMT  
		Size: 3.4 MB (3370673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58f11d45d157fd3c74c3a37342e1dd2d840f957bab954b87f29f99ca2a9ef5fc`  
		Last Modified: Tue, 23 Jul 2024 12:59:51 GMT  
		Size: 2.8 MB (2847983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d19cf2effc57cc16bc7a6d2d85bed5a173351f40b8d4a5b47df03600f1b008d9`  
		Last Modified: Tue, 23 Jul 2024 12:59:50 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20240711-alpine3.20` - unknown; unknown

```console
$ docker pull bash@sha256:e36930f3e1976b30fcbf6d79ed62f9425d02dfa00ec35464c0f394dedc8ba1b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 KB (124272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8da1a6fd6da9bf2031775d55a9b8a1e90376c8c6c056ef038af0011ff3d7f29`

```dockerfile
```

-	Layers:
	-	`sha256:3fb987bb7ce96e780fc6b93186ece2ef8a79636aae5387b0adc92e065f8c1378`  
		Last Modified: Tue, 23 Jul 2024 12:59:50 GMT  
		Size: 108.0 KB (107959 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:861e907379874f8dc8127cde0b6df6ab0ef93eacc377f8c6e16ff1884be0dbdb`  
		Last Modified: Tue, 23 Jul 2024 12:59:50 GMT  
		Size: 16.3 KB (16313 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20240711-alpine3.20` - linux; s390x

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

### `bash:devel-20240711-alpine3.20` - unknown; unknown

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
