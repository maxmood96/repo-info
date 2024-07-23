## `bash:devel`

```console
$ docker pull bash@sha256:fd494e95cbe22bb1dc7918bcca5664ef5eff029f23b01de81fc5a537b1cab40c
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
$ docker pull bash@sha256:768af8da0a30d328b8737e38fd0b9192c5dede55c0f5e3efd312fc85ec73577f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6521282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c651f16b4a144b78f03f125d6aeb2310322539a2ffd0eb95f9f638150e87021`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 20 Jun 2024 20:16:57 GMT
ADD file:33ebe56b967747a97dcec01bc2559962bee8823686c9739d26be060381bbb3ca in / 
# Thu, 20 Jun 2024 20:16:58 GMT
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
	-	`sha256:ec99f8b99825a742d50fb3ce173d291378a46ab54b8ef7dd75e5654e2a296e99`  
		Last Modified: Thu, 20 Jun 2024 20:17:32 GMT  
		Size: 3.6 MB (3623844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b197c565e42feda20114e7b988c4e5b3e1d389d710332d74a3e0580d86b419f8`  
		Last Modified: Tue, 16 Jul 2024 21:58:45 GMT  
		Size: 2.9 MB (2897099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faceeb9fdfa64cf331b758a5cb6efa777bb7f4b2dcb3b0b8ae38fae6f9fa3baf`  
		Last Modified: Tue, 16 Jul 2024 21:58:44 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:302fb84483ff469ae9424cc78f420f2279d99f14c78c1feaccd997968c86a3e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.2 KB (126158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f23d6610c6e2122a90984e0ca93ddf05d6363ca78ec1fe46107fc1fa134e2440`

```dockerfile
```

-	Layers:
	-	`sha256:1a70bccd9c82bf19b72bbafb3ebb2261ea63551a85f61d0c56ca77d4f4a1150a`  
		Last Modified: Tue, 16 Jul 2024 21:58:45 GMT  
		Size: 109.9 KB (109883 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:184d382b6493e5412e024cc57cbc5ce4d439d8e9848ca7438730bebcae2ea6c1`  
		Last Modified: Tue, 16 Jul 2024 21:58:45 GMT  
		Size: 16.3 KB (16275 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; arm variant v6

```console
$ docker pull bash@sha256:e4d191edc182aef2f6f8e9732844c8b0d8a05c64ebd5b7c61e57e871f6f9d5d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6214006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:454df4c4a40e38a7c1f8e44d43752353af845ae5a612956875527dd1b1a10746`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 20 Jun 2024 17:49:15 GMT
ADD file:ef2635f09c1d2632408805d106fbc5d27fb307cb5f584bddc699b4b5ae577623 in / 
# Thu, 20 Jun 2024 17:49:15 GMT
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
	-	`sha256:3d2af5f613c84e549fb09710d45b152d3cdf48eb7a37dc3e9c01e2b3975f4f76`  
		Last Modified: Thu, 20 Jun 2024 17:49:36 GMT  
		Size: 3.4 MB (3367154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d9ac7f7d84c771a49d7d0c50aa6284abb509833c1e96bbcb9fa08bf71854230`  
		Last Modified: Tue, 16 Jul 2024 21:58:34 GMT  
		Size: 2.8 MB (2846518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9fa2f1c495f1ed06be038af231bdeeab409557c8247d52111e8d7f0b11d21b8`  
		Last Modified: Tue, 16 Jul 2024 21:58:33 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:0e3606a17da4cc4170631d59c142ae4e6badb3f6c1faaf5aa86e9726690249f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.1 KB (16125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e0b853ca51a51053d86b58ff377e7df8b3efa06f2fd42468579b6ad8dfc651f`

```dockerfile
```

-	Layers:
	-	`sha256:b385c4ad95479cf654a2b79c41e923e2d8be6eee13522083db04d522449266a7`  
		Last Modified: Tue, 16 Jul 2024 21:58:33 GMT  
		Size: 16.1 KB (16125 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; arm variant v7

```console
$ docker pull bash@sha256:18a9227d72bd1f615c3c2958cf41222e184510b0b0571acbe0562ae161a49e70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5888589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edd73ae5169809c8a2b19e1aed3eb221d4e25399ec8fcb45e47c57d40c7e7402`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 20 Jun 2024 18:00:28 GMT
ADD file:4d58f44e3cedeba6fad741c79bc5acab1a9f2a2f597c854dc3bb8b8595ebf3e1 in / 
# Thu, 20 Jun 2024 18:00:28 GMT
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
	-	`sha256:3fb467f9cb36e54d3cb8806db734a6c640048f3dc270b506ec1f111640905b79`  
		Last Modified: Thu, 20 Jun 2024 18:00:55 GMT  
		Size: 3.1 MB (3094856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b292cdff893c4ecb0ee3e458ff3504c5d0a39af3e3bc87d3426a6f5d54aad6ab`  
		Last Modified: Tue, 16 Jul 2024 21:59:00 GMT  
		Size: 2.8 MB (2793397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1148f312c981a623c772ff4fac7d0e4d07e7d4f66eda7de3ff78a0c46aba1db4`  
		Last Modified: Tue, 16 Jul 2024 21:58:59 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:9085ca4e99c3f9596b487a06ef33916cb93101b1182b68ff09e63cb54e6b86e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.3 KB (126264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78276efe049cd8ea44d32ab204b38d2555c448115226e96b45b521e8d741dc6e`

```dockerfile
```

-	Layers:
	-	`sha256:a3e3dd8b801312aca457bbdd35e1b106f005f460fcca94da9aa3977864734963`  
		Last Modified: Tue, 16 Jul 2024 21:58:59 GMT  
		Size: 109.9 KB (109919 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:941dd2899bafd23291411a305a31b7fb9ade61b428342298c0549b78f16c7641`  
		Last Modified: Tue, 16 Jul 2024 21:58:59 GMT  
		Size: 16.3 KB (16345 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; arm64 variant v8

```console
$ docker pull bash@sha256:5955c4976ca06e6eedac53a5be9d974df1487df0ff81cb1710b68d4c0f5d2448
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7087634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a20a9c07fd803f10fc2860b80f9853023515c9e1bf28676570b83a3a2a08a66`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:35 GMT
ADD file:033626ac44156f3d5800a602c46870486b1492b9ba26096eaa66cceb6fcead77 in / 
# Thu, 20 Jun 2024 17:40:35 GMT
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
	-	`sha256:a258b2a6b59a7aa244d8ceab095c7f8df726f27075a69fca7ad8490f3f63148a`  
		Last Modified: Thu, 20 Jun 2024 17:40:58 GMT  
		Size: 4.1 MB (4088800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a497476a6dfa249d1ce4d0ef97af41c30c05f2411305eef40eaa5310b714aaa`  
		Last Modified: Tue, 16 Jul 2024 21:58:18 GMT  
		Size: 3.0 MB (2998498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ec6c68081c295a2af5c74c606edc7df2bf5335f79471842dcaaed054225ed81`  
		Last Modified: Tue, 16 Jul 2024 21:58:17 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:6d685e6705ff7238785fc525e26a16eba9f8f9f695854961281759caff793e6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.5 KB (126514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f72d86a8513774b0f2c6cbdceb0a601e02134955afb487c5c101117d40d4cf9`

```dockerfile
```

-	Layers:
	-	`sha256:44d80a945736f4fbd7d966fc37abeab82b9aa48810b1504137853f61582ecc80`  
		Last Modified: Tue, 16 Jul 2024 21:58:17 GMT  
		Size: 109.9 KB (109939 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68935744fffef046ac1651fdb063a7a810679f5809bae766277ae185d6774377`  
		Last Modified: Tue, 16 Jul 2024 21:58:17 GMT  
		Size: 16.6 KB (16575 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; 386

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

### `bash:devel` - unknown; unknown

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

### `bash:devel` - linux; ppc64le

```console
$ docker pull bash@sha256:7150c29000c054337a266ef932fd69940feac55f5a2dc4fc905d8692eef06f84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6741583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a72129d688b8a81919c2d8d48b808ad641afc44ed184c5d36faaa6208e2a810d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 20 Jun 2024 18:18:21 GMT
ADD file:c98fdd4075ec8eb66a469bd36f2d1369030638ad4b76778b5ad9c787b9f63c8b in / 
# Thu, 20 Jun 2024 18:18:22 GMT
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
	-	`sha256:b02dcd5eb44e382ea711bca074a007403db63dacf55f888b3a87214d1052dd50`  
		Last Modified: Thu, 20 Jun 2024 18:18:55 GMT  
		Size: 3.6 MB (3571699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33cc5bc0cc99be8020a49551f13aad72c662eab1f04ca03c97c57ef0c54cf604`  
		Last Modified: Tue, 16 Jul 2024 21:58:28 GMT  
		Size: 3.2 MB (3169550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6459b6aa8afe4e2882302299ab2026f63d2942f8b9d36a03cee2acee05d1bc9a`  
		Last Modified: Tue, 16 Jul 2024 21:58:27 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:551ef8cfe766cdf81c32f7309ef59475a85ca67b950e952592efdd669b2e7a44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 KB (124276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76a7ee9f93c5357fde9ade6fa16c632e1432e233a6ba0723fa4060f70b2d6326`

```dockerfile
```

-	Layers:
	-	`sha256:12ebc2ee047284b7956d225ebc12b71f95e3b9e2a655427489ebbbf63a0f564c`  
		Last Modified: Tue, 16 Jul 2024 21:58:28 GMT  
		Size: 108.0 KB (107963 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81a2039b5d629d5b5d7027acf8b92bc372fef06f4320111adf201ae43e28267d`  
		Last Modified: Tue, 16 Jul 2024 21:58:27 GMT  
		Size: 16.3 KB (16313 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; riscv64

```console
$ docker pull bash@sha256:91e3b51adb8d5fb59af196f4c4eabe6f9507125d529eaac8e3f69d0b4f04e08f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6219435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bb23518ba60005a5bcb5390f5e96c863a402e74b61e59641efd4bc1dade0461`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 20 Jun 2024 18:18:03 GMT
ADD file:851dbd05bad08468ee2a960e5f9f0aa9b19f1114ec52c39d1a28cd427344d0ef in / 
# Thu, 20 Jun 2024 18:18:04 GMT
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
	-	`sha256:d4714cc4c8bb5ceda619fceb44b088091082a8d2407d2008123fe93478722d1a`  
		Last Modified: Thu, 20 Jun 2024 18:18:22 GMT  
		Size: 3.4 MB (3371037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e8aec333df526ba42c7b1032f83bd7a9cc693ad69044549c06204e13a096156`  
		Last Modified: Tue, 16 Jul 2024 22:04:57 GMT  
		Size: 2.8 MB (2848061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc1a666617f595941ee4365634c4c02621fd0a7c3bd413af14dc5ac678b968bc`  
		Last Modified: Tue, 16 Jul 2024 22:04:56 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:4fec2a681079423a867adbeb6968c6b1413797ebc147e68c335d8fe1d28c7f8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 KB (124272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a882284f827b6383e9aa8eab2ecad5b7a5405db8e3d26b8115ae652f28842320`

```dockerfile
```

-	Layers:
	-	`sha256:295a0b5c66ac82687aa9a67407271f760dd296e6c2f7de05e64ef1e63de43ffc`  
		Last Modified: Tue, 16 Jul 2024 22:04:57 GMT  
		Size: 108.0 KB (107959 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6cdd68aa0eb21022516bfd7818b402aeae66f18740bcb3500b99464a621c6c7d`  
		Last Modified: Tue, 16 Jul 2024 22:04:57 GMT  
		Size: 16.3 KB (16313 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; s390x

```console
$ docker pull bash@sha256:f82afb556b3bb0648e64c7c7fc7cc89561fe4d42f886b1f70c7e26780aa10edc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6459378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca385d9baa360e2c1e242ace946dc72c6b914fe111166d4cda63bf659e20b315`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 20 Jun 2024 17:42:02 GMT
ADD file:23eeda2aa519e3b51e03f1ce8faeb8c4b597b4b31ec175cb09306147000967fc in / 
# Thu, 20 Jun 2024 17:42:03 GMT
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
	-	`sha256:f9a77bce0ddc1b9251f410e8c69566b002f4e557ee68895b558671311b17fd91`  
		Last Modified: Thu, 20 Jun 2024 17:43:02 GMT  
		Size: 3.5 MB (3461856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23123970e778c7e80215095f15b7962d70d3e319cec56158d5b68f3c96f38278`  
		Last Modified: Tue, 16 Jul 2024 21:58:18 GMT  
		Size: 3.0 MB (2997190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:942163badcd41834b413aa11bc4f1e42039ef657d05aeeca2a01842d505faae5`  
		Last Modified: Tue, 16 Jul 2024 21:58:18 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:2df22c408c28280f2ec3f26b514f77a7b21f3d2515f61e3479a966f18d306ea5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.2 KB (124204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddf1ab87fa11ce2a7e2b540eed20626b6cf736834ee00e150cce0bd229742c8a`

```dockerfile
```

-	Layers:
	-	`sha256:894f81e2be1cdf7f31ea303f19452d373a57d5cc93644466e48b0845ae30f754`  
		Last Modified: Tue, 16 Jul 2024 21:58:18 GMT  
		Size: 107.9 KB (107929 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8590627dd4105fd655b165ba5adbd8c439a8d3d25645f0744052dbc6a667faf`  
		Last Modified: Tue, 16 Jul 2024 21:58:18 GMT  
		Size: 16.3 KB (16275 bytes)  
		MIME: application/vnd.in-toto+json
