## `bash:devel`

```console
$ docker pull bash@sha256:1b990c2bd0203a0475b880e3c9336b8d3fbd31e5edace4651b298e49b255d1c0
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
$ docker pull bash@sha256:fc36745ef79d9742dd1d17ea50299a987171392c43a99880cba99f3f54a05a7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6521421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa3a67e9adb5757e98634d3379ff6e3dbb76c654f6853b980fb520cd45592d0c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 20 Jun 2024 20:16:57 GMT
ADD file:33ebe56b967747a97dcec01bc2559962bee8823686c9739d26be060381bbb3ca in / 
# Thu, 20 Jun 2024 20:16:58 GMT
CMD ["/bin/sh"]
# Tue, 02 Jul 2024 04:18:08 GMT
ENV _BASH_COMMIT=5e28a1813ce7d08628c8df584ea36515091c6d9b
# Tue, 02 Jul 2024 04:18:08 GMT
ENV _BASH_VERSION=devel-20240628
# Tue, 02 Jul 2024 04:18:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 02 Jul 2024 04:18:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Jul 2024 04:18:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 04:18:08 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:ec99f8b99825a742d50fb3ce173d291378a46ab54b8ef7dd75e5654e2a296e99`  
		Last Modified: Thu, 20 Jun 2024 20:17:32 GMT  
		Size: 3.6 MB (3623844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49cb14a59efd215b280bfef68a35a148f9e62af363f7b620ffeb5a276eb96236`  
		Last Modified: Tue, 02 Jul 2024 22:06:53 GMT  
		Size: 2.9 MB (2897244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d38e066e4e068ee458c3ae08d3693e71f44c4f4d884ba04b2c76b8a15bfa638`  
		Last Modified: Tue, 02 Jul 2024 22:06:52 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:91027eba83105746237f32cb117ec1e0ec4fc73838951a23b87c05c3b7d5c24a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.8 KB (122752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34619865d8030023067b5cb4913b968f21e99ca3945f128d24ba5f8b803d72c0`

```dockerfile
```

-	Layers:
	-	`sha256:8ec9325c0796bcb1fe87018d13985ab388dc2fa904aac3e2abe34938e2b5910f`  
		Last Modified: Tue, 02 Jul 2024 22:06:53 GMT  
		Size: 106.5 KB (106509 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aaedc625382bdc9c6973268dd94f349e8460995314be183bea21d80b9d81605c`  
		Last Modified: Tue, 02 Jul 2024 22:06:53 GMT  
		Size: 16.2 KB (16243 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; arm variant v6

```console
$ docker pull bash@sha256:a70560c28302930fd06560e25c6062a89d363e90a04a0deb01a0a6b868e25648
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6213317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f4efdf523555beb3f244d7b5ac51cfd8c85307d8411584a71a82d8dab91c4ba`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 20 Jun 2024 17:49:15 GMT
ADD file:ef2635f09c1d2632408805d106fbc5d27fb307cb5f584bddc699b4b5ae577623 in / 
# Thu, 20 Jun 2024 17:49:15 GMT
CMD ["/bin/sh"]
# Tue, 02 Jul 2024 04:18:08 GMT
ENV _BASH_COMMIT=5e28a1813ce7d08628c8df584ea36515091c6d9b
# Tue, 02 Jul 2024 04:18:08 GMT
ENV _BASH_VERSION=devel-20240628
# Tue, 02 Jul 2024 04:18:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 02 Jul 2024 04:18:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Jul 2024 04:18:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 04:18:08 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:3d2af5f613c84e549fb09710d45b152d3cdf48eb7a37dc3e9c01e2b3975f4f76`  
		Last Modified: Thu, 20 Jun 2024 17:49:36 GMT  
		Size: 3.4 MB (3367154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd306395f3bc830122b8f97dee60baf69351e6670eb3961d51ca3fc57480da39`  
		Last Modified: Tue, 02 Jul 2024 22:21:28 GMT  
		Size: 2.8 MB (2845826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcbe2ddeb2dedc890f73009a53fa9b9c6bc94c4ffafbcc0fbac752ae4fee56c8`  
		Last Modified: Tue, 02 Jul 2024 22:21:28 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:84267891afeccb64ac3850d50a2a525f1bc6acff338799533178fdeb73f04335
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.1 KB (16094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fd585784e70c2bc92d150d625e48e6db501031ed446502fe37a656e4e88ce02`

```dockerfile
```

-	Layers:
	-	`sha256:419c7e66f62481161dacc2a8db3f94cfe7a38dd879509f3834d06c248e04b896`  
		Last Modified: Tue, 02 Jul 2024 22:21:28 GMT  
		Size: 16.1 KB (16094 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; arm variant v7

```console
$ docker pull bash@sha256:dd2591bc68c7d26a7f2edf8ea461d3da7d4d1316459eca03183073effa766ac6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5888193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44e1534140352f231068773207da44173429f25df5d14aceb145aaaf04e81c75`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 20 Jun 2024 18:00:28 GMT
ADD file:4d58f44e3cedeba6fad741c79bc5acab1a9f2a2f597c854dc3bb8b8595ebf3e1 in / 
# Thu, 20 Jun 2024 18:00:28 GMT
CMD ["/bin/sh"]
# Tue, 25 Jun 2024 04:18:11 GMT
ENV _BASH_COMMIT=ad1f497a8477df4f3387adfb6a0f465980d2a292
# Tue, 25 Jun 2024 04:18:11 GMT
ENV _BASH_VERSION=devel-20240621
# Tue, 25 Jun 2024 04:18:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 25 Jun 2024 04:18:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Jun 2024 04:18:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Jun 2024 04:18:11 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:3fb467f9cb36e54d3cb8806db734a6c640048f3dc270b506ec1f111640905b79`  
		Last Modified: Thu, 20 Jun 2024 18:00:55 GMT  
		Size: 3.1 MB (3094856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46b79b2444236be9c8b4e916d605799f37e272ac5e0a91b1b57149044146c318`  
		Last Modified: Wed, 26 Jun 2024 02:50:01 GMT  
		Size: 2.8 MB (2792993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a99d99da7c3048e2d35e2fbae971a10b96b515ab1935377adb9cf56ae5527e1c`  
		Last Modified: Wed, 26 Jun 2024 02:50:00 GMT  
		Size: 344.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:4d61a2afb4d5f7f18dd308e10cf7fbae8e1e84972a9f325aed109b4488630d73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.8 KB (122826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5713dd23da8923296ad7e3e8a3bad153568f0e17d8ec7a4bbfe7b2f651be9245`

```dockerfile
```

-	Layers:
	-	`sha256:fd4ff6676afcde7a8966bf539570a1f41fc52b7ed438c3b0e1be61eb686a128e`  
		Last Modified: Wed, 26 Jun 2024 02:50:00 GMT  
		Size: 106.5 KB (106545 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe5e24daceb5be4f33d07d86241044b4e8527792a887f6924dbee375ced3715d`  
		Last Modified: Wed, 26 Jun 2024 02:50:00 GMT  
		Size: 16.3 KB (16281 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; arm64 variant v8

```console
$ docker pull bash@sha256:f1fb7338e8bdebe277e29569ba9b71185025e3319d63d27b1be1e93315129d22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7087557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8ffd7ba4bedf38aa27d329434b85ee7a3125278b4bf7e8355df67bca206eb20`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:35 GMT
ADD file:033626ac44156f3d5800a602c46870486b1492b9ba26096eaa66cceb6fcead77 in / 
# Thu, 20 Jun 2024 17:40:35 GMT
CMD ["/bin/sh"]
# Tue, 25 Jun 2024 04:18:11 GMT
ENV _BASH_COMMIT=ad1f497a8477df4f3387adfb6a0f465980d2a292
# Tue, 25 Jun 2024 04:18:11 GMT
ENV _BASH_VERSION=devel-20240621
# Tue, 25 Jun 2024 04:18:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 25 Jun 2024 04:18:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Jun 2024 04:18:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Jun 2024 04:18:11 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:a258b2a6b59a7aa244d8ceab095c7f8df726f27075a69fca7ad8490f3f63148a`  
		Last Modified: Thu, 20 Jun 2024 17:40:58 GMT  
		Size: 4.1 MB (4088800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bfcaa8f4495b1714ad4a9eed1177465b592daab5bbbb66f17c33e97767c3a1a`  
		Last Modified: Wed, 26 Jun 2024 03:50:25 GMT  
		Size: 3.0 MB (2998424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c8240bb235cd3b50fb1b2e112c3d7c426400fd4499180946b0ea55a27a0d5f8`  
		Last Modified: Wed, 26 Jun 2024 03:50:25 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:50a9d7077b2c86a09cd3d15481e671f597a47a2f1306407cb7f9b6eafde4f74b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.1 KB (123076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d83b0e4509764b7de488a951f75df7ad28f7bc267b8372089d7f81272a307742`

```dockerfile
```

-	Layers:
	-	`sha256:f9c16be5e1824eec611062cad5b495258cb0953f8b238c3e207569a38664c173`  
		Last Modified: Wed, 26 Jun 2024 03:50:24 GMT  
		Size: 106.6 KB (106565 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a88a789d9723bb90baa0239d3aa3575128d3029b0fc234e4a78ddc644aad6fd`  
		Last Modified: Wed, 26 Jun 2024 03:50:25 GMT  
		Size: 16.5 KB (16511 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; 386

```console
$ docker pull bash@sha256:b6600c535da370abcc6151b5bee4309a637b35e62c4d57e8effdf0276f455155
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6311121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4f006dc8996632eb1ec3601cda9cd8c18c8986d6ba1d3c5c9e3d30a4c821898`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 20 Jun 2024 17:38:24 GMT
ADD file:cd0e8f9dc9e579bd0c884d2c92e4773391bd73d8302d6f4a9bca0796e7ff9a77 in / 
# Thu, 20 Jun 2024 17:38:25 GMT
CMD ["/bin/sh"]
# Tue, 25 Jun 2024 04:18:11 GMT
ENV _BASH_COMMIT=ad1f497a8477df4f3387adfb6a0f465980d2a292
# Tue, 25 Jun 2024 04:18:11 GMT
ENV _BASH_VERSION=devel-20240621
# Tue, 25 Jun 2024 04:18:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 25 Jun 2024 04:18:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Jun 2024 04:18:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Jun 2024 04:18:11 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:354eb832d25d95145569d0a3a573fb95b8350ee897d5b90a2f67ec1157706ec2`  
		Last Modified: Thu, 20 Jun 2024 17:38:50 GMT  
		Size: 3.5 MB (3469470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:661366d28db4b4e7b022c3af2574ce1aeb0fe0c888f80d6bfe5c20e6bb5f0ad6`  
		Last Modified: Wed, 26 Jun 2024 02:50:30 GMT  
		Size: 2.8 MB (2841311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7da6471f89a42437efc85dde688767bb5c155bbf05bfbb96dd93ba8885c9383e`  
		Last Modified: Wed, 26 Jun 2024 02:50:30 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:47836d5f2fb8cbd6a5c2bbf9b5b172bc2a049c3e9b90f3708553fe55bd451bb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.7 KB (122665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12267cc021eda01e0e0857e1ccd6933384e9d84f8d42d4d1ca3849901245eea2`

```dockerfile
```

-	Layers:
	-	`sha256:c9bcdc51cdf282fc236a81de6d85ee5df3af33080f27294b247108a38cbda7ec`  
		Last Modified: Wed, 26 Jun 2024 02:50:30 GMT  
		Size: 106.5 KB (106484 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3d29ad0df7de1360d9ef2ca11f7ddb9e6b3f59fce4e951a1adc4cf8d057cbf3`  
		Last Modified: Wed, 26 Jun 2024 02:50:30 GMT  
		Size: 16.2 KB (16181 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; ppc64le

```console
$ docker pull bash@sha256:869823c1e5ebb6f2690de9db12054164a2bc84daf9495afc9e2c2b3a2037b50d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6741224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82f37933b80cadfd704e87482154879d94b83d5aee83b4bbfcd6cbb485e899c6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 20 Jun 2024 18:18:21 GMT
ADD file:c98fdd4075ec8eb66a469bd36f2d1369030638ad4b76778b5ad9c787b9f63c8b in / 
# Thu, 20 Jun 2024 18:18:22 GMT
CMD ["/bin/sh"]
# Tue, 25 Jun 2024 04:18:11 GMT
ENV _BASH_COMMIT=ad1f497a8477df4f3387adfb6a0f465980d2a292
# Tue, 25 Jun 2024 04:18:11 GMT
ENV _BASH_VERSION=devel-20240621
# Tue, 25 Jun 2024 04:18:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 25 Jun 2024 04:18:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Jun 2024 04:18:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Jun 2024 04:18:11 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:b02dcd5eb44e382ea711bca074a007403db63dacf55f888b3a87214d1052dd50`  
		Last Modified: Thu, 20 Jun 2024 18:18:55 GMT  
		Size: 3.6 MB (3571699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38d14f5b4f5dc6ab8bbbb9027b4cac02a3e9bfd090d92ba8e3e3cce1dc3551b7`  
		Last Modified: Wed, 26 Jun 2024 05:29:04 GMT  
		Size: 3.2 MB (3169185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:850cae7b8db6fcd2f74f6d809e3ce0aa32ec87ea798b4670cd54be315d5a5f14`  
		Last Modified: Wed, 26 Jun 2024 05:29:03 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:c519053b023a3a99556c073fd794a28ac2522fe3c3961f054766f129cddfa221
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.8 KB (120838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42e7b43a75bae24060d321203d28c6d7b09067c744cb905d326b82a63e89d0a8`

```dockerfile
```

-	Layers:
	-	`sha256:ae278b87f01918c7fa58ecc1365cc1206bd3eba013637460efa292ce8546e68a`  
		Last Modified: Wed, 26 Jun 2024 05:29:04 GMT  
		Size: 104.6 KB (104589 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dda751ee1ddd350c4ef5d754503633152dbd499986d836e289d830ab9ec8aa4b`  
		Last Modified: Wed, 26 Jun 2024 05:29:03 GMT  
		Size: 16.2 KB (16249 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; riscv64

```console
$ docker pull bash@sha256:98c36c6f2a00d7e1bcb6c778579a0c1b1919b34c5176c7aad41d4a0b3a58d518
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6219673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7092b32e6ab66a1e01d668367e270fa5d50b3ea654f932880675ed21cfdad9a9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 20 Jun 2024 18:18:03 GMT
ADD file:851dbd05bad08468ee2a960e5f9f0aa9b19f1114ec52c39d1a28cd427344d0ef in / 
# Thu, 20 Jun 2024 18:18:04 GMT
CMD ["/bin/sh"]
# Tue, 25 Jun 2024 04:18:11 GMT
ENV _BASH_COMMIT=ad1f497a8477df4f3387adfb6a0f465980d2a292
# Tue, 25 Jun 2024 04:18:11 GMT
ENV _BASH_VERSION=devel-20240621
# Tue, 25 Jun 2024 04:18:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 25 Jun 2024 04:18:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Jun 2024 04:18:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Jun 2024 04:18:11 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:d4714cc4c8bb5ceda619fceb44b088091082a8d2407d2008123fe93478722d1a`  
		Last Modified: Thu, 20 Jun 2024 18:18:22 GMT  
		Size: 3.4 MB (3371037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8952b9155d5ed9b0f0c156440822e2376b9410e85a842734f384a25c8b66822`  
		Last Modified: Wed, 26 Jun 2024 02:56:16 GMT  
		Size: 2.8 MB (2848293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fa6dc29531415ca21749a9fde776b97863df0dedc69b4791830abe5ed89cf76`  
		Last Modified: Wed, 26 Jun 2024 02:56:15 GMT  
		Size: 343.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:3c2aee930b54b26e4d271e29bc4f9ea8016dc566453eb77889aa1017762139ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.8 KB (120834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23f6ad4bbc92eae48f9e59eea20de25a1132e3875ad0da0a2fd1d7da100a9488`

```dockerfile
```

-	Layers:
	-	`sha256:d591985ed0871b79a10ec361d2b8c5a2f602836fec7e9daa683e6e1a41151d57`  
		Last Modified: Wed, 26 Jun 2024 02:56:15 GMT  
		Size: 104.6 KB (104585 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db40d272a0010057fed8246cd3ad6f71a6d583d6607b22f1c6918e79fd98cac6`  
		Last Modified: Wed, 26 Jun 2024 02:56:15 GMT  
		Size: 16.2 KB (16249 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; s390x

```console
$ docker pull bash@sha256:9357e489dbcf43473158e0004c6a9e77de3c9af7d1d3636178e3713a39ef0e61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6459041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6db3e1dbe94b1a676de96c2a82ed39daa0fd8ae6078f914f9a01e82e99cbddf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 20 Jun 2024 17:42:02 GMT
ADD file:23eeda2aa519e3b51e03f1ce8faeb8c4b597b4b31ec175cb09306147000967fc in / 
# Thu, 20 Jun 2024 17:42:03 GMT
CMD ["/bin/sh"]
# Tue, 25 Jun 2024 04:18:11 GMT
ENV _BASH_COMMIT=ad1f497a8477df4f3387adfb6a0f465980d2a292
# Tue, 25 Jun 2024 04:18:11 GMT
ENV _BASH_VERSION=devel-20240621
# Tue, 25 Jun 2024 04:18:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 25 Jun 2024 04:18:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Jun 2024 04:18:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Jun 2024 04:18:11 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:f9a77bce0ddc1b9251f410e8c69566b002f4e557ee68895b558671311b17fd91`  
		Last Modified: Thu, 20 Jun 2024 17:43:02 GMT  
		Size: 3.5 MB (3461856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7135dcbcad9bc0355cfb7d300b4b20fab843b07b2b9053bdbfc7cd24d0e2068d`  
		Last Modified: Wed, 26 Jun 2024 02:50:09 GMT  
		Size: 3.0 MB (2996849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b7999fb7fbd9dcc8d8a14e9997b280ad42f4f65eb3072f90752507870cbe211`  
		Last Modified: Wed, 26 Jun 2024 02:50:09 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:5549c1fd226f6ac5611b7e277959a7042478209920667bb40751ccc466caf05e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.8 KB (120766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:768412beaa3bfa0ba1d8734add520eb352f65ac74dbdf8ff05bcb264359519a2`

```dockerfile
```

-	Layers:
	-	`sha256:b22b35d6243134912a73e0c201775873ddc4052d913eb4961d1efa527b8ccd8b`  
		Last Modified: Wed, 26 Jun 2024 02:50:09 GMT  
		Size: 104.6 KB (104555 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8bc069839043c907cafb4581cde6f38fcf53c2c55553d491d44eff1d01ba9470`  
		Last Modified: Wed, 26 Jun 2024 02:50:09 GMT  
		Size: 16.2 KB (16211 bytes)  
		MIME: application/vnd.in-toto+json
