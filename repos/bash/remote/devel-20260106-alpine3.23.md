## `bash:devel-20260106-alpine3.23`

```console
$ docker pull bash@sha256:826945674147cb632242d38f2be8d5318345f4a30e0c88128a75ae00790d3e99
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

### `bash:devel-20260106-alpine3.23` - linux; amd64

```console
$ docker pull bash@sha256:59a61d58c50cb238a8accc7e4e1df5b4c2d3778d25646d005c3e04781a140e10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6872428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03df6a6f932f108f049cbbc43f1d0d186efe8ebd2c90df9f016e9eabd6e9d32b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Tue, 13 Jan 2026 22:52:13 GMT
ENV _BASH_COMMIT=e7c3acf10876963d15f4b6b8030717d308c12bd4
# Tue, 13 Jan 2026 22:52:13 GMT
ENV _BASH_VERSION=devel-20260106
# Tue, 13 Jan 2026 22:52:13 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 13 Jan 2026 22:52:50 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 13 Jan 2026 22:52:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 22:52:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jan 2026 22:52:50 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:49:00 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:003a49e7702d7fe377ef2638a304680ce97f66e0c9799da4475432b605d35e8a`  
		Last Modified: Tue, 13 Jan 2026 22:53:12 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a94596300f432242651a1e953df2fc3447d77e12eef48f1c5f25bbf2e859507f`  
		Last Modified: Tue, 13 Jan 2026 22:52:56 GMT  
		Size: 3.0 MB (3011531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c091575ea4a33d165e937849ddf1257d2018463f0c8e7a24c32c4ce390a3def5`  
		Last Modified: Tue, 13 Jan 2026 22:53:13 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20260106-alpine3.23` - unknown; unknown

```console
$ docker pull bash@sha256:d8d4890a03580793adb2c7110a65df3ec5df9fd3e276f615a493fb1209b2c0f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.3 KB (135330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1edb3ae80790a84c42a858f244b30dba697833ab70f94950c22ee11469d9baea`

```dockerfile
```

-	Layers:
	-	`sha256:4a5edf8bb4b07cce51e05de5c9169619cf87f945296fd6e522c18751b537c28f`  
		Last Modified: Tue, 13 Jan 2026 22:52:55 GMT  
		Size: 117.1 KB (117122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fba28b7d80ddc78826a63392a8e980617a178019d17380b6696a7cddf8ec131b`  
		Last Modified: Tue, 13 Jan 2026 22:52:55 GMT  
		Size: 18.2 KB (18208 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20260106-alpine3.23` - linux; arm variant v6

```console
$ docker pull bash@sha256:ae4a9405ad9112866196f47748f0c952d21a25cd8db7f1e2ba4b606ba26ff9f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6541406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33f5b9e2a8e6986b0f17a1bc08430384bb90be0aba7ea2b5f67432418765464f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Tue, 13 Jan 2026 22:52:06 GMT
ENV _BASH_COMMIT=e7c3acf10876963d15f4b6b8030717d308c12bd4
# Tue, 13 Jan 2026 22:52:06 GMT
ENV _BASH_VERSION=devel-20260106
# Tue, 13 Jan 2026 22:52:06 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 13 Jan 2026 22:52:51 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 13 Jan 2026 22:52:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 22:52:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jan 2026 22:52:51 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:27 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a65d79a8210cd01fce2a61b4529484dd21e93f0ea786f6d4b406fdc1dbfddb7e`  
		Last Modified: Tue, 13 Jan 2026 22:52:55 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0718b71d153cc2d28e8076ee897b9ffe0024049027eec55a8dace3214d21843`  
		Last Modified: Tue, 13 Jan 2026 22:53:04 GMT  
		Size: 3.0 MB (2972185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e369712bece9df1cf6697689d7d45c44489341c6aaaa98fbf73a8a4e1247905`  
		Last Modified: Tue, 13 Jan 2026 22:52:55 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20260106-alpine3.23` - unknown; unknown

```console
$ docker pull bash@sha256:097849bbdf847ed198a6c3e4177b20da6f03bb91aa5570dc4984d0b6272e6993
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 KB (18073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af9a24dc8a4003a479d7e32fd84854a1c65b7763d99dcac5d76171da5a49007c`

```dockerfile
```

-	Layers:
	-	`sha256:569dec5629cc99e531506f11cd55872af54e55427119da2bb7ae90fbf9bdef1c`  
		Last Modified: Wed, 14 Jan 2026 01:03:00 GMT  
		Size: 18.1 KB (18073 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20260106-alpine3.23` - linux; arm variant v7

```console
$ docker pull bash@sha256:854642813d52d3a86e81941c34b9d921f5adabed0d8393e1b5853e22f41319e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6201647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd5e0a030ff015f68f6f312b724117cee7878de06289c432b382ea9dcce33eef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:23 GMT
ADD alpine-minirootfs-3.23.2-armv7.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:23 GMT
CMD ["/bin/sh"]
# Tue, 13 Jan 2026 22:52:13 GMT
ENV _BASH_COMMIT=e7c3acf10876963d15f4b6b8030717d308c12bd4
# Tue, 13 Jan 2026 22:52:13 GMT
ENV _BASH_VERSION=devel-20260106
# Tue, 13 Jan 2026 22:52:13 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 13 Jan 2026 22:52:56 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 13 Jan 2026 22:52:56 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 22:52:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jan 2026 22:52:56 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:fb78f26011a0b45e0ee3135541eee4683a4b98bf30b3d23f0981be37e8794a2a`  
		Last Modified: Thu, 18 Dec 2025 00:12:43 GMT  
		Size: 3.3 MB (3279388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:174dcadd1b6f46251d4ce7e5928679fe812b730ee9b7a944b7e63d4b4807955e`  
		Last Modified: Tue, 13 Jan 2026 22:53:15 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2d09f49c7453f6880d81713da9272c4c750cafa05dd988f008cb834010021e5`  
		Last Modified: Tue, 13 Jan 2026 22:53:23 GMT  
		Size: 2.9 MB (2921470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7819ec9d75d9cdb0f2c5691133cc0ed97c4adf9153688c8b316ffc320ab9dc6`  
		Last Modified: Tue, 13 Jan 2026 22:53:02 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20260106-alpine3.23` - unknown; unknown

```console
$ docker pull bash@sha256:f06cc8eac6b01cb003df7776c46dd70dfffe0bcba068eb88c7ff179c6d67c5cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.8 KB (134795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc0bbef79a65471d1eefe9b859eb0c3d767e94b23ce71cc4c4d9c0c1e0012bb8`

```dockerfile
```

-	Layers:
	-	`sha256:cc7010a39d258d8b5ae05b0cf2893530993f3e02731c5b9a7c18c983c0bf86d9`  
		Last Modified: Wed, 14 Jan 2026 01:03:03 GMT  
		Size: 116.5 KB (116508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98922e5d03a13355b6fad841b853a0649f5fa25365c3b0a85c57a46c8c2fd1f4`  
		Last Modified: Wed, 14 Jan 2026 01:03:04 GMT  
		Size: 18.3 KB (18287 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20260106-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull bash@sha256:f85eaab00e63849373e8495c74d89d04a6be6b354c39b2ded737352d2bfb372e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7276095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0a248f47825b1f81b3e8a2eb896627cd9e68125e639da63e8abe6041cceaca0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Tue, 13 Jan 2026 22:52:18 GMT
ENV _BASH_COMMIT=e7c3acf10876963d15f4b6b8030717d308c12bd4
# Tue, 13 Jan 2026 22:52:18 GMT
ENV _BASH_VERSION=devel-20260106
# Tue, 13 Jan 2026 22:52:18 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 13 Jan 2026 22:52:56 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 13 Jan 2026 22:52:56 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 22:52:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jan 2026 22:52:56 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:50 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26812754cc71de3a96e5d7f94ad4b283586b8b840208626510fc20895eef3f27`  
		Last Modified: Tue, 13 Jan 2026 22:53:18 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6202e9c21c90338789ee708c10f14a3fe716e81d3711e36e118c0263c0af68f4`  
		Last Modified: Tue, 13 Jan 2026 22:53:18 GMT  
		Size: 3.1 MB (3079567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf0416e080abedc4a8d2efc7c3b99d8d42064423149e02d24910512c78f909b1`  
		Last Modified: Tue, 13 Jan 2026 22:53:18 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20260106-alpine3.23` - unknown; unknown

```console
$ docker pull bash@sha256:edbbec2209d1eef24c31dc7dfb73143b406ebef2d315af229efbedb40d308c1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.8 KB (134840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47085d639968dd92e0f8abeb85f7d0bacecfa842d9f59c082d55a33ebd42ca8a`

```dockerfile
```

-	Layers:
	-	`sha256:41d31fe39450bc6e7e85d0ffec4d77177a458a62e0e5ef9002ed6d44142eb8b1`  
		Last Modified: Tue, 13 Jan 2026 22:53:02 GMT  
		Size: 116.5 KB (116528 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6e46d75c3146e4348eca8a59ba5fe72e767e843e15fe9638e10481617faae17`  
		Last Modified: Tue, 13 Jan 2026 22:53:02 GMT  
		Size: 18.3 KB (18312 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20260106-alpine3.23` - linux; 386

```console
$ docker pull bash@sha256:a3bc8f03dec80b4ec42bb5ff03c828ddb195e72ab059ec50cf9a3786cbeeab35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6627574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:400e1ee2937063a387c8d5e0052f929e1de90591b45d1d8a04ee688e3785d1bc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 18 Dec 2025 00:13:19 GMT
ADD alpine-minirootfs-3.23.2-x86.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:13:19 GMT
CMD ["/bin/sh"]
# Tue, 13 Jan 2026 22:52:37 GMT
ENV _BASH_COMMIT=e7c3acf10876963d15f4b6b8030717d308c12bd4
# Tue, 13 Jan 2026 22:52:37 GMT
ENV _BASH_VERSION=devel-20260106
# Tue, 13 Jan 2026 22:52:37 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 13 Jan 2026 22:53:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 13 Jan 2026 22:53:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 22:53:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jan 2026 22:53:17 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:c21df6a7383dfce37a4bfe31b291881f55907c419caf5d06cb6d699d290d0718`  
		Last Modified: Thu, 18 Dec 2025 00:13:38 GMT  
		Size: 3.7 MB (3686100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:534048d3f7d3102ce9186359c59d0b4d35d654e1f269400c88a86b334e207466`  
		Last Modified: Tue, 13 Jan 2026 22:53:32 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e2fbcefd7674ef6327ef0ca2b52f72a541481cbc346f8c78ad1f83d9b6d9fa9`  
		Last Modified: Tue, 13 Jan 2026 22:53:23 GMT  
		Size: 2.9 MB (2940684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c41f767a030a0062cfc56c397f6b591b809f8197519ba886a521aa9adc9e9711`  
		Last Modified: Tue, 13 Jan 2026 22:53:32 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20260106-alpine3.23` - unknown; unknown

```console
$ docker pull bash@sha256:dfe768e74c8c48290a049fa0a5e981663740fac2f4e90fda5d1b16b23400edc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.3 KB (135273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ded33db3868ffefbf7ea315a3c6324d3f77f49b600808d98ff49eff349228457`

```dockerfile
```

-	Layers:
	-	`sha256:cf5db90f6f7d505bc5c864bfba5afdffe93268b56a8c5c537d1aa35b4c7834aa`  
		Last Modified: Tue, 13 Jan 2026 22:53:23 GMT  
		Size: 117.1 KB (117097 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eafa20328144edb16fc21620376f886c96f23b35e61ea31e3271d28d887d34af`  
		Last Modified: Wed, 14 Jan 2026 07:02:48 GMT  
		Size: 18.2 KB (18176 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20260106-alpine3.23` - linux; ppc64le

```console
$ docker pull bash@sha256:34a4282f9222961b53a2e584d56e4cd320b951be711bf54804ed8b467a0e926f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7144968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:610c1e94fd7ff83d7ce855d0a589532553b038d2700a024fa6904adc6bcf3bcd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:34 GMT
ADD alpine-minirootfs-3.23.2-ppc64le.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:34 GMT
CMD ["/bin/sh"]
# Tue, 06 Jan 2026 18:58:47 GMT
ENV _BASH_COMMIT=e7c3acf10876963d15f4b6b8030717d308c12bd4
# Tue, 06 Jan 2026 18:58:47 GMT
ENV _BASH_VERSION=devel-20260106
# Tue, 06 Jan 2026 18:58:47 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 13 Jan 2026 22:53:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 13 Jan 2026 22:53:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 22:53:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jan 2026 22:53:20 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:2dbbc2b20d556edcc853ddf744c4b2e946f16fba62ed0f0c4526533fdaa56e3b`  
		Last Modified: Thu, 18 Dec 2025 00:11:57 GMT  
		Size: 3.8 MB (3827755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66370ff64caff24f7cb3a649867d909a0786e73592e15d3a2290667f7d87ecee`  
		Last Modified: Tue, 06 Jan 2026 19:00:25 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:614e55b0820ed80f7eb31988305af3d129f6b3cd83988aef1b957fdf98e92258`  
		Last Modified: Tue, 13 Jan 2026 22:53:51 GMT  
		Size: 3.3 MB (3316420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aa93487e3cb8e62fbfd7fc964586eb6061d1ebcf4e2691f99487786a6cc1615`  
		Last Modified: Tue, 13 Jan 2026 22:53:36 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20260106-alpine3.23` - unknown; unknown

```console
$ docker pull bash@sha256:ed2a31313e13d9d82b9bff400258700b51a85fbc98346407425649b6147a2574
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.8 KB (134757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b86e96a081201da88b43fa4c64ac9d28a5cd0d72c9d76bbeeb35cbcb0738d40`

```dockerfile
```

-	Layers:
	-	`sha256:b8bd9010a9e23d07880ca4778a51c399960e30db96e61705934fd240298b8315`  
		Last Modified: Wed, 14 Jan 2026 07:02:51 GMT  
		Size: 116.5 KB (116505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6a03bfa7f641309795d580e29702e0e53de0892819a79e04b1ea1e9ec4c4c9d`  
		Last Modified: Wed, 14 Jan 2026 07:02:52 GMT  
		Size: 18.3 KB (18252 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20260106-alpine3.23` - linux; riscv64

```console
$ docker pull bash@sha256:3b26b7c6967e8274dfbeea5e92458b0a6b6b9f46a21efe9bece5b8ab7f11e73e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6788624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d94acead3d5c0a8a184bf1ad01a307786fb167b97e53939a6daaa85b424b7669`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 18 Dec 2025 02:40:00 GMT
ADD alpine-minirootfs-3.23.2-riscv64.tar.gz / # buildkit
# Thu, 18 Dec 2025 02:40:00 GMT
CMD ["/bin/sh"]
# Wed, 07 Jan 2026 04:49:14 GMT
ENV _BASH_COMMIT=e7c3acf10876963d15f4b6b8030717d308c12bd4
# Wed, 07 Jan 2026 04:49:14 GMT
ENV _BASH_VERSION=devel-20260106
# Wed, 07 Jan 2026 04:49:14 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Wed, 14 Jan 2026 04:01:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Wed, 14 Jan 2026 04:01:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 14 Jan 2026 04:01:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jan 2026 04:01:03 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:b4b94acc94b4406ae94f444e29a6c06ae16918e74a98367370cf7529ea8d988c`  
		Last Modified: Thu, 18 Dec 2025 02:40:23 GMT  
		Size: 3.6 MB (3583938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30a0915c11c90c7796fb85d74e9a605c5fd9c8dc8211939e70a75a39808a1341`  
		Last Modified: Wed, 07 Jan 2026 04:58:35 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c2215dee6859fd64a995ae8bc955224279d6195f59afb79ae3b4998804a3cfa`  
		Last Modified: Wed, 14 Jan 2026 04:01:28 GMT  
		Size: 3.2 MB (3203893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:234baa132d1b0cc06e4344d720a715f71ffaeaa422a948647666dd3224080214`  
		Last Modified: Wed, 14 Jan 2026 04:01:50 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20260106-alpine3.23` - unknown; unknown

```console
$ docker pull bash@sha256:c54a5786fb749c738a55d99a3c11f1a09f5a784f4abfa4a2d4b9a60850ed0d21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.8 KB (134753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:600ed59dc7f9b943788456cee47da5ca1cc0b2cb49732959696092f903aa3cbe`

```dockerfile
```

-	Layers:
	-	`sha256:d53e0fb7f595b16d2753fc688929416edec301f8a0527e117addc53e187a5961`  
		Last Modified: Wed, 14 Jan 2026 07:02:55 GMT  
		Size: 116.5 KB (116501 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0bd09bde03dd63002a194fa11540637b3cd2f985ad8e6d688e5a9d581ef4bc5`  
		Last Modified: Wed, 14 Jan 2026 07:02:55 GMT  
		Size: 18.3 KB (18252 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20260106-alpine3.23` - linux; s390x

```console
$ docker pull bash@sha256:ed424b7a4be20144c6010b6be087641a9354647121a2b9552d21b2ba32e62bc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6827307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33846ae805eb8995471019a0b36c7816a3b0026c8209da30092a6acf9f869f49`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:56 GMT
ADD alpine-minirootfs-3.23.2-s390x.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:56 GMT
CMD ["/bin/sh"]
# Tue, 06 Jan 2026 18:52:33 GMT
ENV _BASH_COMMIT=e7c3acf10876963d15f4b6b8030717d308c12bd4
# Tue, 06 Jan 2026 18:52:33 GMT
ENV _BASH_VERSION=devel-20260106
# Tue, 06 Jan 2026 18:52:33 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 13 Jan 2026 22:52:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 13 Jan 2026 22:52:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 22:52:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jan 2026 22:52:12 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:3d8fe54ac4e72ef775998241dc95a39f582dbddd5cf822b793130a331db6726f`  
		Last Modified: Thu, 18 Dec 2025 00:12:04 GMT  
		Size: 3.7 MB (3724311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44787419c87ce7babdf5a9529a53f8c0397ae4d9d35fa8a814789863073a5d73`  
		Last Modified: Tue, 06 Jan 2026 18:53:24 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b37663e8177ced0197a16619e36c8683745b9b68550f852403363d6bd94204f8`  
		Last Modified: Tue, 13 Jan 2026 22:52:22 GMT  
		Size: 3.1 MB (3102207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:547dfcea919e77592d7ec15823b82f6191a3507cc6b6f49c10df2f80f834ff8d`  
		Last Modified: Tue, 13 Jan 2026 22:52:34 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20260106-alpine3.23` - unknown; unknown

```console
$ docker pull bash@sha256:f3c02873c5cab50f1570b2ba3b958e8887e953fcf0e943915b986d4b96a040d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 KB (134679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcb02db9bcffe6d938e60fbdfbb8d5ff042db234dc4ab06352c0a0fd9f0cbbe2`

```dockerfile
```

-	Layers:
	-	`sha256:e6a9f4830d4e4792262df3179f0135c38761763b69888f0bc099aa7a292916c1`  
		Last Modified: Tue, 13 Jan 2026 22:52:21 GMT  
		Size: 116.5 KB (116471 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19ed540eb3f62faf95956268f1ec4cc8b4d6446639374c29dcb11e4f49fd8ea9`  
		Last Modified: Wed, 14 Jan 2026 07:02:59 GMT  
		Size: 18.2 KB (18208 bytes)  
		MIME: application/vnd.in-toto+json
