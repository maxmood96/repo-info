## `bash:devel`

```console
$ docker pull bash@sha256:634efff36ecfb1d9fe82fc078363823455c2c3ba87b2ddf7991c247bf91072ef
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
$ docker pull bash@sha256:8844d932521cf4b8d8d3032657acee96b59be854ba72dcf6bd1469b42000fc60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6887509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:991246846ca8a47aabeb65760f2e3460f6d97e43aa5fefb00b255cdab9cb8d6a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Tue, 03 Feb 2026 17:23:55 GMT
ENV _BASH_COMMIT=468e98e574c182a4c5cee6ae63eb124907bfce16
# Tue, 03 Feb 2026 17:23:55 GMT
ENV _BASH_VERSION=devel-20260130
# Tue, 03 Feb 2026 17:23:55 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 03 Feb 2026 17:24:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 03 Feb 2026 17:24:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 17:24:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 17:24:32 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e71805ca7033091ee25973fe518b23408d16a80a87386e1ede807616c889e3ce`  
		Last Modified: Tue, 03 Feb 2026 17:24:37 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b705b01cf4b40ae3e5583fd56f78a52ff0be9660e3692813be1e8691db0cfec1`  
		Last Modified: Tue, 03 Feb 2026 17:24:37 GMT  
		Size: 3.0 MB (3024896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a281729992c63ecf36254df18d1cd2000dbcad7644f3031c6f2624500b3d009`  
		Last Modified: Tue, 03 Feb 2026 17:24:37 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:47623162382a8fb21bc2a5b84777875895b708f3c8af7cdc42d9df05479df25e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.2 KB (135198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fdb94193d9085350ef7948578ca5e6cdfe333a1d0f7bf14a14f4e0648f999ab`

```dockerfile
```

-	Layers:
	-	`sha256:ff26a4a5f378a6148dccb79444dc850ebf27c34f50109b8eaf409c5d85f6195a`  
		Last Modified: Tue, 03 Feb 2026 17:24:37 GMT  
		Size: 117.1 KB (117122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8610cf779aae716878c7aa3639a99209aecacf06549bdb2af0fcf3803d184201`  
		Last Modified: Tue, 03 Feb 2026 17:24:37 GMT  
		Size: 18.1 KB (18076 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; arm variant v6

```console
$ docker pull bash@sha256:b4bb9d50b44eb6acc372b71d2fca0a9c7fcdc9bc9b1c4370fa19788ef071a000
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6553529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02543c45e3edcab3e2a7eb6dfd265d3bc34a1e717b4436ffa7505f2954857df4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Tue, 03 Feb 2026 17:23:51 GMT
ENV _BASH_COMMIT=468e98e574c182a4c5cee6ae63eb124907bfce16
# Tue, 03 Feb 2026 17:23:51 GMT
ENV _BASH_VERSION=devel-20260130
# Tue, 03 Feb 2026 17:23:51 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 03 Feb 2026 17:24:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 03 Feb 2026 17:24:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 17:24:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 17:24:36 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42ddeef74b26c6e9f936435e68803bdbb10d28c37f67a1d28c42b7da02e5e00c`  
		Last Modified: Tue, 03 Feb 2026 17:24:40 GMT  
		Size: 458.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9ee7272f34696df6a77f7ccad999ebabfda4da7946f0d207e0db146bf6ba3d8`  
		Last Modified: Tue, 03 Feb 2026 17:24:40 GMT  
		Size: 3.0 MB (2982913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f47900827081a16a473322c0af97faa1d5a3e4b41ddde0fbc22bec735c9af877`  
		Last Modified: Tue, 03 Feb 2026 17:24:40 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:b10514c1ad64ba61e90c5e235d3b9d687c1fac357edaae421b47367f4a3d38df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 KB (17941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faec9a47c8e172d417fc36b1ee15efa86b2460e48e6e83c464d768b9cc487e11`

```dockerfile
```

-	Layers:
	-	`sha256:069c54cdcdafe5a2b41fd9b314b8980db856e1be70f749d68d380125f9d6aa83`  
		Last Modified: Tue, 03 Feb 2026 17:24:40 GMT  
		Size: 17.9 KB (17941 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; arm variant v7

```console
$ docker pull bash@sha256:21c1e6879302c11985f2054ae78f2622ec27e362039df27440d4807862678919
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6216137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd1db299a5ca4d7a126929ba60cae8d3c1b2ac01d73447ce6eba170510e552f5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Tue, 03 Feb 2026 17:24:34 GMT
ENV _BASH_COMMIT=468e98e574c182a4c5cee6ae63eb124907bfce16
# Tue, 03 Feb 2026 17:24:34 GMT
ENV _BASH_VERSION=devel-20260130
# Tue, 03 Feb 2026 17:24:34 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 03 Feb 2026 17:25:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 03 Feb 2026 17:25:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 17:25:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 17:25:17 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3f446735aa4fa9f3525357348c1d61b88120292d7cd9e73b2eef10fbcff47ee`  
		Last Modified: Tue, 03 Feb 2026 17:25:22 GMT  
		Size: 458.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa46df6385d1c5cd734bb0045e4711809479acec10f86846c71e00378f8639f2`  
		Last Modified: Tue, 03 Feb 2026 17:25:22 GMT  
		Size: 2.9 MB (2933620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dc01f35896a1efab8e9b5504c08f7af12a5c49bb6292c3065191b87dccd0021`  
		Last Modified: Tue, 03 Feb 2026 17:25:21 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:fd103acfa9b2e9465ecce9d84752dbdac947ab6d3acfa006fc13047dcc3f677a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 KB (134664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aa46fc60475459fc127092b5c8594e1a9b34f80801ad3c76b0f7cc29f5a1e64`

```dockerfile
```

-	Layers:
	-	`sha256:e52ff3c4d706a158f7a7064ab80e5da003cbafc687acc1299209f5ca9fbaa48e`  
		Last Modified: Tue, 03 Feb 2026 17:25:21 GMT  
		Size: 116.5 KB (116508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf48a8450499fbf0194b5ebac19e12299d706a1a60fedd0bbde678a13f2e07ad`  
		Last Modified: Tue, 03 Feb 2026 17:25:21 GMT  
		Size: 18.2 KB (18156 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; arm64 variant v8

```console
$ docker pull bash@sha256:547f3a5c9d532220205eceb22513ed89ba2a98dea6307ebb219216eacc9021a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7293442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4abb9618ee0dac21ebc5c304d7d6a40c6e20dad3bed1ccfdd146e0dbacbaa1c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Tue, 03 Feb 2026 17:23:56 GMT
ENV _BASH_COMMIT=468e98e574c182a4c5cee6ae63eb124907bfce16
# Tue, 03 Feb 2026 17:23:56 GMT
ENV _BASH_VERSION=devel-20260130
# Tue, 03 Feb 2026 17:23:56 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 03 Feb 2026 17:24:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 03 Feb 2026 17:24:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 17:24:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 17:24:36 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73ba1ca9259650bbc78abb4e925d117295c8df928d84e67aa4a3291bc8bc0629`  
		Last Modified: Tue, 03 Feb 2026 17:24:41 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36c44ac054acb571a67326844613b7287ccf26726213e8300cd69666e99e6d63`  
		Last Modified: Tue, 03 Feb 2026 17:24:41 GMT  
		Size: 3.1 MB (3095560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c718efdf68751e25b6dd9c20c11cbce0f0b3b12f424003160914bf2af8ae0616`  
		Last Modified: Tue, 03 Feb 2026 17:24:41 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:b200b51194777ede10e8d55fdac03098ed0d0906ff615fe297c3d4ca71ce2a03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 KB (134708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc5bbaa736cb338929f8e9cf51cca10b78ebc481555c1a556165bd8f77f05d3a`

```dockerfile
```

-	Layers:
	-	`sha256:8d857c6306d1af410a309c57e37b1df2a30f5e2d550f5df17fe57ecbed0c52e9`  
		Last Modified: Tue, 03 Feb 2026 17:24:41 GMT  
		Size: 116.5 KB (116528 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46975edb04a4d5fc7eb1e09655020305c728d62d85ccc36677dc6092cf5a7b81`  
		Last Modified: Tue, 03 Feb 2026 17:24:41 GMT  
		Size: 18.2 KB (18180 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; 386

```console
$ docker pull bash@sha256:b7c6436e4bdf3e78a64992f09bff9d8ec39dab39b854e4f004eb04943f8bf052
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6639284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a3e678e76592a0b2bb16b16618a3a2232d7e3cbd22101b9de79b159fe3b9ee8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:11 GMT
ADD alpine-minirootfs-3.23.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:11 GMT
CMD ["/bin/sh"]
# Tue, 03 Feb 2026 17:24:14 GMT
ENV _BASH_COMMIT=468e98e574c182a4c5cee6ae63eb124907bfce16
# Tue, 03 Feb 2026 17:24:14 GMT
ENV _BASH_VERSION=devel-20260130
# Tue, 03 Feb 2026 17:24:14 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 03 Feb 2026 17:24:51 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 03 Feb 2026 17:24:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 17:24:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 17:24:51 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:18bdec7eea78464ecf9b88f4ec630eaeb694ea1c0101ecd9c20eda20c9065e23`  
		Last Modified: Wed, 28 Jan 2026 01:18:16 GMT  
		Size: 3.7 MB (3686998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5eaf36007b4d876e97b5d1515f1f620e450986b1ae721f11918afd94da558d8`  
		Last Modified: Tue, 03 Feb 2026 17:24:56 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9cb0d9b3a07ccd6312e54a8a2aaa0a4c7d6c58e546c418cb0bb4d3a38ee3f3f`  
		Last Modified: Tue, 03 Feb 2026 17:24:56 GMT  
		Size: 3.0 MB (2951497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f10acadf5920680e47a48f6c9d2905445ca6630eb1779eec644747fdc2a5b132`  
		Last Modified: Tue, 03 Feb 2026 17:24:56 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:25510f588f188cab758fb043837e9dffcb50d8513b616a95cfac92094c9ceeb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.1 KB (135140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11c0672928c9042e1664f87a70e7a63b64976464c039a52ba04a7abc16df1fc3`

```dockerfile
```

-	Layers:
	-	`sha256:f074e77adaee4df453d893e1c03bbedbfd97b479eff80b863315582c0321de22`  
		Last Modified: Tue, 03 Feb 2026 17:24:56 GMT  
		Size: 117.1 KB (117097 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6455afaaf85296dee989b5795cfb6098d7b07f33672c67270605bc1b9b65d49`  
		Last Modified: Tue, 03 Feb 2026 17:24:56 GMT  
		Size: 18.0 KB (18043 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; ppc64le

```console
$ docker pull bash@sha256:2855f3e1bb994864329f58e72628cbb5fbef07fdfca063bb35ca0ad13c2785c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7163110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3d8e65f6f7ffebdb5879f27efce776c9f7502a4c880e8a5c02913acc44a340c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:12:14 GMT
ENV _BASH_COMMIT=b805bbec801b3ac9adf1e67707b2d5bd3da9e60b
# Wed, 28 Jan 2026 02:12:14 GMT
ENV _BASH_VERSION=devel-20260123
# Wed, 28 Jan 2026 02:12:14 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Wed, 28 Jan 2026 18:38:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Wed, 28 Jan 2026 18:38:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 18:38:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 18:38:38 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1df562137f442ce368a20fd090a2aee8c61c51133b0500c9b70a1c208a23adb`  
		Last Modified: Wed, 28 Jan 2026 02:13:20 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edecbd651eb0ff5f4c88718645fb99e80120615f2124090244de172f50da2452`  
		Last Modified: Wed, 28 Jan 2026 18:38:58 GMT  
		Size: 3.3 MB (3332677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24fa1373bab11ecf768c1e91c2a7f85e868e6a480bd96210b0e53fd9c8171a5b`  
		Last Modified: Wed, 28 Jan 2026 18:38:57 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:118b010f75b303899e7ca56d06f805bf5d3b2fe180a182f038cebdc8bf71f6fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 KB (134712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da14b64972818e9f61f78496d5740817b15ee3b4809d0c8cfd344d7ae5a23fd2`

```dockerfile
```

-	Layers:
	-	`sha256:c1a4104628f8d3e1bfdddaeb127fcc319ef0d8fb28ee4ff6adfdf1b0a96dfaf0`  
		Last Modified: Wed, 28 Jan 2026 18:38:57 GMT  
		Size: 116.5 KB (116505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca5d9a95469e10874d0702c7a8252071d4647d462aa309d35fe48c9bb6d4de8d`  
		Last Modified: Wed, 28 Jan 2026 18:38:57 GMT  
		Size: 18.2 KB (18207 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; riscv64

```console
$ docker pull bash@sha256:d7dacb5d2cdfee4b0d75afea0bdc387a9d1c04153d39baee9ec853cbbe16704e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6799309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13491eeecf751f9a55be83350934a298f331001dc2b649eccd431f5e8cab44ff`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 04:17:11 GMT
ENV _BASH_COMMIT=b805bbec801b3ac9adf1e67707b2d5bd3da9e60b
# Wed, 28 Jan 2026 04:17:11 GMT
ENV _BASH_VERSION=devel-20260123
# Wed, 28 Jan 2026 04:17:11 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Fri, 30 Jan 2026 18:17:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Fri, 30 Jan 2026 18:17:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 30 Jan 2026 18:17:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 30 Jan 2026 18:17:40 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0540f5e7cbbd06be9591105e336b004c6e351dc53f24f7df485f56578662b1b4`  
		Last Modified: Wed, 28 Jan 2026 04:26:38 GMT  
		Size: 460.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7ffaae1805215a6b3be4f6119f35888f3344b419b7f3af56e69625446a86949`  
		Last Modified: Fri, 30 Jan 2026 18:18:12 GMT  
		Size: 3.2 MB (3213221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71bb27a8c065c4964a468af5094d7107bb2569d2c2c9f867432ca01ad1f59ba2`  
		Last Modified: Fri, 30 Jan 2026 18:18:11 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:3002e373749aad7fd6bc59977e729bf9ebdd3e2b00aa501467ccdcdaccbcb18e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 KB (134708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ba41d4db8eb24404bfd8677be3f41efeb6d411881cad65bb4bfd2035a7d578c`

```dockerfile
```

-	Layers:
	-	`sha256:8195a4e4c17ad0bce5c770eb3fa87599546367c9fd5ef7add1a8f1de658e4e0f`  
		Last Modified: Fri, 30 Jan 2026 18:18:11 GMT  
		Size: 116.5 KB (116501 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:563154a110355103f295bdfdf1349f86bbb12483e658dce469eeef2f99cfb201`  
		Last Modified: Fri, 30 Jan 2026 18:18:11 GMT  
		Size: 18.2 KB (18207 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; s390x

```console
$ docker pull bash@sha256:ab5b76ca1e6e3187ac738222d70b2e3632d688198352aa8c3e1fb5e410e01cca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6843176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fd7415da8f43c04f0f15635923d726dc1a980fcd9a597d9ca2daad31b7c3a27`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:12:15 GMT
ENV _BASH_COMMIT=468e98e574c182a4c5cee6ae63eb124907bfce16
# Wed, 28 Jan 2026 02:12:15 GMT
ENV _BASH_VERSION=devel-20260130
# Wed, 28 Jan 2026 02:12:15 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 03 Feb 2026 17:23:56 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 03 Feb 2026 17:23:56 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 17:23:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 17:23:56 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:933f34932483ae323b9c0468361629e1e26fb7403cef6d4353f0f81140eed823`  
		Last Modified: Wed, 28 Jan 2026 02:13:04 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfc68e5be6fdd411a177371e4b6a38153dad28b22225249f0f68bec90ef528ee`  
		Last Modified: Tue, 03 Feb 2026 17:24:05 GMT  
		Size: 3.1 MB (3117056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cec716aee4bb53a42adf2aadbd27340ce20663c83e74334287724e93e297503`  
		Last Modified: Tue, 03 Feb 2026 17:24:05 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:e032f8fe79435a21f392b9d0251f09d8078e923e776d6cfd243ad5016ee7b736
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.5 KB (134547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cec47acd1251b8ac33a2e9c1b58b7681dd847c17ec5f9f9b3c3de9f0a3d9eb23`

```dockerfile
```

-	Layers:
	-	`sha256:ceb04bbdaeb5e9e9d2f2a4dc75511669e60ed5fa7a217404c2826e395e4e17ed`  
		Last Modified: Tue, 03 Feb 2026 17:24:05 GMT  
		Size: 116.5 KB (116471 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34a68fd3496bbf77073b208dff454802918454d5766dd0d28dbd4b9adba9f788`  
		Last Modified: Tue, 03 Feb 2026 17:24:05 GMT  
		Size: 18.1 KB (18076 bytes)  
		MIME: application/vnd.in-toto+json
