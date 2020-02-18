## `bash:devel`

```console
$ docker pull bash@sha256:30b7232db2abd748c952d50a99bd1932c8afad9d0e39cb49995c0d5aeff47d34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `bash:devel` - linux; amd64

```console
$ docker pull bash@sha256:792143567223447c6e9d4a967a6132705367362b652e69aba84a13163d85dac7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5788308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fb489f5e97574b0d1a1e1a94b9e9b5adc271c1151682257da6ce8a965a47559`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 18 Jan 2020 01:19:37 GMT
ADD file:e69d441d729412d24675dcd33e04580885df99981cec43de8c9b24015313ff8e in / 
# Sat, 18 Jan 2020 01:19:37 GMT
CMD ["/bin/sh"]
# Tue, 18 Feb 2020 00:19:28 GMT
ENV _BASH_COMMIT=89d788fb0152724a93e0fdab8c15116e5c76572b
# Tue, 18 Feb 2020 00:19:28 GMT
ENV _BASH_COMMIT_DESC=commit bash-20200214 snapshot
# Tue, 18 Feb 2020 00:20:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 	fi; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -r 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .bash-rundeps $runDeps; 	apk del .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version
# Tue, 18 Feb 2020 00:20:17 GMT
COPY file:651b3bebeba8be9162c56b3eb561199905235f3e1c7811232b6c9f48ac333651 in /usr/local/bin/ 
# Tue, 18 Feb 2020 00:20:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Feb 2020 00:20:17 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:c9b1b535fdd91a9855fb7f82348177e5f019329a58c53c47272962dd60f71fc9`  
		Last Modified: Fri, 17 Jan 2020 08:04:01 GMT  
		Size: 2.8 MB (2802957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7b2707f63ce96a96b934065d321df6d15c133356d0dd57d97583e5f2a78c681`  
		Last Modified: Tue, 18 Feb 2020 00:21:00 GMT  
		Size: 3.0 MB (2985005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:822c1eb55be6945053c071ab8af9ae03444a2cf936d6561756a4f1c58e5722cd`  
		Last Modified: Tue, 18 Feb 2020 00:20:59 GMT  
		Size: 346.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bash:devel` - linux; arm variant v6

```console
$ docker pull bash@sha256:55f1a42d17a393aaa51d9abea9cd534614d0c3824dafa0de3e937eef7b6df44a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5522439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13da334e6bd232cdeba6cbcc52dae9a31238bcd479aa2893e2809d579b24d567`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 18 Jan 2020 01:53:16 GMT
ADD file:a1906f14a4e217a498b550f86a3d17c9012c02a6df0668043b63848c8fa44b9b in / 
# Sat, 18 Jan 2020 01:53:17 GMT
CMD ["/bin/sh"]
# Tue, 18 Feb 2020 00:49:27 GMT
ENV _BASH_COMMIT=89d788fb0152724a93e0fdab8c15116e5c76572b
# Tue, 18 Feb 2020 00:49:28 GMT
ENV _BASH_COMMIT_DESC=commit bash-20200214 snapshot
# Tue, 18 Feb 2020 00:50:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 	fi; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -r 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .bash-rundeps $runDeps; 	apk del .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version
# Tue, 18 Feb 2020 00:50:42 GMT
COPY file:651b3bebeba8be9162c56b3eb561199905235f3e1c7811232b6c9f48ac333651 in /usr/local/bin/ 
# Tue, 18 Feb 2020 00:50:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Feb 2020 00:50:43 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:832e07764099264ef96e50a1e5e41c52d6b0809bd054e29508a6878aa59d156d`  
		Last Modified: Sat, 18 Jan 2020 01:53:52 GMT  
		Size: 2.6 MB (2617562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa80404a0c5439dc687149e52ec689da2ecb84352d6a88d0aa5e99dc2d9ee738`  
		Last Modified: Tue, 18 Feb 2020 00:52:15 GMT  
		Size: 2.9 MB (2904529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:505cd13833f1d9335645c6654a4ae63ebc4701c8ad3a20907d188be9a7496a13`  
		Last Modified: Tue, 18 Feb 2020 00:52:13 GMT  
		Size: 348.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bash:devel` - linux; arm variant v7

```console
$ docker pull bash@sha256:b6574eebc1c4ccc4fe2a99ce2a41cd5f0d4c233917d5f8375ca81f3f199fcc66
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5275547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c01860d4e80e016bf8aea8bfcd895bc33e111a88b8366b202e03e72c898d0c0a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 18 Jan 2020 02:03:19 GMT
ADD file:4c815f4461ff3b8d481f43d84eb2548cb1adbb3015d370cab86dd7f4d3d94279 in / 
# Sat, 18 Jan 2020 02:03:22 GMT
CMD ["/bin/sh"]
# Tue, 18 Feb 2020 00:57:33 GMT
ENV _BASH_COMMIT=89d788fb0152724a93e0fdab8c15116e5c76572b
# Tue, 18 Feb 2020 00:57:34 GMT
ENV _BASH_COMMIT_DESC=commit bash-20200214 snapshot
# Tue, 18 Feb 2020 00:58:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 	fi; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -r 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .bash-rundeps $runDeps; 	apk del .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version
# Tue, 18 Feb 2020 00:58:33 GMT
COPY file:651b3bebeba8be9162c56b3eb561199905235f3e1c7811232b6c9f48ac333651 in /usr/local/bin/ 
# Tue, 18 Feb 2020 00:58:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Feb 2020 00:58:35 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:3a2c5e3c37b2e3d749405512ef3793aa45a2f5c11615d9e9efa80179262cdf27`  
		Last Modified: Sat, 18 Jan 2020 02:04:05 GMT  
		Size: 2.4 MB (2419554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5fb3b333f972934a58a018a3d3c6c170d5735611e4032495a02d46712883f82`  
		Last Modified: Tue, 18 Feb 2020 00:59:44 GMT  
		Size: 2.9 MB (2855645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0280dcfc532f98a5612547d5b9c10d35739f877b5e5c86f1b74f11814e44f35a`  
		Last Modified: Tue, 18 Feb 2020 00:59:43 GMT  
		Size: 348.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bash:devel` - linux; arm64 variant v8

```console
$ docker pull bash@sha256:1407ef1db33b1102075e45eb0f9fc581b62eb93eaa9d2754bfae93876e7bcfc5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5716306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fabf6a62a2440f26ff140a18321b9c9db169da84e21645707b97a300ea592526`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 18 Jan 2020 01:39:43 GMT
ADD file:4109fa86dd80850e84c689ff9e6a3243e30ab1bbcc00c765969b3011bfbb43e1 in / 
# Sat, 18 Jan 2020 01:39:43 GMT
CMD ["/bin/sh"]
# Tue, 18 Feb 2020 00:39:50 GMT
ENV _BASH_COMMIT=89d788fb0152724a93e0fdab8c15116e5c76572b
# Tue, 18 Feb 2020 00:39:50 GMT
ENV _BASH_COMMIT_DESC=commit bash-20200214 snapshot
# Tue, 18 Feb 2020 00:40:48 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 	fi; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -r 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .bash-rundeps $runDeps; 	apk del .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version
# Tue, 18 Feb 2020 00:40:49 GMT
COPY file:651b3bebeba8be9162c56b3eb561199905235f3e1c7811232b6c9f48ac333651 in /usr/local/bin/ 
# Tue, 18 Feb 2020 00:40:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Feb 2020 00:40:51 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:8fa90b21c985a6fcfff966bdfbde81cdd088de0aa8af38110057f6ac408f4408`  
		Last Modified: Sat, 18 Jan 2020 01:40:23 GMT  
		Size: 2.7 MB (2723075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ab34e9821daa6ef71160b30418e93579ba08a3124b8882eace022ea387c7d82`  
		Last Modified: Tue, 18 Feb 2020 00:42:00 GMT  
		Size: 3.0 MB (2992883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d76651fda1cab7c56ed6ddf0a196ce9c0311e71cf694a3a5501d5f09cb02dbcd`  
		Last Modified: Tue, 18 Feb 2020 00:41:59 GMT  
		Size: 348.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bash:devel` - linux; 386

```console
$ docker pull bash@sha256:8e7f369078438877adb7ebcb685ea9c14627eb3c0cd47be8c3a138d41e66cb39
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5746980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1301536f8212b0b5859b53466860de3964067818541c90168fc94a0fa7fb3fd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 18 Jan 2020 01:38:44 GMT
ADD file:381b617b92fe699ad4ef4f30e0d9599f89e43e252883348c420ebe2a0cccbd63 in / 
# Sat, 18 Jan 2020 01:38:45 GMT
CMD ["/bin/sh"]
# Tue, 18 Feb 2020 00:38:19 GMT
ENV _BASH_COMMIT=89d788fb0152724a93e0fdab8c15116e5c76572b
# Tue, 18 Feb 2020 00:38:19 GMT
ENV _BASH_COMMIT_DESC=commit bash-20200214 snapshot
# Tue, 18 Feb 2020 00:39:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 	fi; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -r 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .bash-rundeps $runDeps; 	apk del .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version
# Tue, 18 Feb 2020 00:39:21 GMT
COPY file:651b3bebeba8be9162c56b3eb561199905235f3e1c7811232b6c9f48ac333651 in /usr/local/bin/ 
# Tue, 18 Feb 2020 00:39:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Feb 2020 00:39:22 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:f024b1263dc58db07a458b73ae1a2dca02ca55bef1ccd1fa3fd50656551fadf2`  
		Last Modified: Sat, 18 Jan 2020 01:39:18 GMT  
		Size: 2.8 MB (2806560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3923b660907160989a9876193b0eb80ecfbd4d32f51283c596f688e5122cf610`  
		Last Modified: Tue, 18 Feb 2020 00:40:11 GMT  
		Size: 2.9 MB (2940072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5eefecb8fb36d8de3158a883e1386d9c334a6f59ffc684458d68e47b9ec4863`  
		Last Modified: Tue, 18 Feb 2020 00:40:10 GMT  
		Size: 348.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bash:devel` - linux; ppc64le

```console
$ docker pull bash@sha256:605fe8c35ff301b0fc164ebbfd37517415d9bbb3548a4581046ad7ce071c1366
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5947735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:069f5561a2267aaaa91c78a292adba16f62922b08536c758f04d2aae786a2fb6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 18 Jan 2020 02:20:41 GMT
ADD file:32ddb3d5255071cca51573ceee2464dd5a87c8d1cce514ae965b6e824d9ef24b in / 
# Sat, 18 Jan 2020 02:20:45 GMT
CMD ["/bin/sh"]
# Tue, 18 Feb 2020 00:16:33 GMT
ENV _BASH_COMMIT=89d788fb0152724a93e0fdab8c15116e5c76572b
# Tue, 18 Feb 2020 00:16:37 GMT
ENV _BASH_COMMIT_DESC=commit bash-20200214 snapshot
# Tue, 18 Feb 2020 00:17:44 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 	fi; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -r 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .bash-rundeps $runDeps; 	apk del .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version
# Tue, 18 Feb 2020 00:17:45 GMT
COPY file:651b3bebeba8be9162c56b3eb561199905235f3e1c7811232b6c9f48ac333651 in /usr/local/bin/ 
# Tue, 18 Feb 2020 00:17:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Feb 2020 00:17:50 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:cd95c8a93e39dcaa0634a65d5b86a88bcd5c3092adb1f96504a7030faa165123`  
		Last Modified: Sat, 18 Jan 2020 02:21:25 GMT  
		Size: 2.8 MB (2822125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:363b535bd052a301250495eb4242983c26e37ee287a911c8c5cf990e6720442b`  
		Last Modified: Tue, 18 Feb 2020 00:18:58 GMT  
		Size: 3.1 MB (3125262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12fa5325868aaf97da0cd9b4255e7ce4f7d717c64067c2ab01259e5ac22560d7`  
		Last Modified: Tue, 18 Feb 2020 00:18:56 GMT  
		Size: 348.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bash:devel` - linux; s390x

```console
$ docker pull bash@sha256:35fd04c54e8b8efda4136e5430966f0ea435958ff2f97b4ce12e36aab9a1eaa6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5576561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:953e03b223dfd2dafe234a2861600c723be29b0cbcce65d573aef626b5404f67`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 18 Jan 2020 01:41:33 GMT
ADD file:a6f8b7d4ba199527053ef1ac710b5e318135cb6903cb9ad6fae4fe42e6ad0bf7 in / 
# Sat, 18 Jan 2020 01:41:33 GMT
CMD ["/bin/sh"]
# Tue, 18 Feb 2020 00:41:27 GMT
ENV _BASH_COMMIT=89d788fb0152724a93e0fdab8c15116e5c76572b
# Tue, 18 Feb 2020 00:41:27 GMT
ENV _BASH_COMMIT_DESC=commit bash-20200214 snapshot
# Tue, 18 Feb 2020 00:41:56 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 	fi; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -r 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .bash-rundeps $runDeps; 	apk del .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version
# Tue, 18 Feb 2020 00:41:57 GMT
COPY file:651b3bebeba8be9162c56b3eb561199905235f3e1c7811232b6c9f48ac333651 in /usr/local/bin/ 
# Tue, 18 Feb 2020 00:41:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Feb 2020 00:41:57 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:176bad61a3a435da03ec603d2bd8f7a69286d92f21f447b17f21f0bc4e085bde`  
		Last Modified: Sat, 18 Jan 2020 01:41:59 GMT  
		Size: 2.6 MB (2582031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bad6f339d5f7def206a882351085b0b965315f4252039c39df2d8d4358f442cb`  
		Last Modified: Tue, 18 Feb 2020 00:42:48 GMT  
		Size: 3.0 MB (2994182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:615ec33d227ec448fd8aea0324d02afb750bc6dc35e1b273ea8c15dd436d3a54`  
		Last Modified: Tue, 18 Feb 2020 00:42:53 GMT  
		Size: 348.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
