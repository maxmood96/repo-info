## `bash:devel`

```console
$ docker pull bash@sha256:648881fb4d60d005783289f8f3db574ea1f1f9a0f3283cc7f54330e4a77532fe
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
$ docker pull bash@sha256:1bb98aff6460eaffad5b9a5fd74a30f97d5142f8f2f2968572970f1d024ab428
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6524114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea2e74e2e08c6ce23eb1334f2e965cdd8ef98c207a24193bb69fe145cef9c9bb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:43 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Mon, 22 Jul 2024 22:26:43 GMT
CMD ["/bin/sh"]
# Tue, 23 Jul 2024 04:18:11 GMT
ENV _BASH_COMMIT=6c703092759ace29263ea96374e18412c59acc7f
# Tue, 23 Jul 2024 04:18:11 GMT
ENV _BASH_VERSION=devel-20240718
# Tue, 23 Jul 2024 04:18:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 23 Jul 2024 04:18:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 23 Jul 2024 04:18:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Jul 2024 04:18:11 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f127ade244c2a43594a076a4c397384e1aeedb6bb60294b87c62a4480cdbdbe`  
		Last Modified: Wed, 24 Jul 2024 01:09:30 GMT  
		Size: 2.9 MB (2900893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:694f343e252d1f5154743de9f00a01945ca53935cf75bb351b810c6ecfce9d70`  
		Last Modified: Wed, 24 Jul 2024 01:09:29 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:f733954d72be78e0a412c82376e3fecc624c71d56f895f29cdee4f9704e8eef9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.0 KB (126050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eef4438141ec9ecc9171942fdcf38a4a019163a759b461fbd6071e9d8b01527a`

```dockerfile
```

-	Layers:
	-	`sha256:ed977c12e3a9b5c61f8ef55072e402bc23dda8792acefaf0c736b83e916fa9e6`  
		Last Modified: Wed, 24 Jul 2024 01:09:29 GMT  
		Size: 109.9 KB (109883 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8b39f7c907b3e029bd01f2ea3b14ad3ff91fe04763b57122bbaf558ce020f26`  
		Last Modified: Wed, 24 Jul 2024 01:09:29 GMT  
		Size: 16.2 KB (16167 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; arm variant v6

```console
$ docker pull bash@sha256:674ff40bf6e62434801fa9319e14de398325a3841f3135aa0bf227ea67defd20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6216232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0371522912b9866d217e4dc8658f6095fa74c302b1e83e4e78ffba6812b7f10b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 22 Jul 2024 21:49:18 GMT
ADD file:85f927c1895bee1d0b095b2905c8d47ada8773f13e03fd4a201f718103ef7958 in / 
# Mon, 22 Jul 2024 21:49:19 GMT
CMD ["/bin/sh"]
# Tue, 23 Jul 2024 04:18:11 GMT
ENV _BASH_COMMIT=6c703092759ace29263ea96374e18412c59acc7f
# Tue, 23 Jul 2024 04:18:11 GMT
ENV _BASH_VERSION=devel-20240718
# Tue, 23 Jul 2024 04:18:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 23 Jul 2024 04:18:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 23 Jul 2024 04:18:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Jul 2024 04:18:11 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:ae2458422e4465e718700cd0c5970c709804ded4caa7b7f317eada5d16878e29`  
		Last Modified: Mon, 22 Jul 2024 21:49:42 GMT  
		Size: 3.4 MB (3365189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cd6dd0529423fed9d69536ce127c961acf71d851435a8676294bb3aecee7140`  
		Last Modified: Wed, 24 Jul 2024 01:09:19 GMT  
		Size: 2.9 MB (2850712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc7be86a073a09911a708b9c0f415456e29c367b545582b5479d1dd3f9d38d32`  
		Last Modified: Wed, 24 Jul 2024 01:09:19 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:66b84ddf5b4d5f615150c02aa1ba4cece24b6abd86d31cc80b8b786d95b0a616
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 KB (16018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcd37fbfaa2eb7a67fa1535474cc8f81d44b5977661b0ec2f51e8bd94b084e70`

```dockerfile
```

-	Layers:
	-	`sha256:03e7d36141a11bc69e5b44969b0afec07410973ed91919962ce9b5d46311a6fe`  
		Last Modified: Wed, 24 Jul 2024 01:09:19 GMT  
		Size: 16.0 KB (16018 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; arm variant v7

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

### `bash:devel` - unknown; unknown

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

### `bash:devel` - linux; arm64 variant v8

```console
$ docker pull bash@sha256:02be8145b51d8c5ec26ab2376e047eb5055d5959bb8b72ed7e127f9ab44e6b11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7089001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:805cb3b089c3ae84187ffe2d87d6c1c24aa0baf07247ce89ab76d11a5125ffbc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:13 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 22 Jul 2024 21:44:13 GMT
CMD ["/bin/sh"]
# Tue, 23 Jul 2024 04:18:11 GMT
ENV _BASH_COMMIT=6c703092759ace29263ea96374e18412c59acc7f
# Tue, 23 Jul 2024 04:18:11 GMT
ENV _BASH_VERSION=devel-20240718
# Tue, 23 Jul 2024 04:18:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 23 Jul 2024 04:18:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 23 Jul 2024 04:18:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Jul 2024 04:18:11 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec2338bfa0aa6d47ca61317280e58e7f70d445a151589980c745068cdfa78fbc`  
		Last Modified: Wed, 24 Jul 2024 11:20:48 GMT  
		Size: 3.0 MB (3001736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0d8e786a79b6d47253526279eb3155c476a043109e7d734c2abf340a181ea9e`  
		Last Modified: Wed, 24 Jul 2024 11:20:47 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:7dccf5dc8dce6a62f87b25c59453f4778b8c266cf6e737f6fc9fe2374001809f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.4 KB (126406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc8073c93f10018e921d9600d308739b6d12abb2dd9e7bfdd1f4f68975dff02e`

```dockerfile
```

-	Layers:
	-	`sha256:d014d1352c5bd2b180778394e2f68f46bc888a4ce7574be73d4d04eb0f3f0d54`  
		Last Modified: Wed, 24 Jul 2024 11:20:48 GMT  
		Size: 109.9 KB (109939 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7104d35212939f595ed9f3f80dc7b49d6cd0e651a3c56d147af237d2feb66fe8`  
		Last Modified: Wed, 24 Jul 2024 11:20:47 GMT  
		Size: 16.5 KB (16467 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; 386

```console
$ docker pull bash@sha256:ce6e987221157622322b47710df8ef53dc87121e2da617dbf3283275d3d6e1ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6312466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e99ec4d90a91b8cee1688ed9b55331c4353279af786d792c4b1c2a9d57e9d7b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 22 Jul 2024 21:38:29 GMT
ADD file:e5b77b9337c5f89df9a65f8c439736a6d79e68274100ab1a1d7d61359a9abf5d in / 
# Mon, 22 Jul 2024 21:38:30 GMT
CMD ["/bin/sh"]
# Tue, 23 Jul 2024 04:18:11 GMT
ENV _BASH_COMMIT=6c703092759ace29263ea96374e18412c59acc7f
# Tue, 23 Jul 2024 04:18:11 GMT
ENV _BASH_VERSION=devel-20240718
# Tue, 23 Jul 2024 04:18:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 23 Jul 2024 04:18:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 23 Jul 2024 04:18:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Jul 2024 04:18:11 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:2585500d54afa42a6b579f9ed6f62b49c5fb21c2653f79194342804bde8770fe`  
		Last Modified: Mon, 22 Jul 2024 21:38:55 GMT  
		Size: 3.5 MB (3468071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:718d37441c7b37743e1b081a5501106bca443f3bbc8ffd96ee407a0d010d6b6a`  
		Last Modified: Wed, 24 Jul 2024 01:09:34 GMT  
		Size: 2.8 MB (2844058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eb5b13c009783df42a82319089a707f1117bf36f25aef151a596ad14627b8f3`  
		Last Modified: Wed, 24 Jul 2024 01:09:34 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:eba98cb51ad42bfeabfe9ff68ec7305e424b60f3110a8df511a67c97623b1462
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.0 KB (125996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:432dc472b0b2df3ec47e9274ae8b152862208ccfe1d6d0115d8c73d9acacab05`

```dockerfile
```

-	Layers:
	-	`sha256:0882da2d48134c9a7c94cf898c73fac8551769d63b4f70483cab7cd6968d2a61`  
		Last Modified: Wed, 24 Jul 2024 01:09:34 GMT  
		Size: 109.9 KB (109858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5c4f2b995251a52c1e946099859c9e5a187a53b4f6070094d622825489ec1f8`  
		Last Modified: Wed, 24 Jul 2024 01:09:34 GMT  
		Size: 16.1 KB (16138 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; ppc64le

```console
$ docker pull bash@sha256:f709952df2ee313e6b868b6e6d68952448bf414b4f4e90ad62129f0ee6fd1d5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6745644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36ba870a3b21869df668779ea82418bed10ce333392ff09c8ab45fb632fe7753`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 22 Jul 2024 21:26:21 GMT
ADD file:9fcad21b83b7efd6ef267ba714c3ef5a8d4d2064a0bdf528cbb17d0c3388f03f in / 
# Mon, 22 Jul 2024 21:26:22 GMT
CMD ["/bin/sh"]
# Tue, 23 Jul 2024 04:18:11 GMT
ENV _BASH_COMMIT=6c703092759ace29263ea96374e18412c59acc7f
# Tue, 23 Jul 2024 04:18:11 GMT
ENV _BASH_VERSION=devel-20240718
# Tue, 23 Jul 2024 04:18:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 23 Jul 2024 04:18:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 23 Jul 2024 04:18:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Jul 2024 04:18:11 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:6e59b4988c495782a5b0c8f8d6698931851c16c5c0fc5ef09cbb0637ade56e36`  
		Last Modified: Mon, 22 Jul 2024 21:26:52 GMT  
		Size: 3.6 MB (3571555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:543cf3cc9e64bc2ddb6f2a5b7d053631386ccd0a00827736b6b9ed711774ab25`  
		Last Modified: Wed, 24 Jul 2024 12:37:25 GMT  
		Size: 3.2 MB (3173752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6e937155d14e73be01c8e52d90079de6ebe34efb480fdada12b2d021fcffa6a`  
		Last Modified: Wed, 24 Jul 2024 12:37:25 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:3cf021fcf3e5ca5f83198560beaabc0409948eec49651f94469fb3c23cda2f61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.2 KB (124167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29a57f5261ec29adaadf2ad78a01479d3fbe5643fecac1ab1178e66594bdfae1`

```dockerfile
```

-	Layers:
	-	`sha256:4c13c607deb8311f27411d1803752b08b879e28f8120209455429488446fd504`  
		Last Modified: Wed, 24 Jul 2024 12:37:25 GMT  
		Size: 108.0 KB (107963 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:953425314ae5266bfa62a9a9a2ccce498de0285f9332d78628097338ee5a8bab`  
		Last Modified: Wed, 24 Jul 2024 12:37:25 GMT  
		Size: 16.2 KB (16204 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; riscv64

```console
$ docker pull bash@sha256:76818a59ccc7dd2bb339b084e5fef873822120347fd19b848defae0f8da0617d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6223274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e676ffffb7172a57a60aac2e9fc6d77e5cae0a33d85b5307f5c86a3dbab4bbf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 22 Jul 2024 22:21:00 GMT
ADD file:cdf7088bbd70519f0f5d7b4249df34386e40f0194752f45842b3d85f2d331cf5 in / 
# Mon, 22 Jul 2024 22:21:00 GMT
CMD ["/bin/sh"]
# Tue, 23 Jul 2024 04:18:11 GMT
ENV _BASH_COMMIT=6c703092759ace29263ea96374e18412c59acc7f
# Tue, 23 Jul 2024 04:18:11 GMT
ENV _BASH_VERSION=devel-20240718
# Tue, 23 Jul 2024 04:18:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 23 Jul 2024 04:18:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 23 Jul 2024 04:18:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Jul 2024 04:18:11 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:faf447acae27573624c0613a79c4bcf1f9bc46d29f523140352abfd3f7691282`  
		Last Modified: Mon, 22 Jul 2024 22:21:18 GMT  
		Size: 3.4 MB (3370673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9d3e76237150d4f5216d45fb4a0b6516c6b041bfde8c362a32b66b88a188568`  
		Last Modified: Wed, 24 Jul 2024 11:51:53 GMT  
		Size: 2.9 MB (2852262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:822f9cfab0d8442f6352e69de377b890a7444058aa54c6897bdd297bffd03199`  
		Last Modified: Wed, 24 Jul 2024 11:51:52 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:3de111e5c896ab1f6eacd157851bfede9bc5c1efb5e7324e82264e6f7ad8d92d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.2 KB (124164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7235cd85b9648e7c57d004e39916b675166323e3fef87ac13bcbbcbbfccf332b`

```dockerfile
```

-	Layers:
	-	`sha256:4485aaefc6c82255d4c725e2136fb090aa3a09895ccee0056d4f5ff184cf147c`  
		Last Modified: Wed, 24 Jul 2024 11:51:53 GMT  
		Size: 108.0 KB (107959 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c29d1cf242b8f2efe0781c773d85788915cb96e7b2b4c2c60ef2bbb832ec14e5`  
		Last Modified: Wed, 24 Jul 2024 11:51:52 GMT  
		Size: 16.2 KB (16205 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; s390x

```console
$ docker pull bash@sha256:8f53c3f1f0b16a282235e448fa09054b58768e493ea02f3ab45e4359a4cdc450
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6462939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b126c15421fa7ec290c3a785118682108a4a0a9220ae5bee7d3f91f8e15bdd8f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 22 Jul 2024 21:50:06 GMT
ADD file:63d382fb7a431c57868274a368a659bde32a60ae0cd05c8af34c3d6a57066a77 in / 
# Mon, 22 Jul 2024 21:50:07 GMT
CMD ["/bin/sh"]
# Tue, 23 Jul 2024 04:18:11 GMT
ENV _BASH_COMMIT=6c703092759ace29263ea96374e18412c59acc7f
# Tue, 23 Jul 2024 04:18:11 GMT
ENV _BASH_VERSION=devel-20240718
# Tue, 23 Jul 2024 04:18:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 23 Jul 2024 04:18:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 23 Jul 2024 04:18:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Jul 2024 04:18:11 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:834c666d55eae0e308600077be061a01680e7cd02b579be887d9469075f0d943`  
		Last Modified: Mon, 22 Jul 2024 21:51:06 GMT  
		Size: 3.5 MB (3461066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90fb82b67bc11e24c5127c0984f1c33b6cb94828f0ca9a6c07e3e2f96228943c`  
		Last Modified: Wed, 24 Jul 2024 12:05:38 GMT  
		Size: 3.0 MB (3001537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a60fe2b0e8128f9487b67c444fd4b2d1ae1ad6e2f98600026943301d2132383`  
		Last Modified: Wed, 24 Jul 2024 12:05:38 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:8c6c5eb103509fb7b56b4376c728d62d9d2845ef1e2abc1d024e392ece1261ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.1 KB (124096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e476f143026a56a1cf2e45e1f99a48befa8b5cf1eb21b80f674e8952bef5e70f`

```dockerfile
```

-	Layers:
	-	`sha256:5677f1df3c23d3b3ed1839ce6f30ce439f467597a01876a465a2f79c22531a00`  
		Last Modified: Wed, 24 Jul 2024 12:05:38 GMT  
		Size: 107.9 KB (107929 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36bb147ed70570818b35ddaba9c235dbf7fe64b4a7d9089a943880a982f24bda`  
		Last Modified: Wed, 24 Jul 2024 12:05:38 GMT  
		Size: 16.2 KB (16167 bytes)  
		MIME: application/vnd.in-toto+json
