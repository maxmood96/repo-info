## `bash:devel-alpine3.19`

```console
$ docker pull bash@sha256:99fc78e13c1d0c0f87e4f2942d82a0801d3ab8567c8272863b82a9746de67f37
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
$ docker pull bash@sha256:884e2d941efdce49e7e51a22c2222e319cb4f81a2f423d4b995e802b79dcd594
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6284404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36479c435f0b9e73594e0267804c035a45d589c838bcc21fd77b020f3edaaf89`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Tue, 26 Mar 2024 04:18:04 GMT
ENV _BASH_COMMIT=8af5a8e0ca7d75f91eac7d81783af7d06d32dd50
# Tue, 26 Mar 2024 04:18:04 GMT
ENV _BASH_VERSION=devel-20240325
# Tue, 26 Mar 2024 04:18:04 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 26 Mar 2024 04:18:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 04:18:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Mar 2024 04:18:04 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a00e98300e8e08da637bc3b896a44680a899aed5b52d4e3dd390a73f4550b9d`  
		Last Modified: Tue, 26 Mar 2024 18:50:05 GMT  
		Size: 2.9 MB (2875342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7696838e9691500e5f7e8120dd0dab304595ed43fba264e3712b36a73f9cc43`  
		Last Modified: Tue, 26 Mar 2024 18:50:05 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.19` - unknown; unknown

```console
$ docker pull bash@sha256:bd58345209efe4d8391bd1c7b3ba36b02ef80870a94c83034a13ec54a1907614
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.8 KB (126786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aec82e4a411b2e536c1ee7ca3a0cf446211eb0271f739633e1b929209dcb8a7`

```dockerfile
```

-	Layers:
	-	`sha256:1e909a3d6bf1c6df4a60a2fcca6a6c5dff5b7d133cfba721f634a15edf72e444`  
		Last Modified: Tue, 26 Mar 2024 18:50:05 GMT  
		Size: 110.5 KB (110458 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4069a65a2430090b631e97db9144a6dc9b31578fc545f13862dc8dfd0ba6a05f`  
		Last Modified: Tue, 26 Mar 2024 18:50:05 GMT  
		Size: 16.3 KB (16328 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.19` - linux; arm variant v6

```console
$ docker pull bash@sha256:652052b638c1d226a0fab77cf6ebd4e0a6444369a7c0b1ed107a7917850dcb52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5990624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6faefa1708e393f3682845a79351f215b89429b7f2ccef84517f2e63e6d6c33`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Tue, 19 Mar 2024 04:18:07 GMT
ENV _BASH_COMMIT=b1e7f68032bd90dec1a2968a616b32a469929c78
# Tue, 19 Mar 2024 04:18:07 GMT
ENV _BASH_VERSION=devel-20240318
# Tue, 19 Mar 2024 04:18:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 19 Mar 2024 04:18:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Mar 2024 04:18:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Mar 2024 04:18:07 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9afa0290ad1a0756facda314671bd5e850e7dcd33bc84892424b0e4acaf327a`  
		Last Modified: Tue, 19 Mar 2024 21:56:31 GMT  
		Size: 2.8 MB (2824889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5b971c1c9235e2d6e3a594da62e842540354de09f613e09211133e9a1d3eab5`  
		Last Modified: Tue, 19 Mar 2024 21:56:30 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.19` - unknown; unknown

```console
$ docker pull bash@sha256:679418f4903922da04f6bee1fc7428bd9b76b59a2e31dc6b729e88498ab534d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 KB (15981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37c15046eb2e091a6485114f399bf39648f58fff1d812676ae317b03f55df648`

```dockerfile
```

-	Layers:
	-	`sha256:696387f64933a61659d85e7aa8dec2ec13eb05878e468bbdcdee80bb9ef23db3`  
		Last Modified: Tue, 19 Mar 2024 21:56:30 GMT  
		Size: 16.0 KB (15981 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.19` - linux; arm variant v7

```console
$ docker pull bash@sha256:3d6a0ca5c753a1a275c3cead0cceb4445dc330a78470ae80389d02d6217862bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5690016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9491ef43d1ee7a843e4b197793093b3b694e027c0af39cce2a62a365d1f57d7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Tue, 19 Mar 2024 04:18:07 GMT
ENV _BASH_COMMIT=b1e7f68032bd90dec1a2968a616b32a469929c78
# Tue, 19 Mar 2024 04:18:07 GMT
ENV _BASH_VERSION=devel-20240318
# Tue, 19 Mar 2024 04:18:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 19 Mar 2024 04:18:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Mar 2024 04:18:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Mar 2024 04:18:07 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b49d4bc890b96e158a85b08a8dc42e9ec3943527ba67085e81abd85295bc3bb`  
		Last Modified: Tue, 19 Mar 2024 20:01:20 GMT  
		Size: 2.8 MB (2770780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d4535ffbe4bccdc80764b07d80f6f6b919dce1a8ca84563c6d693f45591198c`  
		Last Modified: Tue, 19 Mar 2024 20:01:20 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.19` - unknown; unknown

```console
$ docker pull bash@sha256:ece9a7f0d3110ffab38b138ba3e3069d46ee06f97ab8733353f3f0dfaad17419
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.7 KB (126690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:429dd2c5777a978e40d504f67706b43f021ea8401224890b944396a761961110`

```dockerfile
```

-	Layers:
	-	`sha256:fd23702526c7a692dc0186425d938a722f803a6221b657c84037dadd77cfafdb`  
		Last Modified: Tue, 19 Mar 2024 20:01:20 GMT  
		Size: 110.5 KB (110494 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18ba1c6512681c5c4bf0dbe3dfc42cff33e332d6e2e1117347c5e5b7c6f8120f`  
		Last Modified: Tue, 19 Mar 2024 20:01:20 GMT  
		Size: 16.2 KB (16196 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull bash@sha256:bd0e2fb0130840f8e936873da92599b2bff3df484828a36b8f9ddba184f3bebf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6324792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d610dd16d64cd3d3e6a09e39336a8577b343bf7b61fbca8da50a3dec9af51904`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Tue, 19 Mar 2024 04:18:07 GMT
ENV _BASH_COMMIT=b1e7f68032bd90dec1a2968a616b32a469929c78
# Tue, 19 Mar 2024 04:18:07 GMT
ENV _BASH_VERSION=devel-20240318
# Tue, 19 Mar 2024 04:18:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 19 Mar 2024 04:18:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Mar 2024 04:18:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Mar 2024 04:18:07 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7273cf500df369f6730f88f157d58c4bab0d8156558d29a7a1a45b4609d36d25`  
		Last Modified: Tue, 19 Mar 2024 19:51:03 GMT  
		Size: 3.0 MB (2976745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a860264da4b1a2cd6ac7e379afa69032be4e6c30324247ef909d128366d06c15`  
		Last Modified: Tue, 19 Mar 2024 19:51:03 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.19` - unknown; unknown

```console
$ docker pull bash@sha256:10ff3ca4a2e6344895ba70205e0e090d4e7c159eba17d58c09f36c361365c6b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.6 KB (126605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81daade06e1ffa1c659d686e601992f397ea307d37109cf287ea0962d3cbc404`

```dockerfile
```

-	Layers:
	-	`sha256:a6ba0974e373b7d2458641d18de6eb5fadc9aee1943a4507e73a3bae64f67aea`  
		Last Modified: Tue, 19 Mar 2024 19:51:02 GMT  
		Size: 110.5 KB (110469 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:baec501a175d4ec0222da3bbf8b2da5a6ee01d94e34dd13b58b1b163282d146e`  
		Last Modified: Tue, 19 Mar 2024 19:51:02 GMT  
		Size: 16.1 KB (16136 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.19` - linux; 386

```console
$ docker pull bash@sha256:53f375f2ffbacaa99e2b2aac1c589cc57847b987b516f782ed1ae49d7806f0f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6059343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:004807d74e56257d2e72330e67b6a3d66ba0e4d5bfb06fd7273324e6cd195872`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:19 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Sat, 27 Jan 2024 00:38:19 GMT
CMD ["/bin/sh"]
# Tue, 26 Mar 2024 04:18:04 GMT
ENV _BASH_COMMIT=8af5a8e0ca7d75f91eac7d81783af7d06d32dd50
# Tue, 26 Mar 2024 04:18:04 GMT
ENV _BASH_VERSION=devel-20240325
# Tue, 26 Mar 2024 04:18:04 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 26 Mar 2024 04:18:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 04:18:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Mar 2024 04:18:04 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41ea3af591a0106a70488865f5a8adfbcab5932d4aaf45dfdfbd673d8894df8d`  
		Last Modified: Tue, 26 Mar 2024 18:50:12 GMT  
		Size: 2.8 MB (2814923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:468d494ee13cf322fe86f8d66c4aa9943ae0e1c0e11d042fb5e66db7a9238bdb`  
		Last Modified: Tue, 26 Mar 2024 18:50:12 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.19` - unknown; unknown

```console
$ docker pull bash@sha256:ea73f858177ee1e4d653b30157737b4495bbdd50e557871da8799cb314676a89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.7 KB (126732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ea70c77b611e31e0b9681342f880b1958da0322068261c3e479a9c54b0d843a`

```dockerfile
```

-	Layers:
	-	`sha256:8c5e64559f382be8256b2de8e79b4c04e241cb2f4044713156dcff0c5978f97f`  
		Last Modified: Tue, 26 Mar 2024 18:50:12 GMT  
		Size: 110.4 KB (110433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76a6621cac86574a7e304a01a708cb34a9436163ecf98788d1f6ea3de02b8d6d`  
		Last Modified: Tue, 26 Mar 2024 18:50:12 GMT  
		Size: 16.3 KB (16299 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.19` - linux; ppc64le

```console
$ docker pull bash@sha256:701b84974511b5742021f1336356bacbc49f9eaa1b53cfb5e9880f99a31a6c25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6505314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6d99d3cd94d3a5391f3606605f029d4b5b8f205e4b445a55fc6efe75f03f8a8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Tue, 26 Mar 2024 04:18:04 GMT
ENV _BASH_COMMIT=8af5a8e0ca7d75f91eac7d81783af7d06d32dd50
# Tue, 26 Mar 2024 04:18:04 GMT
ENV _BASH_VERSION=devel-20240325
# Tue, 26 Mar 2024 04:18:04 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 26 Mar 2024 04:18:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 04:18:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Mar 2024 04:18:04 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffcd7d96b623f656262aa8f52dd4ca800f993c6a413e897541d16a88165e16fc`  
		Last Modified: Tue, 26 Mar 2024 19:11:19 GMT  
		Size: 3.1 MB (3146623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d941ec862f1a0fa6521653af7a5e8f4f8b70dbf3719b568a0aa8d22322d87f4`  
		Last Modified: Tue, 26 Mar 2024 19:11:18 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.19` - unknown; unknown

```console
$ docker pull bash@sha256:d65750ff54a171e86510739538c0c70598bfbde8fa8bf650b635343be1d464f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.7 KB (124738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d37f8405fc2cc65d4bcae00514e110559a6adb1d4d98b05e456a9832cb44844`

```dockerfile
```

-	Layers:
	-	`sha256:77bcf3b24eac76b0821ba68a71a68c795254400f783f4a4f0f58cc2a887f64df`  
		Last Modified: Tue, 26 Mar 2024 19:11:18 GMT  
		Size: 108.5 KB (108538 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20f778562652fc4d9ae41f9db3c22298cd79e38a27e9724d3b7f41509c0e4bac`  
		Last Modified: Tue, 26 Mar 2024 19:11:18 GMT  
		Size: 16.2 KB (16200 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.19` - linux; s390x

```console
$ docker pull bash@sha256:84dd7fbb7681123028b361c3a9ad8e7991425a3ee7634855505ac47662bea2f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6219133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21601403be297b7e308f86336a84456b3254ad41cb0bc3b6fb7f0bc0ae97833c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Tue, 26 Mar 2024 04:18:04 GMT
ENV _BASH_COMMIT=8af5a8e0ca7d75f91eac7d81783af7d06d32dd50
# Tue, 26 Mar 2024 04:18:04 GMT
ENV _BASH_VERSION=devel-20240325
# Tue, 26 Mar 2024 04:18:04 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 26 Mar 2024 04:18:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 04:18:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Mar 2024 04:18:04 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:751a0ea80b7df51c44df3246e49e388d1bf855bb46145a4a7cbd70d2d42669bc`  
		Last Modified: Tue, 26 Mar 2024 18:55:43 GMT  
		Size: 3.0 MB (2976164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20bdb7c4c1906246f886c1666c44ff2aa7179c992f65e6af39078acb9e915568`  
		Last Modified: Tue, 26 Mar 2024 18:55:43 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.19` - unknown; unknown

```console
$ docker pull bash@sha256:04c4290087fa89a9bd93befcfa26272559b8d79618399690828e42356e923826
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.7 KB (124666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afb24eccc8c5ff751cb062b1276d4badfb9a5ba76920b207e94e566513c0bf6c`

```dockerfile
```

-	Layers:
	-	`sha256:fd9332a01fe6f73e89f4db8c2adb52abff2ca48170d055ce56a9b2a5909012a6`  
		Last Modified: Tue, 26 Mar 2024 18:55:43 GMT  
		Size: 108.5 KB (108504 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9041d31a6ee4c1e766aa52dcbb919633a496152f9c47acaa634ac8bee3e1f3ec`  
		Last Modified: Tue, 26 Mar 2024 18:55:43 GMT  
		Size: 16.2 KB (16162 bytes)  
		MIME: application/vnd.in-toto+json
