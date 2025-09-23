## `bash:devel-alpine3.22`

```console
$ docker pull bash@sha256:312587d9b9316975079b4f0ec943d153df6eeab03db986d4174d3c2fa79c5cb5
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

### `bash:devel-alpine3.22` - linux; amd64

```console
$ docker pull bash@sha256:8c4dd3f704a443e34a1aa9952b304de5148c54388ff6aed80d0a2b06db1da65d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6802668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:376e768ec4e15b92ee8ddb2ea388c2418902684b24eb8ef58421ba85478ab296`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 23 Sep 2025 10:21:35 GMT
ENV _BASH_COMMIT=cf8a2518c8b94f75b330d398f5daa0ee21417e1b
# Tue, 23 Sep 2025 10:21:35 GMT
ENV _BASH_VERSION=devel-20250918
# Tue, 23 Sep 2025 10:21:35 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 23 Sep 2025 10:21:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 23 Sep 2025 10:21:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 23 Sep 2025 10:21:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Sep 2025 10:21:35 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1926526997ec4e13dc9bbe4ba4f53170824005a10365fc710e5c8ad1359f52a0`  
		Last Modified: Tue, 23 Sep 2025 19:48:19 GMT  
		Size: 458.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:429cd906597a7ff3376ef34717171a0e238e4504714404ee3b9338b733e99230`  
		Last Modified: Tue, 23 Sep 2025 19:48:19 GMT  
		Size: 3.0 MB (3002191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed9f46a56c4c5ae30a323030e6836e61d838562a16edccbebbfa6957608ddb2a`  
		Last Modified: Tue, 23 Sep 2025 19:48:19 GMT  
		Size: 330.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.22` - unknown; unknown

```console
$ docker pull bash@sha256:efa875aad1ba755baa56431a0b5e02d2a1b227789d7870d6d87e74c5e721f387
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.6 KB (136608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28e6e15a721de710a49ecd2786089113c00bd4c7a2ce0fc978f3c08f61b311b0`

```dockerfile
```

-	Layers:
	-	`sha256:9f56468dcfbbda1c1f2623470b27c55dbafc00d79f322fb3b6fc8696febc3f5b`  
		Last Modified: Tue, 23 Sep 2025 21:02:53 GMT  
		Size: 118.4 KB (118429 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a2ac718c521146de715a792882a09a3c757ef6ff7a3f295efd5f94aec95f554`  
		Last Modified: Tue, 23 Sep 2025 21:02:54 GMT  
		Size: 18.2 KB (18179 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.22` - linux; arm variant v6

```console
$ docker pull bash@sha256:70785706e1f4bc2fccd3b585edba4e674e696541a34c594b83e2aa0cb87a322c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6441978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1eb5e04632f1a34938d3cebef86401b75d452e5ea0fa559e4898ebae111084b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 23 Sep 2025 10:21:35 GMT
ENV _BASH_COMMIT=cf8a2518c8b94f75b330d398f5daa0ee21417e1b
# Tue, 23 Sep 2025 10:21:35 GMT
ENV _BASH_VERSION=devel-20250918
# Tue, 23 Sep 2025 10:21:35 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 23 Sep 2025 10:21:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 23 Sep 2025 10:21:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 23 Sep 2025 10:21:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Sep 2025 10:21:35 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:327f0ef74923f6992c80fc202fcfe6f552711be065291ad660bd8fbcc3cbc919`  
		Last Modified: Tue, 23 Sep 2025 18:04:55 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eab8fa79daf1db771cddcf09f0b6005d00b269957b98aede49364874685e6bd`  
		Last Modified: Tue, 23 Sep 2025 18:04:56 GMT  
		Size: 2.9 MB (2940276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3413be753c8bdd20ce43b9bc35daffc418caa6a657da1f67ba84eac1340cceb`  
		Last Modified: Tue, 23 Sep 2025 18:04:56 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.22` - unknown; unknown

```console
$ docker pull bash@sha256:0956eb7502431db2e45f49e84dbeb5982c6abdb73f76c2e3333dcb71bb0e6814
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (18044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5452f1658eea617e467de5b2e6d8bfe0c04f0b314022ec8e5cbd33213ee8aaa`

```dockerfile
```

-	Layers:
	-	`sha256:31f5b60b5dbe090655a63cf1d1bc0a36686b63b2455bc4fa37f42c199d762823`  
		Last Modified: Tue, 23 Sep 2025 21:02:57 GMT  
		Size: 18.0 KB (18044 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.22` - linux; arm variant v7

```console
$ docker pull bash@sha256:b4ba1e59f182456ea3949d5491eee32ed9c30a81508d9892a51ec80fd540304c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6110978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2278bfc3a11eab3d7a77b623b8f18e78f05566457c7700c29243724ff4414e78`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 23 Sep 2025 10:21:35 GMT
ENV _BASH_COMMIT=cf8a2518c8b94f75b330d398f5daa0ee21417e1b
# Tue, 23 Sep 2025 10:21:35 GMT
ENV _BASH_VERSION=devel-20250918
# Tue, 23 Sep 2025 10:21:35 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 23 Sep 2025 10:21:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 23 Sep 2025 10:21:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 23 Sep 2025 10:21:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Sep 2025 10:21:35 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36da663a751c3b30d32482bb7f138e1224e054f4185b4e0cd8c9d42aaa338a3c`  
		Last Modified: Tue, 23 Sep 2025 18:07:53 GMT  
		Size: 459.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7504c585bc36c17de2b9c2468c85026fc1ab4e5ef343888c267b04d7d45976a0`  
		Last Modified: Tue, 23 Sep 2025 18:07:53 GMT  
		Size: 2.9 MB (2891148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2ea07471893ce1b2d3c1cbdefa96894d50fa7e6a0aa57d8c40e6a1f1c84d6c8`  
		Last Modified: Tue, 23 Sep 2025 18:07:53 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.22` - unknown; unknown

```console
$ docker pull bash@sha256:4c85a8ed83340d57ac27b43d5502ac24d389f8bec7bb01c12a92b56d34c06518
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.7 KB (136724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b049757edff71fdf5ff456816a75ad8a4c105b163a9550cd368386a225091f1`

```dockerfile
```

-	Layers:
	-	`sha256:fd0641e60f2b70465fe7001cd9c75951947c62c701ca3b24b23ab49cd50897c2`  
		Last Modified: Tue, 23 Sep 2025 21:03:00 GMT  
		Size: 118.5 KB (118465 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f56d4862a63231bd4be79bcb1b7edef6a92abcf116e410c227529cdb34354c1e`  
		Last Modified: Tue, 23 Sep 2025 21:03:01 GMT  
		Size: 18.3 KB (18259 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull bash@sha256:b102aeaab00f1e6da769da7322c52dfca8c2596dad406c7222be2d3a33f9a10a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7220722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c35d990464d7cba80fe79c6926f4f96ae3b1710b15173253c82747e2ec67548`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 23 Sep 2025 10:21:35 GMT
ENV _BASH_COMMIT=cf8a2518c8b94f75b330d398f5daa0ee21417e1b
# Tue, 23 Sep 2025 10:21:35 GMT
ENV _BASH_VERSION=devel-20250918
# Tue, 23 Sep 2025 10:21:35 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 23 Sep 2025 10:21:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 23 Sep 2025 10:21:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 23 Sep 2025 10:21:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Sep 2025 10:21:35 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:921cfe8319f05bdcd5a2223996f5bb1d5480d55ea574923dde6959ae1b530c2b`  
		Last Modified: Tue, 23 Sep 2025 18:05:30 GMT  
		Size: 458.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6206ef5c70d710e715e848ed59eb4c461e066917ae9ede141284c45cb4b4e1ce`  
		Last Modified: Tue, 23 Sep 2025 18:05:07 GMT  
		Size: 3.1 MB (3089182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2854d57619c3fc9c608ae0ce8c8e35b4fd30fe529ad23a3af41629e0585e9ec8`  
		Last Modified: Tue, 23 Sep 2025 18:05:07 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.22` - unknown; unknown

```console
$ docker pull bash@sha256:8c0c675380e308a6fe372e5a6dbab1a04d6125027ef0b0777b2be849ea16f2a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.8 KB (136768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8fa021fdd73046eefe67c89fa052590e77c756a2f0d2038f1bdc5a739d2b9e2`

```dockerfile
```

-	Layers:
	-	`sha256:a3dc1200888f0faca16d86dd2b35b645de55905edd4ee3a6271886c62380decb`  
		Last Modified: Tue, 23 Sep 2025 21:03:04 GMT  
		Size: 118.5 KB (118485 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c26b4dcf4fb95825e0475038b3993887e2a790ce421ff7d810e3aee0be06437`  
		Last Modified: Tue, 23 Sep 2025 21:03:05 GMT  
		Size: 18.3 KB (18283 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.22` - linux; 386

```console
$ docker pull bash@sha256:218aee2984e84c65924fd64d7ea0f54943dfa926d742cac97e46d18c43792cbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6543500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd32cc1074173c40e309941f30922264b255f08909bd19f358c80f7d19afb28f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 23 Sep 2025 10:21:35 GMT
ENV _BASH_COMMIT=cf8a2518c8b94f75b330d398f5daa0ee21417e1b
# Tue, 23 Sep 2025 10:21:35 GMT
ENV _BASH_VERSION=devel-20250918
# Tue, 23 Sep 2025 10:21:35 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 23 Sep 2025 10:21:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 23 Sep 2025 10:21:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 23 Sep 2025 10:21:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Sep 2025 10:21:35 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:a55f2fb89da4caae0d783c0045a67446dee9bbd977fecb44db9e1231550fa888`  
		Last Modified: Tue, 15 Jul 2025 19:04:11 GMT  
		Size: 3.6 MB (3615006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee20a2e575793e9b009c533a8fd4a997eb171d0d64ed4a86f7fbe800a464e790`  
		Last Modified: Tue, 23 Sep 2025 18:05:58 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f3dd71674af4759a9eb3e16e816a7ac32f4cfef3db6bd6360a973fb776ad24`  
		Last Modified: Tue, 23 Sep 2025 18:05:58 GMT  
		Size: 2.9 MB (2927705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caae81acb674ae83735be13063ca4841aa217c6b429886dd82c71fd9c8f95b3f`  
		Last Modified: Tue, 23 Sep 2025 18:05:58 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.22` - unknown; unknown

```console
$ docker pull bash@sha256:a9d7aef8f4543759588dd3953678b58c023752a26294524e8f5f7ca3ef686b45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.6 KB (136551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12b6d5fed2e1cbc0509f5aaf520fd33e885a55c72536760be99db6303327e741`

```dockerfile
```

-	Layers:
	-	`sha256:7b27b077c707d52f6f32f838f6042ae4da9db542e474207b45ed96a6fb22c51a`  
		Last Modified: Tue, 23 Sep 2025 21:03:08 GMT  
		Size: 118.4 KB (118404 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6055db48500408449e8cf063896bc44c5a61154b5a58a05409d4f4633f53269a`  
		Last Modified: Tue, 23 Sep 2025 21:03:09 GMT  
		Size: 18.1 KB (18147 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.22` - linux; ppc64le

```console
$ docker pull bash@sha256:e09514bea64ceb7d1e0c75293c378bf7be274e00c254abd1ba092934674bf28b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7003318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fb00f1eaa5c09ee75d4b5ee52f32902887589f726e367c3968be93049c627a5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 23 Sep 2025 10:21:35 GMT
ENV _BASH_COMMIT=cf8a2518c8b94f75b330d398f5daa0ee21417e1b
# Tue, 23 Sep 2025 10:21:35 GMT
ENV _BASH_VERSION=devel-20250918
# Tue, 23 Sep 2025 10:21:35 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 23 Sep 2025 10:21:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 23 Sep 2025 10:21:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 23 Sep 2025 10:21:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Sep 2025 10:21:35 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2827cb18b1848c6600ad7fdd381e12b7c9537219a9b24ba0cf15f756859fbd2c`  
		Last Modified: Tue, 23 Sep 2025 18:04:52 GMT  
		Size: 458.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df5f0b06a603432261ddcc5bd769220dce98d49696e85e124f21ac5b67d034ac`  
		Last Modified: Tue, 23 Sep 2025 18:04:52 GMT  
		Size: 3.3 MB (3275410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6c5325d81caa16492cfd1280f9786e8d9bfc7762ed192a10e89156beac7db11`  
		Last Modified: Tue, 23 Sep 2025 18:04:52 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.22` - unknown; unknown

```console
$ docker pull bash@sha256:08cce5c9e03cc970cea678e1321654ae42ab92c62bef6b8c017029d216c1a3c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 KB (134735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cffa6e8695b431f4150f7b9bf2bf5ffc71de9840899616a816786ba38778737`

```dockerfile
```

-	Layers:
	-	`sha256:ec1a5bea75e11c7e067b47d8d658a475abbb077bd7c44ee0298a7070e8adec64`  
		Last Modified: Tue, 23 Sep 2025 21:03:13 GMT  
		Size: 116.5 KB (116512 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8b25520d1819898f6ead9dc9ff1e78e55825824ca8f2d3a31471fcc29096f9a`  
		Last Modified: Tue, 23 Sep 2025 21:03:13 GMT  
		Size: 18.2 KB (18223 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.22` - linux; riscv64

```console
$ docker pull bash@sha256:b6b1a87f8375c5e26eb89a3711c30f090dab1571821fed26ed4a9a1543f8a0d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6462256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1451fecafb314c70632f52afb0a1d2279c0f0dee2e1f12b44e8a435b4aa7f020`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 23 Sep 2025 10:21:35 GMT
ENV _BASH_COMMIT=cf8a2518c8b94f75b330d398f5daa0ee21417e1b
# Tue, 23 Sep 2025 10:21:35 GMT
ENV _BASH_VERSION=devel-20250918
# Tue, 23 Sep 2025 10:21:35 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 23 Sep 2025 10:21:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 23 Sep 2025 10:21:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 23 Sep 2025 10:21:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Sep 2025 10:21:35 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:939ecb2c5bb396fba892ee75cc90fad15afe5e8468e6e15f915f925769d8983e`  
		Last Modified: Tue, 23 Sep 2025 18:13:16 GMT  
		Size: 459.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68bf2e72cc6584be0328b9b86afde9fc8513cf6458b6795c6bb194cdeed3ed19`  
		Last Modified: Tue, 23 Sep 2025 18:13:17 GMT  
		Size: 2.9 MB (2948658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1433af8ebf64213a9613ccaff4badd9dc5402cb5547ea54517a099985e71b666`  
		Last Modified: Tue, 23 Sep 2025 18:13:18 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.22` - unknown; unknown

```console
$ docker pull bash@sha256:092b46b2621c560c5b601536901cfb03704ec2c1a3feb78bd896cdfc7eb2ee08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 KB (134731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8e5c2801470bef76d63a95c88290addb49e0bd0dcb3c4b47c7cd93b2a2328de`

```dockerfile
```

-	Layers:
	-	`sha256:82284d1158cc09387d7401a4c25f336954b4b1d25404f6a9a4df0d1740c64daa`  
		Last Modified: Tue, 23 Sep 2025 21:03:16 GMT  
		Size: 116.5 KB (116508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e23bd548367cd930ddd72125a23ab1240b8699ea7e0594f1da4ea33e2aa44885`  
		Last Modified: Tue, 23 Sep 2025 21:03:17 GMT  
		Size: 18.2 KB (18223 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.22` - linux; s390x

```console
$ docker pull bash@sha256:9d4694c81f4910c1f3b29cec757da0a11d8dc22f2948b360f46014e2a3815d82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6738967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f27946cfc66702ec14653f38c77c98a1c2a6a99db8fc37e785ca6614dfee5e0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 23 Sep 2025 10:21:35 GMT
ENV _BASH_COMMIT=cf8a2518c8b94f75b330d398f5daa0ee21417e1b
# Tue, 23 Sep 2025 10:21:35 GMT
ENV _BASH_VERSION=devel-20250918
# Tue, 23 Sep 2025 10:21:35 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 23 Sep 2025 10:21:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 23 Sep 2025 10:21:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 23 Sep 2025 10:21:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Sep 2025 10:21:35 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aad62a67006bbf0e845a2acb935f292e7525ff97cba8d2bb966e7000ccfde735`  
		Last Modified: Tue, 23 Sep 2025 18:07:40 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f3858708d54ed9dd60afd004aaac95c86b13835124ea6fcbd5755196f11d045`  
		Last Modified: Tue, 23 Sep 2025 18:05:55 GMT  
		Size: 3.1 MB (3093207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4835da107ceeb4ea54ee4ccef3c146b87bf3e4adadbb85ebc8564afe5635f6c6`  
		Last Modified: Tue, 23 Sep 2025 18:05:54 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.22` - unknown; unknown

```console
$ docker pull bash@sha256:2c6fb1d8d3682d50625ea6497627c46e066c4ae2ac60b11545c3e6bb56acd24b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 KB (134657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c609eefa2d3e633ec94401acee65bce19e4c32f66cbcb5d613f477bba5ecad2`

```dockerfile
```

-	Layers:
	-	`sha256:520cbc761573770bba50907959c8d47f4634c7008d2273ad1bfc7739d6a4195c`  
		Last Modified: Tue, 23 Sep 2025 21:03:20 GMT  
		Size: 116.5 KB (116478 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd44c778d95dcd4dde526e0fe7448c8590b42cdba0f07f8bdf423cfa1aa24ca9`  
		Last Modified: Tue, 23 Sep 2025 21:03:21 GMT  
		Size: 18.2 KB (18179 bytes)  
		MIME: application/vnd.in-toto+json
