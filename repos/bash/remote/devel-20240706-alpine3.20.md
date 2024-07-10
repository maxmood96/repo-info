## `bash:devel-20240706-alpine3.20`

```console
$ docker pull bash@sha256:2643288bd21530b3e42e96eb8c9d81af96585bb3f1c2362fac0e67f40c96d098
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

### `bash:devel-20240706-alpine3.20` - linux; amd64

```console
$ docker pull bash@sha256:346dd6ecaa4c162c69727b9b1f84673e3c5f4c5f7c5e8bf1b4a11fb3ff191dbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6521510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:147f11249994df0b0c7f1de4db263bb8d33ede986afe42ffac60c8bc38bc6f0f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 20 Jun 2024 20:16:57 GMT
ADD file:33ebe56b967747a97dcec01bc2559962bee8823686c9739d26be060381bbb3ca in / 
# Thu, 20 Jun 2024 20:16:58 GMT
CMD ["/bin/sh"]
# Tue, 09 Jul 2024 04:18:10 GMT
ENV _BASH_COMMIT=a91b8b077300b0a2a7daefe02f0363f9116e00d5
# Tue, 09 Jul 2024 04:18:10 GMT
ENV _BASH_VERSION=devel-20240706
# Tue, 09 Jul 2024 04:18:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 09 Jul 2024 04:18:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 09 Jul 2024 04:18:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jul 2024 04:18:10 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:ec99f8b99825a742d50fb3ce173d291378a46ab54b8ef7dd75e5654e2a296e99`  
		Last Modified: Thu, 20 Jun 2024 20:17:32 GMT  
		Size: 3.6 MB (3623844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1b424d629f56cf84bc16950ee3b58140ceb365dfb8bcaecac6271765c79943a`  
		Last Modified: Tue, 09 Jul 2024 18:59:01 GMT  
		Size: 2.9 MB (2897334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24b5d59eb00fb4f58c7d84953c4d63d73fb0e8f8c6656d10d07dbbc7e84311e6`  
		Last Modified: Tue, 09 Jul 2024 18:59:00 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20240706-alpine3.20` - unknown; unknown

```console
$ docker pull bash@sha256:b805f70258c768e4057670272fe1a547467fcf1178f4cce37e2b5f5c5739677f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.7 KB (122652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:027dc992155bef94421e558e7f3d4e5902e9a8632ffa388779bfd48fbc32dfd1`

```dockerfile
```

-	Layers:
	-	`sha256:54fd30517b406218a8f482834a86a52dd7639823b00bd09573be5f91e470ae5a`  
		Last Modified: Tue, 09 Jul 2024 18:59:00 GMT  
		Size: 106.5 KB (106509 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a95a4e2ae91b6e0f53fb0741c9731cf754faa12a57db29699669b96d938d15bd`  
		Last Modified: Tue, 09 Jul 2024 18:59:00 GMT  
		Size: 16.1 KB (16143 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20240706-alpine3.20` - linux; arm variant v6

```console
$ docker pull bash@sha256:7fe4570ec529865ec7563a67f6894616f4078e386024be6f9c2ecf5694d1ec4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6213380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:508c66164f1a862b1150db2e9d948411c95c603d2c6dc1233b28d5988bce5a45`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 20 Jun 2024 17:49:15 GMT
ADD file:ef2635f09c1d2632408805d106fbc5d27fb307cb5f584bddc699b4b5ae577623 in / 
# Thu, 20 Jun 2024 17:49:15 GMT
CMD ["/bin/sh"]
# Tue, 09 Jul 2024 04:18:10 GMT
ENV _BASH_COMMIT=a91b8b077300b0a2a7daefe02f0363f9116e00d5
# Tue, 09 Jul 2024 04:18:10 GMT
ENV _BASH_VERSION=devel-20240706
# Tue, 09 Jul 2024 04:18:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 09 Jul 2024 04:18:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 09 Jul 2024 04:18:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jul 2024 04:18:10 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:3d2af5f613c84e549fb09710d45b152d3cdf48eb7a37dc3e9c01e2b3975f4f76`  
		Last Modified: Thu, 20 Jun 2024 17:49:36 GMT  
		Size: 3.4 MB (3367154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f2c017570c65bb8229e0d25305214ebf43adbf30165028baff7d6f683c8f5ee`  
		Last Modified: Tue, 09 Jul 2024 21:58:18 GMT  
		Size: 2.8 MB (2845888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7f9404423c4f7f37e89bd61f5f28413533ea5b6c9c94eabcee12b9959f53c54`  
		Last Modified: Tue, 09 Jul 2024 21:58:17 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20240706-alpine3.20` - unknown; unknown

```console
$ docker pull bash@sha256:5c90a1f2da68e6ca6913f57906dae292ee153cf3dfe1318f37f5be7e5e997334
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 KB (15994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58fe5a600a99cf691be08bec97f361a992d13b9df39644e51745fdc754dd3010`

```dockerfile
```

-	Layers:
	-	`sha256:193a5a9ea4e839dfe1c664fe150512b52b4487f3ae1cdc1c5ed2da791243acdf`  
		Last Modified: Tue, 09 Jul 2024 21:58:17 GMT  
		Size: 16.0 KB (15994 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20240706-alpine3.20` - linux; arm variant v7

```console
$ docker pull bash@sha256:5cd75390dea92233ffef319ffcdc9b920a2f7add9d2c7de7c40c9ad874b3f5f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5888444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16bdbce9841b5917ed322806194a8f16b21fbd16026a73756d60c23495f513d8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 20 Jun 2024 18:00:28 GMT
ADD file:4d58f44e3cedeba6fad741c79bc5acab1a9f2a2f597c854dc3bb8b8595ebf3e1 in / 
# Thu, 20 Jun 2024 18:00:28 GMT
CMD ["/bin/sh"]
# Tue, 09 Jul 2024 04:18:10 GMT
ENV _BASH_COMMIT=a91b8b077300b0a2a7daefe02f0363f9116e00d5
# Tue, 09 Jul 2024 04:18:10 GMT
ENV _BASH_VERSION=devel-20240706
# Tue, 09 Jul 2024 04:18:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 09 Jul 2024 04:18:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 09 Jul 2024 04:18:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jul 2024 04:18:10 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:3fb467f9cb36e54d3cb8806db734a6c640048f3dc270b506ec1f111640905b79`  
		Last Modified: Thu, 20 Jun 2024 18:00:55 GMT  
		Size: 3.1 MB (3094856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81dc3cbe83e76e6f5e581afd3099317cf4442735adea30e158c2fce8f3bf4119`  
		Last Modified: Tue, 09 Jul 2024 22:21:18 GMT  
		Size: 2.8 MB (2793253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb5a9bcfeef1ff0687d7e45939e806c356138201b01459c5eec89d9c29e8fe6b`  
		Last Modified: Tue, 09 Jul 2024 22:21:18 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20240706-alpine3.20` - unknown; unknown

```console
$ docker pull bash@sha256:f557d608aadfbf1ed150014993cb9beb4cacf6997b8e0c5aa0b31c001ce44435
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.8 KB (122758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff9d46fd6034543ec841ffaca39d0e4acfb3bd75045c087b531d4c40e2f318ff`

```dockerfile
```

-	Layers:
	-	`sha256:6a7a790da3b79bee0cf0038e0993f008eea38bbfe64a284829350dfa5146a5f9`  
		Last Modified: Tue, 09 Jul 2024 22:21:18 GMT  
		Size: 106.5 KB (106545 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e7ac1c80111a100c1ba0293de1d2ea136e8dbed2e0f55dd2b178bf775e55d70`  
		Last Modified: Tue, 09 Jul 2024 22:21:18 GMT  
		Size: 16.2 KB (16213 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20240706-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull bash@sha256:7ab180b22aea7cd06c4b5be86b8cd915f66f5248228f82bddb20e7ca3f3d3582
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7087719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e96f03ef95ed9ce232a43818db5fe7c780f8d0ea978cc001ff49e2fa8a78bc70`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:35 GMT
ADD file:033626ac44156f3d5800a602c46870486b1492b9ba26096eaa66cceb6fcead77 in / 
# Thu, 20 Jun 2024 17:40:35 GMT
CMD ["/bin/sh"]
# Tue, 09 Jul 2024 04:18:10 GMT
ENV _BASH_COMMIT=a91b8b077300b0a2a7daefe02f0363f9116e00d5
# Tue, 09 Jul 2024 04:18:10 GMT
ENV _BASH_VERSION=devel-20240706
# Tue, 09 Jul 2024 04:18:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 09 Jul 2024 04:18:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 09 Jul 2024 04:18:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jul 2024 04:18:10 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:a258b2a6b59a7aa244d8ceab095c7f8df726f27075a69fca7ad8490f3f63148a`  
		Last Modified: Thu, 20 Jun 2024 17:40:58 GMT  
		Size: 4.1 MB (4088800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fab8ad3c293d517c8ed0d0972b8ef7498bc8be416f3bc68a8c62ebec962ea96a`  
		Last Modified: Tue, 09 Jul 2024 19:37:07 GMT  
		Size: 3.0 MB (2998585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7748b4383d3b519f6e212d35691e983f1beb570085092c1e5a103731e88b3cbf`  
		Last Modified: Tue, 09 Jul 2024 19:37:07 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20240706-alpine3.20` - unknown; unknown

```console
$ docker pull bash@sha256:f935208a0bb68f4eb975338d2e38e075fd5b1aa2db79d2245867b2170e8ac882
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.0 KB (123007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c230028af8346c9a4721114cdf1f190b3a99648e25878782ac54188f4637a060`

```dockerfile
```

-	Layers:
	-	`sha256:dbb648ada8d6fd29f8b79ad20120d48d264d846b16fee3a129fffaf260f9c4a7`  
		Last Modified: Tue, 09 Jul 2024 19:37:07 GMT  
		Size: 106.6 KB (106565 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81c069d792d97f8a8dce687d88ab84d6f4742d460cd262a8f01a1e0c34cc8ab1`  
		Last Modified: Tue, 09 Jul 2024 19:37:07 GMT  
		Size: 16.4 KB (16442 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20240706-alpine3.20` - linux; 386

```console
$ docker pull bash@sha256:ad2cc5ff86ee01a2950f0072d4140115e6d3c4ec5837230da882691f862a404c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6311252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4efcb03c33c0c36ce54267c25ace0fb3788c3b620fb6deda8a3e77ffff9ad3bd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 20 Jun 2024 17:38:24 GMT
ADD file:cd0e8f9dc9e579bd0c884d2c92e4773391bd73d8302d6f4a9bca0796e7ff9a77 in / 
# Thu, 20 Jun 2024 17:38:25 GMT
CMD ["/bin/sh"]
# Tue, 09 Jul 2024 04:18:10 GMT
ENV _BASH_COMMIT=a91b8b077300b0a2a7daefe02f0363f9116e00d5
# Tue, 09 Jul 2024 04:18:10 GMT
ENV _BASH_VERSION=devel-20240706
# Tue, 09 Jul 2024 04:18:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 09 Jul 2024 04:18:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 09 Jul 2024 04:18:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jul 2024 04:18:10 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:354eb832d25d95145569d0a3a573fb95b8350ee897d5b90a2f67ec1157706ec2`  
		Last Modified: Thu, 20 Jun 2024 17:38:50 GMT  
		Size: 3.5 MB (3469470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac6293b4f8b75ec3350ca464cb9d617cb993445dbd772e9eb48792c68c6045a1`  
		Last Modified: Tue, 09 Jul 2024 18:59:02 GMT  
		Size: 2.8 MB (2841450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cb5f4dfd096bee1596cde86a1191f5c7c13c571884380ecf894e3c2b8524309`  
		Last Modified: Tue, 09 Jul 2024 18:59:02 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20240706-alpine3.20` - unknown; unknown

```console
$ docker pull bash@sha256:8b2ca99a0206fa3369e1a6c5d45ccb7ae881237a24933aa87e68d412ec5e6cfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.6 KB (122598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7820d7df09ef581fcc9c02ca1bcaa8af92a580990aca51de9dddff2dcf9a5e2e`

```dockerfile
```

-	Layers:
	-	`sha256:c71773cfbb12fbd76d91fb28bf3e80a96429c363f0c23fe89f1bd95aa0359436`  
		Last Modified: Tue, 09 Jul 2024 18:59:02 GMT  
		Size: 106.5 KB (106484 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10e4f2bfe92aeda77630910fc2b8553f73291394d735766a4696cb77e5372bf1`  
		Last Modified: Tue, 09 Jul 2024 18:59:02 GMT  
		Size: 16.1 KB (16114 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20240706-alpine3.20` - linux; ppc64le

```console
$ docker pull bash@sha256:9d66ec275c55d3489da97f996033da9487ea5ee495dd5f7f3bbd6c67bbb7b670
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6741647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3f0342dc949918797f61a6d62da1243090372f46349b159309d6ec2567f6e5b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 20 Jun 2024 18:18:21 GMT
ADD file:c98fdd4075ec8eb66a469bd36f2d1369030638ad4b76778b5ad9c787b9f63c8b in / 
# Thu, 20 Jun 2024 18:18:22 GMT
CMD ["/bin/sh"]
# Tue, 09 Jul 2024 04:18:10 GMT
ENV _BASH_COMMIT=a91b8b077300b0a2a7daefe02f0363f9116e00d5
# Tue, 09 Jul 2024 04:18:10 GMT
ENV _BASH_VERSION=devel-20240706
# Tue, 09 Jul 2024 04:18:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 09 Jul 2024 04:18:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 09 Jul 2024 04:18:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jul 2024 04:18:10 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:b02dcd5eb44e382ea711bca074a007403db63dacf55f888b3a87214d1052dd50`  
		Last Modified: Thu, 20 Jun 2024 18:18:55 GMT  
		Size: 3.6 MB (3571699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:609db02fb706d5407f286cb515ba26bd8e4838cb1238a27c0d56f5898ef1a376`  
		Last Modified: Tue, 09 Jul 2024 18:58:55 GMT  
		Size: 3.2 MB (3169611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c4987d773494a2abafebfbcb7f252daa8cd9edb27d8b974decb959e58835960`  
		Last Modified: Tue, 09 Jul 2024 18:58:55 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20240706-alpine3.20` - unknown; unknown

```console
$ docker pull bash@sha256:8def5fb6ef8a1f7dc8572922d41f301cbcb742bebe8ad09a842554cf7ede1191
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.8 KB (120770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:681841c4d86b2d705ab559175d72aec82995bcc85458620d884add14b5a6512b`

```dockerfile
```

-	Layers:
	-	`sha256:c0792e9971c1baea3cfbd4bd457265d995b0a2e150955e45b14093d60b9295f2`  
		Last Modified: Tue, 09 Jul 2024 18:58:55 GMT  
		Size: 104.6 KB (104589 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09dca349218ac52d91dff70efab62d95e73d49dc2862e0571f6852be7921e457`  
		Last Modified: Tue, 09 Jul 2024 18:58:55 GMT  
		Size: 16.2 KB (16181 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20240706-alpine3.20` - linux; riscv64

```console
$ docker pull bash@sha256:ee2ee476b005ad65774714ffaaf87451e73abb3176760f2ccc362960712c06f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6219897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58057039b22e9231d0e99a244c208a702bff8f619da49fa3f09607c0eb5d5ad0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 20 Jun 2024 18:18:03 GMT
ADD file:851dbd05bad08468ee2a960e5f9f0aa9b19f1114ec52c39d1a28cd427344d0ef in / 
# Thu, 20 Jun 2024 18:18:04 GMT
CMD ["/bin/sh"]
# Tue, 09 Jul 2024 04:18:10 GMT
ENV _BASH_COMMIT=a91b8b077300b0a2a7daefe02f0363f9116e00d5
# Tue, 09 Jul 2024 04:18:10 GMT
ENV _BASH_VERSION=devel-20240706
# Tue, 09 Jul 2024 04:18:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 09 Jul 2024 04:18:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 09 Jul 2024 04:18:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jul 2024 04:18:10 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:d4714cc4c8bb5ceda619fceb44b088091082a8d2407d2008123fe93478722d1a`  
		Last Modified: Thu, 20 Jun 2024 18:18:22 GMT  
		Size: 3.4 MB (3371037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecd8b341643dec9cbe33d174af3ec05b320ca25f7c0c37a50d97d3604b95610c`  
		Last Modified: Wed, 10 Jul 2024 01:12:17 GMT  
		Size: 2.8 MB (2848521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:832b9bf79bc8d0a8a173397dae8dc2dc67fea62098bdbab2e93b389ff0381932`  
		Last Modified: Wed, 10 Jul 2024 01:12:16 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20240706-alpine3.20` - unknown; unknown

```console
$ docker pull bash@sha256:e6560aabef44d7bda948d2a603632d0aaf9ff745ec4dbd2ce78be47f64241672
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.8 KB (120766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2dec6b0f3901371c9b00d8518233155803bae3de8004ca92929b5ae651f3749`

```dockerfile
```

-	Layers:
	-	`sha256:60a762156741c45879bee728401e3923d0b206f87257f33c44a5d54553676795`  
		Last Modified: Wed, 10 Jul 2024 01:12:16 GMT  
		Size: 104.6 KB (104585 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1524d36f2742308ee53e08e9a2dcd32fd5da2e854f343deacf1ad74cde97c9c`  
		Last Modified: Wed, 10 Jul 2024 01:12:16 GMT  
		Size: 16.2 KB (16181 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20240706-alpine3.20` - linux; s390x

```console
$ docker pull bash@sha256:5cfcf472a57125c8592b16d197d1bd7219bcd80936f41537c7e280f82f566d55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6459526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3680e6cc1683a46d18da78fb41ef6326792a923664aa7c790be82cf4db146f0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 20 Jun 2024 17:42:02 GMT
ADD file:23eeda2aa519e3b51e03f1ce8faeb8c4b597b4b31ec175cb09306147000967fc in / 
# Thu, 20 Jun 2024 17:42:03 GMT
CMD ["/bin/sh"]
# Tue, 09 Jul 2024 04:18:10 GMT
ENV _BASH_COMMIT=a91b8b077300b0a2a7daefe02f0363f9116e00d5
# Tue, 09 Jul 2024 04:18:10 GMT
ENV _BASH_VERSION=devel-20240706
# Tue, 09 Jul 2024 04:18:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 09 Jul 2024 04:18:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 09 Jul 2024 04:18:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jul 2024 04:18:10 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:f9a77bce0ddc1b9251f410e8c69566b002f4e557ee68895b558671311b17fd91`  
		Last Modified: Thu, 20 Jun 2024 17:43:02 GMT  
		Size: 3.5 MB (3461856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97ff915dd493d88284185a02f225f4c09f6e9ede4c058a107254b60965fdbd11`  
		Last Modified: Tue, 09 Jul 2024 20:50:42 GMT  
		Size: 3.0 MB (2997333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c415d9b031d4f75647bdc05498793104f80fce7956b13b8f7b76f0bdbf04d5b4`  
		Last Modified: Tue, 09 Jul 2024 20:50:42 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20240706-alpine3.20` - unknown; unknown

```console
$ docker pull bash@sha256:87568b396f7a486ce8fb411eafcf3e5611c867986f20c2edfc2b8f804c8f498b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.7 KB (120698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cdf8e0bd87b4a3a852285b011c72c9868b22609b1d489643fc1d97166b2c72d`

```dockerfile
```

-	Layers:
	-	`sha256:d79d5093b61fbc3af8604587682d040cd02a071ab7977125d926199960a317b2`  
		Last Modified: Tue, 09 Jul 2024 20:50:42 GMT  
		Size: 104.6 KB (104555 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bdfdbf9be49a1d4fb0b08d0b8be16d8b7b77c1bac93d0a9397eb5f53f10aba5`  
		Last Modified: Tue, 09 Jul 2024 20:50:42 GMT  
		Size: 16.1 KB (16143 bytes)  
		MIME: application/vnd.in-toto+json
