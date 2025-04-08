## `bash:devel-20250404-alpine3.21`

```console
$ docker pull bash@sha256:58118b82c58e659def2393cc53053af8af9517616acb4af1787aa096497ed604
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `bash:devel-20250404-alpine3.21` - linux; amd64

```console
$ docker pull bash@sha256:c824c1b07af1d085a60342688a7db70f245e84f1a6dce200199826d4de4746f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6601654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3a43254d06e820c7f6f467f03c22b93c962f4639e6de29f5c351a0c117ed65d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 08 Apr 2025 04:18:08 GMT
ENV _BASH_COMMIT=2e113467f061587a3475b692d25ca449717834c8
# Tue, 08 Apr 2025 04:18:08 GMT
ENV _BASH_VERSION=devel-20250404
# Tue, 08 Apr 2025 04:18:08 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 08 Apr 2025 04:18:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 08 Apr 2025 04:18:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 08 Apr 2025 04:18:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Apr 2025 04:18:08 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:979b899593e9659a90fbbb5f3c2e77f0b59f3293f00408b7c8ee2cb079ab97b5`  
		Last Modified: Tue, 08 Apr 2025 17:33:34 GMT  
		Size: 458.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7640a3bdd2e11115ea184097b82162d3b6f00a64956347819200fb72802c06fa`  
		Last Modified: Tue, 08 Apr 2025 17:33:35 GMT  
		Size: 3.0 MB (2958616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55aa00a612fed4e678e3d71e4448370b3b570768a00971360c6ed4669ab0b9b7`  
		Last Modified: Tue, 08 Apr 2025 17:33:34 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20250404-alpine3.21` - unknown; unknown

```console
$ docker pull bash@sha256:db612a012c7e36b963ce40a40446c28957d7f5f775dc0ed1d21605cb4e2c1901
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.5 KB (132465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f71d620fd660df40c1901caa387f1fe8d2d06fdafd6d5dac93c1e6050df3a497`

```dockerfile
```

-	Layers:
	-	`sha256:cdb4758a2f11755e7dc69e9088a1e15b4879f53bedfb1bd6b3e0ff5d62f3f1db`  
		Last Modified: Tue, 08 Apr 2025 17:33:34 GMT  
		Size: 114.9 KB (114928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e16e51db203fcbf8f265a895bb47e3a5f43dac518f333b4e913c925c8ee1f6b`  
		Last Modified: Tue, 08 Apr 2025 17:33:34 GMT  
		Size: 17.5 KB (17537 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20250404-alpine3.21` - linux; arm variant v6

```console
$ docker pull bash@sha256:77bfcd29366b209469e84211fcb47a81ee71f477f0f8a742cff6eeb168f20b34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6260291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a77a309a92599959328732c3ba1a485eed6a7f9dd588c1fcce69ca67e4852b2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 08 Apr 2025 04:18:08 GMT
ENV _BASH_COMMIT=2e113467f061587a3475b692d25ca449717834c8
# Tue, 08 Apr 2025 04:18:08 GMT
ENV _BASH_VERSION=devel-20250404
# Tue, 08 Apr 2025 04:18:08 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 08 Apr 2025 04:18:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 08 Apr 2025 04:18:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 08 Apr 2025 04:18:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Apr 2025 04:18:08 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38f71d03b79647836cd876f54899ad58fcddbbb6e8b09ec300fc132bd64af9c6`  
		Last Modified: Fri, 14 Feb 2025 19:17:59 GMT  
		Size: 459.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd2f74824f105052e0b9370e1123ff6f25f043ba1a2a5f7c234643b459d2e823`  
		Last Modified: Tue, 08 Apr 2025 17:31:21 GMT  
		Size: 2.9 MB (2894771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95f2713fa06dcd00072f2be509a1431c767bdc33052cc1d90eeea2726874d65a`  
		Last Modified: Tue, 08 Apr 2025 17:31:21 GMT  
		Size: 330.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20250404-alpine3.21` - unknown; unknown

```console
$ docker pull bash@sha256:7b5a99454286d4d42fb79cbdecc6b13361e9866c3bf6da47b00de35b9eb39198
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 KB (17397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4521c687b4707c2a6e6c4f3d9616fc35b9d76250116e528d21889bcdb83cced1`

```dockerfile
```

-	Layers:
	-	`sha256:1b98d919c0362f1e00740d7365cc6cb0917a6c9fc657613f556e783a5f1f8988`  
		Last Modified: Tue, 08 Apr 2025 17:31:21 GMT  
		Size: 17.4 KB (17397 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20250404-alpine3.21` - linux; 386

```console
$ docker pull bash@sha256:c1242c9fb9cad8868de50f58c4df51d7edeec5b1b19124ee104a38777029258e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6350149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11e17de9b60cf25ebba62645df7d94f93d979f37b1db4f89b563d64b45702243`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 08 Apr 2025 04:18:08 GMT
ENV _BASH_COMMIT=2e113467f061587a3475b692d25ca449717834c8
# Tue, 08 Apr 2025 04:18:08 GMT
ENV _BASH_VERSION=devel-20250404
# Tue, 08 Apr 2025 04:18:08 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 08 Apr 2025 04:18:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 08 Apr 2025 04:18:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 08 Apr 2025 04:18:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Apr 2025 04:18:08 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6389c107b70cf89015422c29fed7234941eb632822a6e81a61af8673a49e2eaa`  
		Last Modified: Tue, 08 Apr 2025 17:30:56 GMT  
		Size: 458.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beb2be2f010d180f3a48007fe9c4387b0cb30a3c6d2c4f75ccaeca9e04b02cbb`  
		Last Modified: Tue, 08 Apr 2025 17:30:56 GMT  
		Size: 2.9 MB (2885738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be1c28448b6329453b1373d123a944534e4208a926374aa4663af650a00025b6`  
		Last Modified: Tue, 08 Apr 2025 17:30:56 GMT  
		Size: 330.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20250404-alpine3.21` - unknown; unknown

```console
$ docker pull bash@sha256:8e5630319abd36ac2414ebfb1f822b1a90f7d9456b427cd68a4af9250f992f35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.4 KB (132408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcd34c49387991659d77ef0ae1bf0dc4ece61b5269d51c5e1add6bf1fbe045db`

```dockerfile
```

-	Layers:
	-	`sha256:e0029e29764a44854707e42d813f17adbdbd50be1b4a88eb7be09e058d8859ba`  
		Last Modified: Tue, 08 Apr 2025 17:30:56 GMT  
		Size: 114.9 KB (114903 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7d2eec4a56f867d90ab667c9b79d133e7f8d87dfed2bb834662d23c5b64494b`  
		Last Modified: Tue, 08 Apr 2025 17:30:56 GMT  
		Size: 17.5 KB (17505 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20250404-alpine3.21` - linux; ppc64le

```console
$ docker pull bash@sha256:bb58d56c8583c848eb38c622d2137559772ef397019b1f386b6301300c3e62c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6806000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60b2b0b985f12cac9a6be323af4dcb2acaec5bf788e406a58557b8e61e6f2d25`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 08 Apr 2025 04:18:08 GMT
ENV _BASH_COMMIT=2e113467f061587a3475b692d25ca449717834c8
# Tue, 08 Apr 2025 04:18:08 GMT
ENV _BASH_VERSION=devel-20250404
# Tue, 08 Apr 2025 04:18:08 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 08 Apr 2025 04:18:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 08 Apr 2025 04:18:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 08 Apr 2025 04:18:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Apr 2025 04:18:08 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e36049ca8d20b61234d6959e293fa53a0267e9cfd98d7f17f6c24ae271b006d4`  
		Last Modified: Tue, 08 Apr 2025 19:29:49 GMT  
		Size: 458.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3365b0e09ad808e31fe678aa872b6e290966bccbe28943047c7956848cf7875`  
		Last Modified: Tue, 08 Apr 2025 19:29:49 GMT  
		Size: 3.2 MB (3230861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90e5d4de5c1095f96126d6e03a8f448c7d83740a1f8b62738a9a89616f7c87de`  
		Last Modified: Tue, 08 Apr 2025 19:29:49 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20250404-alpine3.21` - unknown; unknown

```console
$ docker pull bash@sha256:56a54524aca0850cacf5c038148b858519500189c308bd768e5acf31fbb7dd46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.6 KB (130592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b93672b6cdecf8b6518d6f0ea131b4bc97e30355557b31a12e87338b09d0b21`

```dockerfile
```

-	Layers:
	-	`sha256:e98daa3d81f3a59d09adc4b12cea5ea4a6ba45eff742814760d648dc470c1105`  
		Last Modified: Tue, 08 Apr 2025 19:29:49 GMT  
		Size: 113.0 KB (113011 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7df7d5b7ffbb45a63b439ac86d493ff00e082e9ef6f9baa32d773c49716fee8`  
		Last Modified: Tue, 08 Apr 2025 19:29:49 GMT  
		Size: 17.6 KB (17581 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20250404-alpine3.21` - linux; riscv64

```console
$ docker pull bash@sha256:7a48064ceeb4bbdfb74966c3178e839360c6fa0a9590927b795484c7c2229e5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6261365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c36885cbc7ca7063fa7cd69df4e0fa0028eea657904cb00761e40c9023c17ab3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 08 Apr 2025 04:18:08 GMT
ENV _BASH_COMMIT=2e113467f061587a3475b692d25ca449717834c8
# Tue, 08 Apr 2025 04:18:08 GMT
ENV _BASH_VERSION=devel-20250404
# Tue, 08 Apr 2025 04:18:08 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 08 Apr 2025 04:18:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 08 Apr 2025 04:18:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 08 Apr 2025 04:18:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Apr 2025 04:18:08 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:7df33f7ad8beb367ac09bdd1b2f220db3ee2bbdda14a6310d1340e5628b5ba88`  
		Last Modified: Fri, 14 Feb 2025 18:56:36 GMT  
		Size: 3.4 MB (3351439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03589e78b235e506dafea1c4a2d73b5326f0580bc335cad463e8b5863a7e527d`  
		Last Modified: Fri, 14 Feb 2025 19:22:45 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4b8e889980c21d284ee063b7855ec50c9cfdde434f859cb3ebb4b1c47c55f4f`  
		Last Modified: Tue, 08 Apr 2025 17:40:25 GMT  
		Size: 2.9 MB (2909131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d79e1a753178edcb408a400b36f482dccb634c0b98ffac6da09b1a14af377b38`  
		Last Modified: Tue, 08 Apr 2025 17:40:24 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20250404-alpine3.21` - unknown; unknown

```console
$ docker pull bash@sha256:d719ec9e57a27785b361a66939b75afc1a6bb6dffc3f8a77282f3ddb8735f618
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.6 KB (130588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aacb675942be4f5cfdcb41ae2828deceae6b32209d5e28579cb03fbbf44abbca`

```dockerfile
```

-	Layers:
	-	`sha256:e441fb1c3f0689ef2edb6fac30102e422a04896ffad751722c3bf6e466813cf4`  
		Last Modified: Tue, 08 Apr 2025 17:40:24 GMT  
		Size: 113.0 KB (113007 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24b32f90d118d93b7cf07a31f598eb0dddc922e1c7d9fbce1e5dcc5eb079728e`  
		Last Modified: Tue, 08 Apr 2025 17:40:24 GMT  
		Size: 17.6 KB (17581 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20250404-alpine3.21` - linux; s390x

```console
$ docker pull bash@sha256:9b605884adcb2236af1f478394f91f1ae1443058abda058b84620e9d7f906ad2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6524251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1be395dd3d3bef3c406aeee70c09f104476c376ebd45d6cc7b118979eb7f92ae`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 08 Apr 2025 04:18:08 GMT
ENV _BASH_COMMIT=2e113467f061587a3475b692d25ca449717834c8
# Tue, 08 Apr 2025 04:18:08 GMT
ENV _BASH_VERSION=devel-20250404
# Tue, 08 Apr 2025 04:18:08 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 08 Apr 2025 04:18:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 08 Apr 2025 04:18:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 08 Apr 2025 04:18:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Apr 2025 04:18:08 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:938fac8358e6a698a64c69e9876d1469da804cdb09bb1fbc7cd7f4466de7e7fd`  
		Last Modified: Tue, 25 Mar 2025 20:47:22 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58774f69fc3dcce2692279a8ee6d7704f4b4bc74b441924a228aa8cbe0732543`  
		Last Modified: Tue, 08 Apr 2025 18:22:30 GMT  
		Size: 3.1 MB (3055889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a07bbde00982a2f7319148c8a4e24fb977d0470fa5786fb9db75cf9f30a5adf`  
		Last Modified: Tue, 08 Apr 2025 18:22:30 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20250404-alpine3.21` - unknown; unknown

```console
$ docker pull bash@sha256:4c2978cb66d2ce2e2113c4326e3d3ee0790a48c352b066a6542cb4341af86722
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.5 KB (130514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a099fa3df6da97a1e51e8ac7f76313d4e71d3bb0f3d78e65517fce5b5e48abe`

```dockerfile
```

-	Layers:
	-	`sha256:8cf25dc28904e6cb2842b6e84ee9b33a7b60672aeba153942f7e569ef884033f`  
		Last Modified: Tue, 08 Apr 2025 18:22:30 GMT  
		Size: 113.0 KB (112977 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9f4a0930fb0b44cefb76634ea0d5e5c9befd2660b2d2e320cd0deba24d42526`  
		Last Modified: Tue, 08 Apr 2025 18:22:30 GMT  
		Size: 17.5 KB (17537 bytes)  
		MIME: application/vnd.in-toto+json
