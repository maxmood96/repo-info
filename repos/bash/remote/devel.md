## `bash:devel`

```console
$ docker pull bash@sha256:c1f0aa56005e4da6cf53bb8567efb40d8be4d85949a3975aa7b5f53b050c94a9
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
$ docker pull bash@sha256:d63ea27bf03909f53e90db3c00d9bec6b6c8fd16e7ac95ecda23cdc0a9450189
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5738283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a66a7cc67c769cb4e75e22b407b7400cc9216aa4e97be6624a05416b023a4094`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 29 May 2020 21:19:46 GMT
ADD file:c92c248239f8c7b9b3c067650954815f391b7bcb09023f984972c082ace2a8d0 in / 
# Fri, 29 May 2020 21:19:46 GMT
CMD ["/bin/sh"]
# Sat, 30 May 2020 00:19:35 GMT
ENV _BASH_COMMIT=37adc8b99d4c15dcb9e6582aa19a2ef61afb592f
# Sat, 30 May 2020 00:19:36 GMT
ENV _BASH_COMMIT_DESC=commit bash-20200527 snapshot
# Sat, 30 May 2020 00:20:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 	fi; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -r 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .bash-rundeps $runDeps; 	apk del .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version
# Sat, 30 May 2020 00:20:25 GMT
COPY file:651b3bebeba8be9162c56b3eb561199905235f3e1c7811232b6c9f48ac333651 in /usr/local/bin/ 
# Sat, 30 May 2020 00:20:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 30 May 2020 00:20:26 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:df20fa9351a15782c64e6dddb2d4a6f50bf6d3688060a34c4014b0d9a752eb4c`  
		Last Modified: Fri, 29 May 2020 21:20:06 GMT  
		Size: 2.8 MB (2797541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2af9823da86aecfbe733f68bdcb10ee571e99f640600898d59fefe70da3587e9`  
		Last Modified: Sat, 30 May 2020 00:31:42 GMT  
		Size: 2.9 MB (2940399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeb6f9f404726f8113ee92857acb42c316f96fbf706d3b5fa7c4cee41d8b8391`  
		Last Modified: Sat, 30 May 2020 00:31:41 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bash:devel` - linux; arm variant v6

```console
$ docker pull bash@sha256:62ef22038b423a370127c359d343c9307cc33b7f0c027cdd8b1fc6409bf6a7dc
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5430169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bc6305c03a97ef128f93f858690a3b3eb11b3ca6671b44bccef7b1bd8872898`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 29 May 2020 21:50:55 GMT
ADD file:f46e997a56849423db17e5fc9f0249ab6c73b155245927dba5fcb9dfd65f622f in / 
# Fri, 29 May 2020 21:50:56 GMT
CMD ["/bin/sh"]
# Tue, 09 Jun 2020 21:49:26 GMT
ENV _BASH_COMMIT=ab309487d5c1d7fa1a40e2d6b2e77e413cef4933
# Tue, 09 Jun 2020 21:49:27 GMT
ENV _BASH_COMMIT_DESC=commit bash-20200605 snapshot
# Tue, 09 Jun 2020 21:50:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 	fi; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -r 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .bash-rundeps $runDeps; 	apk del .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version
# Tue, 09 Jun 2020 21:50:43 GMT
COPY file:651b3bebeba8be9162c56b3eb561199905235f3e1c7811232b6c9f48ac333651 in /usr/local/bin/ 
# Tue, 09 Jun 2020 21:50:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jun 2020 21:50:46 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:b4b72e716706d29f5d2351709c20bf737b94f876a5472a43ff1b6e203c65d27f`  
		Last Modified: Fri, 29 May 2020 21:51:30 GMT  
		Size: 2.6 MB (2603286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09ec9e96c286f4e1f2a517ec2dcb3fdaba9e7a9a61096bff43b801186d6132ed`  
		Last Modified: Tue, 09 Jun 2020 21:52:03 GMT  
		Size: 2.8 MB (2826540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d7f1ab8144a3e9f5545fbb5ac9d2c10f5eba2ba693f83d17358e31465e549b6`  
		Last Modified: Tue, 09 Jun 2020 21:52:02 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bash:devel` - linux; arm variant v7

```console
$ docker pull bash@sha256:b41857cb4f65d1a46157efb01c795723d9704e7b71266c1aa8eefe9933a6dea2
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5177836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29c54117b82ceb5058da0d0e92374dc5d44e73d01f8c878f6e41c67c230f40f0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 29 May 2020 21:02:07 GMT
ADD file:e97bf0d217846312b19a9f7264604851aedd125c23b4d291eed4c69b880dce26 in / 
# Fri, 29 May 2020 21:02:08 GMT
CMD ["/bin/sh"]
# Sat, 30 May 2020 00:57:33 GMT
ENV _BASH_COMMIT=37adc8b99d4c15dcb9e6582aa19a2ef61afb592f
# Sat, 30 May 2020 00:57:34 GMT
ENV _BASH_COMMIT_DESC=commit bash-20200527 snapshot
# Sat, 30 May 2020 00:58:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 	fi; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -r 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .bash-rundeps $runDeps; 	apk del .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version
# Sat, 30 May 2020 00:58:34 GMT
COPY file:651b3bebeba8be9162c56b3eb561199905235f3e1c7811232b6c9f48ac333651 in /usr/local/bin/ 
# Sat, 30 May 2020 00:58:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 30 May 2020 00:58:35 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:52278dd8e57993669c5b72a9620e89bebdc098f2af2379caaa8945f7403f77a2`  
		Last Modified: Fri, 29 May 2020 21:02:38 GMT  
		Size: 2.4 MB (2406763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07a9b07b6b895613a83ff46a443699d9eba96ac8f6068cc892931368c46a5ae5`  
		Last Modified: Sat, 30 May 2020 01:13:37 GMT  
		Size: 2.8 MB (2770733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4196e0ec14d542ec52e64c8aacb510a6c906f33ba8832c24e9a2cbb4df70c76`  
		Last Modified: Sat, 30 May 2020 01:13:36 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bash:devel` - linux; arm64 variant v8

```console
$ docker pull bash@sha256:b9edbc0cfce08e801d7138af41abad9c39fd88ff9f6b9736d6fce450bdf40346
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5646569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:277e1ca9646577a3e35498fce224b307543f039035e6e212515a5748f01779b9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 29 May 2020 21:43:19 GMT
ADD file:7574aee4e37a85460ab889212d52912723a9b30dda1c060548f0deb4a05fc398 in / 
# Fri, 29 May 2020 21:43:20 GMT
CMD ["/bin/sh"]
# Sat, 30 May 2020 00:39:42 GMT
ENV _BASH_COMMIT=37adc8b99d4c15dcb9e6582aa19a2ef61afb592f
# Sat, 30 May 2020 00:39:43 GMT
ENV _BASH_COMMIT_DESC=commit bash-20200527 snapshot
# Sat, 30 May 2020 00:40:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 	fi; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -r 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .bash-rundeps $runDeps; 	apk del .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version
# Sat, 30 May 2020 00:40:41 GMT
COPY file:651b3bebeba8be9162c56b3eb561199905235f3e1c7811232b6c9f48ac333651 in /usr/local/bin/ 
# Sat, 30 May 2020 00:40:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 30 May 2020 00:40:43 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:b538f80385f9b48122e3da068c932a96ea5018afa3c7be79da00437414bd18cd`  
		Last Modified: Fri, 29 May 2020 21:43:57 GMT  
		Size: 2.7 MB (2707964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99389cce2b8624eafa1f89945d2647ea570a1a74e16c5c2d4f71956b17430a14`  
		Last Modified: Sat, 30 May 2020 00:54:49 GMT  
		Size: 2.9 MB (2938261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ce091437e6f071efda80d81b56814d654407f56eabe1b9243f07467f807dfa4`  
		Last Modified: Sat, 30 May 2020 00:54:48 GMT  
		Size: 344.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bash:devel` - linux; 386

```console
$ docker pull bash@sha256:31646cd11d79ba2b4a967c11ed2389e3b51760e96b7fb50a8d3fded8e82fd2a2
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5670365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bd38fa570dd6b2ccd3a679b6524948636781536a9cfec5d9e2b84f18fa5ba8c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 29 May 2020 21:38:33 GMT
ADD file:5624441d97aca5eeb82a582941efc3586397098b8391227a9040ebe434cc1d6b in / 
# Fri, 29 May 2020 21:38:33 GMT
CMD ["/bin/sh"]
# Sat, 30 May 2020 00:38:23 GMT
ENV _BASH_COMMIT=37adc8b99d4c15dcb9e6582aa19a2ef61afb592f
# Sat, 30 May 2020 00:38:23 GMT
ENV _BASH_COMMIT_DESC=commit bash-20200527 snapshot
# Sat, 30 May 2020 00:39:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 	fi; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -r 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .bash-rundeps $runDeps; 	apk del .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version
# Sat, 30 May 2020 00:39:25 GMT
COPY file:651b3bebeba8be9162c56b3eb561199905235f3e1c7811232b6c9f48ac333651 in /usr/local/bin/ 
# Sat, 30 May 2020 00:39:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 30 May 2020 00:39:26 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:0625b4155e2a59f647ece47c0cd77ed3196b1f84454fa64ce80cad90e2b9b79e`  
		Last Modified: Fri, 29 May 2020 21:38:53 GMT  
		Size: 2.8 MB (2792298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e54c4154a77e532ea375529824e8425d55f9654c2a85f6ae0961f25f2de85d0c`  
		Last Modified: Sat, 30 May 2020 00:51:49 GMT  
		Size: 2.9 MB (2877726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9f48f34627581ca115e863c2e213640c7d4d680ba4bf4468b7c91f8ffd84107`  
		Last Modified: Sat, 30 May 2020 00:51:49 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bash:devel` - linux; ppc64le

```console
$ docker pull bash@sha256:e015d5f6dba6ec3d85b75e22ed6d4abe26a8b708f2ea7414166f1e8f78a5bcc0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5988184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de250cc4745216aeb978b1f4630182f3cd6d51f57ad9678b7ed7bb16c0c841c5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 29 May 2020 21:23:03 GMT
ADD file:8194808a812370fd2202d80d1667f851bd9eac4c560d69d347fe1964f54343de in / 
# Fri, 29 May 2020 21:23:06 GMT
CMD ["/bin/sh"]
# Sat, 30 May 2020 01:14:19 GMT
ENV _BASH_COMMIT=37adc8b99d4c15dcb9e6582aa19a2ef61afb592f
# Sat, 30 May 2020 01:14:24 GMT
ENV _BASH_COMMIT_DESC=commit bash-20200527 snapshot
# Sat, 30 May 2020 01:15:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 	fi; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -r 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .bash-rundeps $runDeps; 	apk del .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version
# Sat, 30 May 2020 01:15:29 GMT
COPY file:651b3bebeba8be9162c56b3eb561199905235f3e1c7811232b6c9f48ac333651 in /usr/local/bin/ 
# Sat, 30 May 2020 01:15:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 30 May 2020 01:15:34 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:5077f8601dceb5744d875d7740ebc203f674b108a0188f3a31e292b21a4bee64`  
		Last Modified: Fri, 29 May 2020 21:23:37 GMT  
		Size: 2.8 MB (2805199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:985dd55918d55389fa632020186f016097dcbe04f0f7c19dd141816cb0ff77b7`  
		Last Modified: Sat, 30 May 2020 01:32:43 GMT  
		Size: 3.2 MB (3182642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a760788687625f2425552ec56f3c455e006f06fe68c22a955001451aff56dec4`  
		Last Modified: Sat, 30 May 2020 01:32:42 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bash:devel` - linux; s390x

```console
$ docker pull bash@sha256:a66749b45bebe379b9bfb045da140d1272f2f4bfab42d72703968b49407ce304
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5495076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc06cc80dde44b61faccbde3038ed4cc8a33071c10c54589f80ba1b76e692c4a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 29 May 2020 21:41:39 GMT
ADD file:9799ce3b2f782a28e10b1846cd9b3db827fa99c9bc601feb268456195856814e in / 
# Fri, 29 May 2020 21:41:39 GMT
CMD ["/bin/sh"]
# Tue, 09 Jun 2020 21:41:32 GMT
ENV _BASH_COMMIT=ab309487d5c1d7fa1a40e2d6b2e77e413cef4933
# Tue, 09 Jun 2020 21:41:32 GMT
ENV _BASH_COMMIT_DESC=commit bash-20200605 snapshot
# Tue, 09 Jun 2020 21:42:04 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 	fi; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -r 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .bash-rundeps $runDeps; 	apk del .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version
# Tue, 09 Jun 2020 21:42:04 GMT
COPY file:651b3bebeba8be9162c56b3eb561199905235f3e1c7811232b6c9f48ac333651 in /usr/local/bin/ 
# Tue, 09 Jun 2020 21:42:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jun 2020 21:42:04 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:8fb3d41b2e9a59630b51745f257cd2561f96bcd15cf309fcc20120d5fcee8c5b`  
		Last Modified: Fri, 29 May 2020 21:42:03 GMT  
		Size: 2.6 MB (2566189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f3b5ad91814a5cea029327b31732fed9d2c0e42317cf3c454991019a358a6df`  
		Last Modified: Tue, 09 Jun 2020 21:43:00 GMT  
		Size: 2.9 MB (2928551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:116edebf8e44856265c01e689307e2896639fd7239e63ecfa6318545f19328fc`  
		Last Modified: Tue, 09 Jun 2020 21:43:05 GMT  
		Size: 336.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
