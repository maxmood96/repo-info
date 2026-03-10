## `bash:devel`

```console
$ docker pull bash@sha256:d3bea3f2f7393b52432461b52dd807cd3818969670d7e8e505c22fab7685698e
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
$ docker pull bash@sha256:73f2ac0d1932f83d0fd54d85dc655a1b5c23544dc983c6a4f5ee7a3f0b70c17f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6890359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a0c96a4fadba47e197c40621f972e1b8551a9ed14fd5906b5432214b77278d6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Tue, 10 Mar 2026 19:11:37 GMT
ENV _BASH_COMMIT=1f292e433e2e51184c15d8f71b4d9daf1104d3e7
# Tue, 10 Mar 2026 19:11:37 GMT
ENV _BASH_VERSION=devel-20260309
# Tue, 10 Mar 2026 19:11:37 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 10 Mar 2026 19:12:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 10 Mar 2026 19:12:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 10 Mar 2026 19:12:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Mar 2026 19:12:12 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc2427aec123ef4f041373d1ddfda8239b2ead4fd47fdd84e3f5c1af60edc2b8`  
		Last Modified: Tue, 10 Mar 2026 19:12:17 GMT  
		Size: 458.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4efd5d747cf8e9e65742ae84a301cf9abf1650a9fa915beb47d91e890a94551b`  
		Last Modified: Tue, 10 Mar 2026 19:12:17 GMT  
		Size: 3.0 MB (3027748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d2cc9bd62f60e91fcaf270462289798b1fe03fb5fa165338a260287b22a08e7`  
		Last Modified: Tue, 10 Mar 2026 19:12:16 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:63241c889bff992a4eb0303290de40f9a7cfa34aee6414b8938cc014aeb844f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.3 KB (135306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a95639995304bb66b7b173842b9c678ca08b410b3147d729243e4056ad5c50e4`

```dockerfile
```

-	Layers:
	-	`sha256:22457117930847fcf449efc3810e489acbe1d40675e09043c5967c58944b108c`  
		Last Modified: Tue, 10 Mar 2026 19:12:16 GMT  
		Size: 117.1 KB (117122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13ef2dd65fd49038fa15dc8b6db395e788df4119e6d2af4ade6f8d58570e7066`  
		Last Modified: Tue, 10 Mar 2026 19:12:16 GMT  
		Size: 18.2 KB (18184 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; arm variant v6

```console
$ docker pull bash@sha256:c57218b1f1f5b81a8e05f6d5246868b669d939e7c12e381838e6c31af5026369
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6556774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76d3eaf05154c37e9d8c7deb2df813b5375d969d3c643691b13978c1b62ec3fa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Tue, 24 Feb 2026 21:27:32 GMT
ENV _BASH_COMMIT=044c1acc91df168c9e9f1379b9a1ecc75d395bd3
# Tue, 24 Feb 2026 21:27:32 GMT
ENV _BASH_VERSION=devel-20260217
# Tue, 24 Feb 2026 21:27:32 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 24 Feb 2026 21:28:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 24 Feb 2026 21:28:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 21:28:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 21:28:16 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e00ce10d8d9dd1370d656f155a8540f43830b1e5e7ec66670ccb4b8cafd3e7d8`  
		Last Modified: Tue, 24 Feb 2026 21:28:20 GMT  
		Size: 460.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcb2f49c0f646f2c75c0f7a9fe5274d9ae9899cba22fe77a1f88181fece0b823`  
		Last Modified: Tue, 24 Feb 2026 21:28:20 GMT  
		Size: 3.0 MB (2986161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f401096504bfda49850e4c5488c45c9b0c4bca83f90c8b338cbb9385d34615bc`  
		Last Modified: Tue, 24 Feb 2026 21:28:20 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:bb87e018d4d9beff84731b0aad7218a9d12dd5defb962a58257ac589e0a130dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (18049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd66d5ebfab3e071dc914c56d94f3cc828ee5c1f876961e1e30bc6177289bbe7`

```dockerfile
```

-	Layers:
	-	`sha256:2c42d25fd9b15905b065f2a554e77e0678183a845e26ec7a279751a6040f42de`  
		Last Modified: Tue, 24 Feb 2026 21:28:20 GMT  
		Size: 18.0 KB (18049 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; arm variant v7

```console
$ docker pull bash@sha256:c54d80c23b57093ff8fafa61f8f3d7dcd13472f0573e4a6d7e13cd2f206de62b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6219322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96f8ceef1daa10f8f93de24c4a9eeb1cf2090795852e0103aa158b94144e6fd1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Tue, 10 Mar 2026 19:11:40 GMT
ENV _BASH_COMMIT=1f292e433e2e51184c15d8f71b4d9daf1104d3e7
# Tue, 10 Mar 2026 19:11:40 GMT
ENV _BASH_VERSION=devel-20260309
# Tue, 10 Mar 2026 19:11:40 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 10 Mar 2026 19:12:23 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 10 Mar 2026 19:12:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 10 Mar 2026 19:12:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Mar 2026 19:12:23 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93115ebb97ceaa30d1a78e1c69b0d7fd804a8c22b34c51e826c9dce4eaa92745`  
		Last Modified: Tue, 10 Mar 2026 19:12:26 GMT  
		Size: 458.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:106b5b83dec3ef8efdf1c4fe1e2bbf318b1a6ae04bb235f296c6ad26fdd0f65a`  
		Last Modified: Tue, 10 Mar 2026 19:12:28 GMT  
		Size: 2.9 MB (2936806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e50d4c878b82e1ad222de593a229537500df5ff4e2ab11907b3267ff4ed0202`  
		Last Modified: Tue, 10 Mar 2026 19:12:28 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:dbd691c64bd11f79845e06e90b579348d2c655a07a4aae528853f623e59a4c70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.8 KB (134771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bdf521ddae32bf08ede01cda88a87bc9aff8968c7250f72dcc0d9c22c221e22`

```dockerfile
```

-	Layers:
	-	`sha256:9e50a1546f1106ded2f90055e8a304b03cff12908028c5e48b1fa7392362bf30`  
		Last Modified: Tue, 10 Mar 2026 19:12:28 GMT  
		Size: 116.5 KB (116508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:855f97de4433250c071b2d3073042bb6666c78726433156f23e8f8052961f647`  
		Last Modified: Tue, 10 Mar 2026 19:12:28 GMT  
		Size: 18.3 KB (18263 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; arm64 variant v8

```console
$ docker pull bash@sha256:7ded7008c3414f2d1182b1fb95e241458357fac647d2055c3720a3a448133504
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7295617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1f31fe5f92d5566a1a33c258109a71d8ff260948cb5b6f3b0265a0d0b567f05`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Tue, 10 Mar 2026 19:11:40 GMT
ENV _BASH_COMMIT=1f292e433e2e51184c15d8f71b4d9daf1104d3e7
# Tue, 10 Mar 2026 19:11:40 GMT
ENV _BASH_VERSION=devel-20260309
# Tue, 10 Mar 2026 19:11:40 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 10 Mar 2026 19:12:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 10 Mar 2026 19:12:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 10 Mar 2026 19:12:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Mar 2026 19:12:21 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93115ebb97ceaa30d1a78e1c69b0d7fd804a8c22b34c51e826c9dce4eaa92745`  
		Last Modified: Tue, 10 Mar 2026 19:12:26 GMT  
		Size: 458.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eba7a614fb4fe3b009b664d5ef1e236a7a0fcaa83486164cc0181442706d722`  
		Last Modified: Tue, 10 Mar 2026 19:12:26 GMT  
		Size: 3.1 MB (3097734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36d18e74ce9fc7e0a2a7b5adf845d9026faf5f4e9123a781f8e84de9e295ee5e`  
		Last Modified: Tue, 10 Mar 2026 19:12:26 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:3a8ae8a0e6f8ef4f04475587820f992f794b4516a4084adfa0eff610e49b768f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.8 KB (134816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a62496759d49a09477a76137c3e13a0d4eab103f99f9b696c02a746626d515b`

```dockerfile
```

-	Layers:
	-	`sha256:4b24c8c3fc7e6949e82427213b788f6a608c60ddeb754e0476ed898a18554b71`  
		Last Modified: Tue, 10 Mar 2026 19:12:26 GMT  
		Size: 116.5 KB (116528 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0bad9855ec0e9c75b3dd853157c4e2e729db0f2698e90d7d37cf6f36992e1fc5`  
		Last Modified: Tue, 10 Mar 2026 19:12:26 GMT  
		Size: 18.3 KB (18288 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; 386

```console
$ docker pull bash@sha256:b9246b852534aae10a396305f39bb92c775b5a594fde4d23f809a5a6ca5379f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6642295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e332b0a913293d17ebce6912eb8e604511a4a67d7a5283ec576eb029bfb2cda`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:11 GMT
ADD alpine-minirootfs-3.23.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:11 GMT
CMD ["/bin/sh"]
# Tue, 10 Mar 2026 19:14:39 GMT
ENV _BASH_COMMIT=1f292e433e2e51184c15d8f71b4d9daf1104d3e7
# Tue, 10 Mar 2026 19:14:39 GMT
ENV _BASH_VERSION=devel-20260309
# Tue, 10 Mar 2026 19:14:39 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 10 Mar 2026 19:15:36 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 10 Mar 2026 19:15:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 10 Mar 2026 19:15:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Mar 2026 19:15:36 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:18bdec7eea78464ecf9b88f4ec630eaeb694ea1c0101ecd9c20eda20c9065e23`  
		Last Modified: Wed, 28 Jan 2026 01:18:16 GMT  
		Size: 3.7 MB (3686998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78b2da464a382b193b087984909fcf87723113421e2adf0fd6a81a3ff3e2be6c`  
		Last Modified: Tue, 10 Mar 2026 19:15:41 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40f16e76b5a32b5ae76cce3cad6794805886774e0822fcb11c796a394d561338`  
		Last Modified: Tue, 10 Mar 2026 19:15:41 GMT  
		Size: 3.0 MB (2954505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59f4210c45241c1f78da2775733998ff0ea9a399bd8ad82c205711cb2c224f0e`  
		Last Modified: Tue, 10 Mar 2026 19:15:41 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:a6068c0dc0f718365eae088ae79192259de3fb3b850dadd01bdb246f712e47fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.2 KB (135249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9e4bc7f953d00d3959e4e21cf6d2fea2115b3a07db714d1cc549380bde0f7b1`

```dockerfile
```

-	Layers:
	-	`sha256:0a2f8d2ec3e66132960832b861ae91e7fde4beb707cc60e03a5061cb737897f5`  
		Last Modified: Tue, 10 Mar 2026 19:15:41 GMT  
		Size: 117.1 KB (117097 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:125cf7446cfc2c928e250721bfbb2883bc225bcbb819c345f94b81582345dd61`  
		Last Modified: Tue, 10 Mar 2026 19:15:41 GMT  
		Size: 18.2 KB (18152 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; ppc64le

```console
$ docker pull bash@sha256:b64bd22f056aedb1987df51e6d8a08e0cbbeed73008e08b5b337a22073bae1a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7168767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:991aed4eff7be3d2aa9fc823267e364f5e740f2ecfcb1d819117d2068d49c72d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Tue, 10 Mar 2026 19:13:21 GMT
ENV _BASH_COMMIT=1f292e433e2e51184c15d8f71b4d9daf1104d3e7
# Tue, 10 Mar 2026 19:13:21 GMT
ENV _BASH_VERSION=devel-20260309
# Tue, 10 Mar 2026 19:13:21 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 10 Mar 2026 19:14:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 10 Mar 2026 19:14:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 10 Mar 2026 19:14:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Mar 2026 19:14:24 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:921ce0d0e06eca1a82f8447087069eca1ad81556e16858a172e69b5ed75d0fbd`  
		Last Modified: Tue, 10 Mar 2026 19:14:35 GMT  
		Size: 459.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:509dc6d9edcab951261ce88b9c4e6a9fd475c0c662527188508db4991aee9c05`  
		Last Modified: Tue, 10 Mar 2026 19:14:36 GMT  
		Size: 3.3 MB (3338329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be4d8738b00064e9d7ea51ea08f454c1ecdaf910172be3ba86ca66d9fe4b9a6c`  
		Last Modified: Tue, 10 Mar 2026 19:14:35 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:982f6678567aa5f1e9110c1fd76a5dbcb6ced730b6299f5f8716ed35769a1e4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 KB (134732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2040c528d07439abf34071bdfbf57d34b8450e2e3bfa3b1a9e1c073ec1fb476`

```dockerfile
```

-	Layers:
	-	`sha256:0bbb76bcef5d74619190b05a7e7c99d6d7fe95c8ce134f4ed7c439ebfc2e2225`  
		Last Modified: Tue, 10 Mar 2026 19:14:35 GMT  
		Size: 116.5 KB (116505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:355c97a64347b1d0d5e7bae7f71679e3b005b2ac1dda0860f6c54df064a5d618`  
		Last Modified: Tue, 10 Mar 2026 19:14:35 GMT  
		Size: 18.2 KB (18227 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; riscv64

```console
$ docker pull bash@sha256:056420e9a697a4fd9551ecc61e96ae6f0b919c4a47d33dc9774b1e64dabfc476
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6803711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a758aa51a9b458ec8e1754df38fd28fde8fd53a5fe777cabcb046898706b573a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Tue, 24 Feb 2026 20:36:08 GMT
ENV _BASH_COMMIT=044c1acc91df168c9e9f1379b9a1ecc75d395bd3
# Tue, 24 Feb 2026 20:36:08 GMT
ENV _BASH_VERSION=devel-20260217
# Tue, 24 Feb 2026 20:36:08 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 24 Feb 2026 20:45:02 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 24 Feb 2026 20:45:02 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 20:45:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 20:45:02 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f417a7be3c146d2c42c666ab79c82849f3b8de40d74e1a66ce079a295ea58858`  
		Last Modified: Tue, 24 Feb 2026 20:45:28 GMT  
		Size: 459.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31f5ea7f8cd79d7cb81dcb38161255558d4599a68b2d23b9bd873a5cb02bfbc3`  
		Last Modified: Tue, 24 Feb 2026 20:45:28 GMT  
		Size: 3.2 MB (3217625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1be71355d5852ea8aa4857ba654c52b7f608ab2b2aad158bce6002c925335434`  
		Last Modified: Tue, 24 Feb 2026 20:45:28 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:a92756daf2f384ea6c1132bdefcc6eaf5cabc3fe49a9e31da41a1b3251290a44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 KB (134729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0824162ff98ee7ce36eddb2b1956b914155df602ba78e40ab9125fad7d15867`

```dockerfile
```

-	Layers:
	-	`sha256:4983363b36050df200b1f3ee6a888d6a64b3e8fcfff88b5ac2ee55057ac38cc0`  
		Last Modified: Tue, 24 Feb 2026 20:45:28 GMT  
		Size: 116.5 KB (116501 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0365a393e9c5fdbdcc5baac74699337dbca17746205846d361374ffb454bc95d`  
		Last Modified: Tue, 24 Feb 2026 20:45:28 GMT  
		Size: 18.2 KB (18228 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; s390x

```console
$ docker pull bash@sha256:39b3213f51282e2d018e0f175f5ecdf10e4845c5b31369ffbc0b9f974a08e714
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6845923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9f24374baebf7344d903fb9cc983b207d633e74e1f2548e6cfc1a40832faf1a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Tue, 10 Mar 2026 19:12:10 GMT
ENV _BASH_COMMIT=1f292e433e2e51184c15d8f71b4d9daf1104d3e7
# Tue, 10 Mar 2026 19:12:10 GMT
ENV _BASH_VERSION=devel-20260309
# Tue, 10 Mar 2026 19:12:10 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 10 Mar 2026 19:12:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 10 Mar 2026 19:12:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 10 Mar 2026 19:12:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Mar 2026 19:12:55 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0973a61eca6ef7b98bf9efdf2b0974cbe5608b5e0a60f6c019bcf64898e69cc8`  
		Last Modified: Tue, 10 Mar 2026 19:13:05 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a15644d5078c95038abcaaab8d560904330d8b370c9073568a347d39112fec88`  
		Last Modified: Tue, 10 Mar 2026 19:13:05 GMT  
		Size: 3.1 MB (3119801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfa437a0ee2428e389b23e63034c15c03cdd89b95048cc35538024aef988f168`  
		Last Modified: Tue, 10 Mar 2026 19:13:05 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:db73285d0ec97bda08edc5b9086418b221b4aeceed5037769e15fc67656a01da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 KB (134653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eff9e0e2b8d175a4c83b12ca4cd20365345b94765c16ff373a4549a56a33f924`

```dockerfile
```

-	Layers:
	-	`sha256:a18829386a4f2e9dc345d328312e720907bdc38986952b12994d48c94c178322`  
		Last Modified: Tue, 10 Mar 2026 19:13:05 GMT  
		Size: 116.5 KB (116471 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:249936493ee34bce125cc67b0889dfaa46403f71457b77276e4fa6521509544a`  
		Last Modified: Tue, 10 Mar 2026 19:13:05 GMT  
		Size: 18.2 KB (18182 bytes)  
		MIME: application/vnd.in-toto+json
