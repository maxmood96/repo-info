## `bash:devel-20250128-alpine3.21`

```console
$ docker pull bash@sha256:1b5038c0b5ab9f88833be5bf8b2a185acb3a7a242ccf5b3f80e1e94ec49fadd6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown

### `bash:devel-20250128-alpine3.21` - linux; arm variant v6

```console
$ docker pull bash@sha256:492d1af2f16d758d997d126bbb27129ae703124133fc05f4e18db33b6fff40aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6251765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa6344448619f37ad04aadf54e77b29f6d278583a80cf7181fcd67bc255bb4a6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Tue, 04 Feb 2025 05:18:10 GMT
ENV _BASH_COMMIT=0390b4354a9e5df517ef2d4f9d78a099063b22b4
# Tue, 04 Feb 2025 05:18:10 GMT
ENV _BASH_VERSION=devel-20250128
# Tue, 04 Feb 2025 05:18:10 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 04 Feb 2025 05:18:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 04 Feb 2025 05:18:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Feb 2025 05:18:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Feb 2025 05:18:10 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:d3e229a4bb72770bd404e0f6590519a8e566146523e984834c6a3d82836f0069`  
		Last Modified: Wed, 08 Jan 2025 17:23:44 GMT  
		Size: 3.4 MB (3363879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30df67167d1632c1a6da7d7229864f0609dc42113df896a226fec5ace7d08e24`  
		Last Modified: Wed, 08 Jan 2025 18:07:26 GMT  
		Size: 459.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67db2081867282e2ff891fd4925ac4490f06ce9aa4a93bb09bf5922d63f68ae6`  
		Last Modified: Tue, 04 Feb 2025 20:30:53 GMT  
		Size: 2.9 MB (2887094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8311310f2fdee121cd7b52c137c3d0ddf468d4298bea85faa16d84794a4b34a`  
		Last Modified: Tue, 04 Feb 2025 20:30:53 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20250128-alpine3.21` - unknown; unknown

```console
$ docker pull bash@sha256:15aae5416a1018af8680aef7cf9828c3c31278f10f0db95021487fa55947674e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 KB (17514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:798868760f096c0dc41a10781201fa8e589262362703bb835b373bd502c86d89`

```dockerfile
```

-	Layers:
	-	`sha256:db4f8e89617148a2533d0732ad4dac49decbe73985eb2c32696149ae2a618529`  
		Last Modified: Tue, 04 Feb 2025 20:30:53 GMT  
		Size: 17.5 KB (17514 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20250128-alpine3.21` - linux; 386

```console
$ docker pull bash@sha256:d9befa5fef7f5202188cd31f281eb6bde8ab2998f28e12c1eecb17c9c8226bd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6342242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:910e5df3fcd74ad5516de4d8303d481431987c18c190c2c50b253c2537e150c0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Tue, 04 Feb 2025 05:18:10 GMT
ENV _BASH_COMMIT=0390b4354a9e5df517ef2d4f9d78a099063b22b4
# Tue, 04 Feb 2025 05:18:10 GMT
ENV _BASH_VERSION=devel-20250128
# Tue, 04 Feb 2025 05:18:10 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 04 Feb 2025 05:18:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 04 Feb 2025 05:18:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Feb 2025 05:18:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Feb 2025 05:18:10 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:dbaac2331104495e5df0818a1db05c402cfc13af140c75beccf51922d5f37ad5`  
		Last Modified: Wed, 08 Jan 2025 17:23:36 GMT  
		Size: 3.5 MB (3463126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ddafd03c895e8128713a5b95f9b8d73c4422535c24fdbe9150fc21506bf34b8`  
		Last Modified: Tue, 04 Feb 2025 20:31:35 GMT  
		Size: 459.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52a25c7594998783edac337f79227287db459dd892201948bc00c6368ecb09f0`  
		Last Modified: Tue, 04 Feb 2025 20:31:35 GMT  
		Size: 2.9 MB (2878321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ec4f3aca8c1b06956c2a70118b6a0f3e250890f1e8934137f53743261beed1a`  
		Last Modified: Tue, 04 Feb 2025 20:31:35 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20250128-alpine3.21` - unknown; unknown

```console
$ docker pull bash@sha256:98f9397fef70a1055c4a4fbf5ac40349522c929618b519f63a3919f9255ce5b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.5 KB (132518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e54676da4f6a4879fdadefc537a1ef31a6e0a4a6788fccb781892bb6e504f3f9`

```dockerfile
```

-	Layers:
	-	`sha256:f096835a1b3fbed3d0c3d340ba2f44a71069046a4afe3db1339b6b7e741a5d2b`  
		Last Modified: Tue, 04 Feb 2025 20:31:35 GMT  
		Size: 114.9 KB (114897 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a00537c74517e5bd3c29b4dab97319ede5eee6c40e3d80c36d4c4ff556b6381e`  
		Last Modified: Tue, 04 Feb 2025 20:31:35 GMT  
		Size: 17.6 KB (17621 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20250128-alpine3.21` - linux; riscv64

```console
$ docker pull bash@sha256:83a17b12e2c621fc0e1bd2b425eb8768b882a54ebdd32d0dbe88ad2852475112
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6252417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b484e2be0c3e0b93a28afe4b1c0846471495b246becbe0c0c5d2d682f379db93`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-riscv64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Tue, 04 Feb 2025 05:18:10 GMT
ENV _BASH_COMMIT=0390b4354a9e5df517ef2d4f9d78a099063b22b4
# Tue, 04 Feb 2025 05:18:10 GMT
ENV _BASH_VERSION=devel-20250128
# Tue, 04 Feb 2025 05:18:10 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 04 Feb 2025 05:18:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 04 Feb 2025 05:18:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Feb 2025 05:18:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Feb 2025 05:18:10 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:21a89fc8a7107842fa0935d999d700ca9a9df964110a7076d946b16f07a54de5`  
		Last Modified: Wed, 08 Jan 2025 17:48:43 GMT  
		Size: 3.4 MB (3350256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cee5ec45bdf477db840352ec8979a5377f81b57c5bd134c10ef0dd422448e2c3`  
		Last Modified: Wed, 08 Jan 2025 18:10:13 GMT  
		Size: 459.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba78159bd6b72914c7e29200ec10e72d34e390de86dd7692cfad86fc09d9ea63`  
		Last Modified: Tue, 04 Feb 2025 20:40:09 GMT  
		Size: 2.9 MB (2901367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7d5c68bb1733c2219ba44b57f73a0027d030c5781db146a80636eca8f9fb3b1`  
		Last Modified: Tue, 04 Feb 2025 20:40:08 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20250128-alpine3.21` - unknown; unknown

```console
$ docker pull bash@sha256:a3c9942c691bc7e33b41947a641d6f2a6d978d1b89cdeac36e6f89f615a1836b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.7 KB (130698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b1297d9c721b9048e13cc9375030922b37a037190bfe3ac1eedc84c9e684ca7`

```dockerfile
```

-	Layers:
	-	`sha256:71eac0c435e1e47cef47bceaad5af5d96db11ec88f447351f6cb9a361b3468e3`  
		Last Modified: Tue, 04 Feb 2025 20:40:09 GMT  
		Size: 113.0 KB (113001 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42e8993082e4960a26a8b2f997c664fa9cad9641fa7de90a1de22afb93679f83`  
		Last Modified: Tue, 04 Feb 2025 20:40:08 GMT  
		Size: 17.7 KB (17697 bytes)  
		MIME: application/vnd.in-toto+json
