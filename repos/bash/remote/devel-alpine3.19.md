## `bash:devel-alpine3.19`

```console
$ docker pull bash@sha256:d9e9f26804f60d4dce9cd33d3f511546fac3e8d36c2bfc80a78f250ce67a52f1
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
$ docker pull bash@sha256:ad564826fa03a5471a2da0bcd858cd8f0993eac1837c832e2bc427dcbe38e3a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6283588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4130dc748e6f4a2fcc506214ce87bef300de7824b868b6d653130a3e7d684214`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
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
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dece1b89b24a5d6442e83cba79f88598552fb597ddbb8f1d0e3b65ce66fcbe45`  
		Last Modified: Tue, 19 Mar 2024 19:49:24 GMT  
		Size: 2.9 MB (2874529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a1fd13ebc35f5b4ab5d3a238316dd701899dffdbc3320521e084dd8115520e2`  
		Last Modified: Tue, 19 Mar 2024 19:49:24 GMT  
		Size: 330.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.19` - unknown; unknown

```console
$ docker pull bash@sha256:230ab376fbc709513c95c53d90eab9391309b13087bbd4d07362d5b517bb786a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.8 KB (126750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae0c84f035d91e40767b63734925db5a721d0f8738b7535b1649bb6a72234531`

```dockerfile
```

-	Layers:
	-	`sha256:e23b2d2ff0fc681b4a70820a1ebba34f4cef2e15916b3bef7faae926e0008da3`  
		Last Modified: Tue, 19 Mar 2024 19:49:24 GMT  
		Size: 110.5 KB (110458 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d7493373017513027e87be32f3b0a7eca86fa440435fe152142337ad2286fd0`  
		Last Modified: Tue, 19 Mar 2024 19:49:24 GMT  
		Size: 16.3 KB (16292 bytes)  
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
$ docker pull bash@sha256:36e0fa0d552d9c535c56a484425c73362a84c6bf629e74bc08c6e5d614d3fd80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6059568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb634caf93f0a43a6362f0bf433a918d48aa494e39c383af4c372a97eee62e97`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:19 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Sat, 27 Jan 2024 00:38:19 GMT
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
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f900838e43884f765183afbe3f7ddd05734fbde997e3e7010de4a766b8fd33a`  
		Last Modified: Tue, 19 Mar 2024 19:49:24 GMT  
		Size: 2.8 MB (2815141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a09435a30247a8988ad7e7dd3565a70db03bc2879b052bc4f678464d51d05272`  
		Last Modified: Tue, 19 Mar 2024 19:49:23 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.19` - unknown; unknown

```console
$ docker pull bash@sha256:5a432d4bdef52d909be99b2b648fd19048f3e8610462fc3705ec09195253f7cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.7 KB (126696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f880469d28c114dd554fc156407d454c0e533ec2a602f0d72675a2f98de0808b`

```dockerfile
```

-	Layers:
	-	`sha256:e1cb433bdcb4fbcd4654ebcd0b038d25e8924c4b3d31cd0839a07c1929ca37e6`  
		Last Modified: Tue, 19 Mar 2024 19:49:24 GMT  
		Size: 110.4 KB (110433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f345a3b81b34206f7d56792712e7c2f19db7665b7fdf73c6784770709ff25c6`  
		Last Modified: Tue, 19 Mar 2024 19:49:23 GMT  
		Size: 16.3 KB (16263 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.19` - linux; ppc64le

```console
$ docker pull bash@sha256:35f2250cb2eefced8b267ef6f8eba08d4b9caa12f4d26610666138f3b83dad7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6504887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f2e860eb172042a28c49da602ed7f193e75f388a3990da2d063f04f6f04c7b0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
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
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9945a5652eeca6ba00d962cef3402d2c0a2deaeeeb2d9f497c1cf3e17dc27fa`  
		Last Modified: Tue, 19 Mar 2024 20:26:17 GMT  
		Size: 3.1 MB (3146197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d53b0ee58ea7d6e1141712e683f3403c546c5d40d7791ac5f61bba31292d91b`  
		Last Modified: Tue, 19 Mar 2024 20:26:16 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.19` - unknown; unknown

```console
$ docker pull bash@sha256:036c2555737b14f3d3f147563774241a42b2be4359724fbb57e4e373d5cdcae9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.7 KB (124702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87e7a7a786574424c4ef322b466104f2c07070890a96190324ab36de43a6add0`

```dockerfile
```

-	Layers:
	-	`sha256:73678dc453ff9a3a4cdf717ecd4bf74837136d5c88db3fb1b2b0f1e2fea9e07a`  
		Last Modified: Tue, 19 Mar 2024 20:26:16 GMT  
		Size: 108.5 KB (108538 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:902d0f7913353408b6cea6e3f95036c555f158442e5bbcb88b103c1ef107e990`  
		Last Modified: Tue, 19 Mar 2024 20:26:16 GMT  
		Size: 16.2 KB (16164 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.19` - linux; s390x

```console
$ docker pull bash@sha256:d39a3bd235c88344612d1a9199cd128967e2603ec7352610be9bb4ea5b7fa7d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6218312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18c4ee2fb60dd69c6cf8b2954d0f8de5669f19d0b1ce92a440f2628b2588a1f3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
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
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ef4370c9b1f86ddefa6f7cd38bf34434e5aecaa184270ffa54de75a6f43f812`  
		Last Modified: Tue, 19 Mar 2024 20:05:10 GMT  
		Size: 3.0 MB (2975346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:451d46e622d1244c57d19e3101233ac2e622aae94cf2dded0611a9d064f4ba69`  
		Last Modified: Tue, 19 Mar 2024 20:05:10 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.19` - unknown; unknown

```console
$ docker pull bash@sha256:1829168b8ba738346756de73642bdbe21acb8307876c214a2477f1131907c088
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.6 KB (124629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53c5bbde443fd4139894bcd3909ee3a5caba1c718c5afc14021e55aba34ba067`

```dockerfile
```

-	Layers:
	-	`sha256:dfe874043d7a6e46746e400ece7e555ed9173dc525e773eab522f5e347bd863c`  
		Last Modified: Tue, 19 Mar 2024 20:05:10 GMT  
		Size: 108.5 KB (108504 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:176437c4f6451be7fa5480eae90bef12dee466195f2e673a86bc5b750f2c3bf3`  
		Last Modified: Tue, 19 Mar 2024 20:05:11 GMT  
		Size: 16.1 KB (16125 bytes)  
		MIME: application/vnd.in-toto+json
