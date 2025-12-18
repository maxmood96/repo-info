## `bash:devel-20251205-alpine3.23`

```console
$ docker pull bash@sha256:03a5570d539146759cf404f198789ea2d18a419f343515ca9ff5d5ef5eba50e4
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

### `bash:devel-20251205-alpine3.23` - linux; amd64

```console
$ docker pull bash@sha256:61281b4bdbf13f87104877b7841c7ee6345752fcea3256e87c4b8f26c82422f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6867731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e9ed757f0b836929bd1017baecd928ab06b8e6ea424084187f3da15a4d5bf52`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:28:29 GMT
ENV _BASH_COMMIT=f27bf94a7927219f96e97e1a21f2ade9dd439a3e
# Thu, 18 Dec 2025 00:28:29 GMT
ENV _BASH_VERSION=devel-20251205
# Thu, 18 Dec 2025 00:28:29 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Thu, 18 Dec 2025 00:29:02 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Thu, 18 Dec 2025 00:29:02 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:29:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:29:02 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:49:00 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31b8539e7a3b182278cf274fe1f2f74fc3bc3859a29d5ea34c57ba28e142e19a`  
		Last Modified: Thu, 18 Dec 2025 00:29:13 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a85986e8c2436a6fe550d346bbc3b2ec3e314cb1f554a0a7db03feb3366f28fd`  
		Last Modified: Thu, 18 Dec 2025 00:29:13 GMT  
		Size: 3.0 MB (3006834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fbc96fe5aeea04a88197aba52c478d506dae1666063dec853bd39d9df05819f`  
		Last Modified: Thu, 18 Dec 2025 00:29:13 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20251205-alpine3.23` - unknown; unknown

```console
$ docker pull bash@sha256:20264af64c35e205c732207996b6ffebc8a649d5b67ff7d25381a590570ecf7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.1 KB (135054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8bc8dc23806886b5090c8579fb0eb71e58005b33813d7b2fc053541299ed0c3`

```dockerfile
```

-	Layers:
	-	`sha256:96736717bf80b5bcd3fd97d45c7554a220b9649225f43d5f5408c7bd1f956133`  
		Last Modified: Thu, 18 Dec 2025 04:03:26 GMT  
		Size: 117.1 KB (117122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2754d7494a17702626abb54829cbba3bea4bfb96f37cf84be35925e285f7cdc`  
		Last Modified: Thu, 18 Dec 2025 04:03:27 GMT  
		Size: 17.9 KB (17932 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20251205-alpine3.23` - linux; arm variant v6

```console
$ docker pull bash@sha256:e5bb03a21e6e02d5d24e587572b700428b47c14f41a203933472a729d40e505d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6537905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61e9f8b0a744b69fc157f043beea8d6ec98afee4397d91c7192fa663c59dde32`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:27:21 GMT
ENV _BASH_COMMIT=f27bf94a7927219f96e97e1a21f2ade9dd439a3e
# Thu, 18 Dec 2025 00:27:21 GMT
ENV _BASH_VERSION=devel-20251205
# Thu, 18 Dec 2025 00:27:21 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Thu, 18 Dec 2025 00:28:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Thu, 18 Dec 2025 00:28:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:28:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:28:06 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:27 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd28231d6c72fb70763a92ea2a30ed33a0023f8ab94e5f79277360984c74b6ba`  
		Last Modified: Thu, 18 Dec 2025 00:28:15 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aaec30b0ff41ac1e3f1f387b80d373cd4e7baa39e6e60b36b2add5c56b038b0`  
		Last Modified: Thu, 18 Dec 2025 00:28:15 GMT  
		Size: 3.0 MB (2968682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31e1792dadbe7f3aaf035d60a1e83cdbbcf72a6201c1734b022ad26017b10513`  
		Last Modified: Thu, 18 Dec 2025 00:28:15 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20251205-alpine3.23` - unknown; unknown

```console
$ docker pull bash@sha256:c03c64314c087ac0b457a971ed4424c1d0f32f03e06c6c6e3e4be170f78829af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 KB (17797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8df2fb40617f0ae1db404be1a9beffeca9c3cf2b4851d168bc6039b61b8690a`

```dockerfile
```

-	Layers:
	-	`sha256:443310fedf5175d745a904f69a8648693cf575ee5405bbb6d96d98d23dec0148`  
		Last Modified: Thu, 18 Dec 2025 04:03:30 GMT  
		Size: 17.8 KB (17797 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20251205-alpine3.23` - linux; arm variant v7

```console
$ docker pull bash@sha256:6a4a2105fba99d933f0d63ffac418d1f10a7d50f830f0a0df14abbb0588650dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6198248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53743fd672394308fae964067a47dbde426e23c3520b2313d38667194cb2b5c4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:23 GMT
ADD alpine-minirootfs-3.23.2-armv7.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:23 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:27:54 GMT
ENV _BASH_COMMIT=f27bf94a7927219f96e97e1a21f2ade9dd439a3e
# Thu, 18 Dec 2025 00:27:54 GMT
ENV _BASH_VERSION=devel-20251205
# Thu, 18 Dec 2025 00:27:54 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Thu, 18 Dec 2025 00:28:36 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Thu, 18 Dec 2025 00:28:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:28:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:28:36 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:fb78f26011a0b45e0ee3135541eee4683a4b98bf30b3d23f0981be37e8794a2a`  
		Last Modified: Thu, 18 Dec 2025 00:12:43 GMT  
		Size: 3.3 MB (3279388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c078e62c71f2014c5f9b066cb2543e57566bfd7883a7159763740c1400f7cb9b`  
		Last Modified: Thu, 18 Dec 2025 00:28:49 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cadfa99c6e30ad7b8ea294b910b89380a7882a706fcc898f657fbdb881da5f2`  
		Last Modified: Thu, 18 Dec 2025 00:28:50 GMT  
		Size: 2.9 MB (2918072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c293a2d80a45d173deee312fdfcb774d7b86d9d3e784235ff7b664a58fcd2825`  
		Last Modified: Thu, 18 Dec 2025 00:28:50 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20251205-alpine3.23` - unknown; unknown

```console
$ docker pull bash@sha256:d4e8c23ff4f7ec7d56eff962db8a5bcb1a813ac54e0cf0755f3ab4dbcba92ed7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.5 KB (134520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe099d166286b366004397100ade8acf27dfc3da97dc6c9325502aa6c25cf2d8`

```dockerfile
```

-	Layers:
	-	`sha256:ad61acab2fd0ebe7f1f79a8ae2e27d5af7b4db763dc50feedf2f1ebed48b464a`  
		Last Modified: Thu, 18 Dec 2025 04:03:33 GMT  
		Size: 116.5 KB (116508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4fe6d3cef8dcc536ad8080c0b3719e64ffd9d8abce8505a691f16208cb88e26b`  
		Last Modified: Thu, 18 Dec 2025 04:03:34 GMT  
		Size: 18.0 KB (18012 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20251205-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull bash@sha256:ee5cab4ff2b57f4712895a5e00dd7c171514d76f2d9a53db837ff6bf90744398
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7271818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bca09c3f67f963ced02434280e35761e98f6ff893b18d67b9fee63add8d3187`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:27:47 GMT
ENV _BASH_COMMIT=f27bf94a7927219f96e97e1a21f2ade9dd439a3e
# Thu, 18 Dec 2025 00:27:47 GMT
ENV _BASH_VERSION=devel-20251205
# Thu, 18 Dec 2025 00:27:47 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Thu, 18 Dec 2025 00:28:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Thu, 18 Dec 2025 00:28:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:28:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:28:27 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:50 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b495fd7249a186968ab4148e41136b3289013486b6f0e7266fe8833e7c9c2cb1`  
		Last Modified: Thu, 18 Dec 2025 00:28:38 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0e418d094f6b64547b9d85053f9611ce0bb5e3c5806e6a38baf25f178497cd2`  
		Last Modified: Thu, 18 Dec 2025 00:28:38 GMT  
		Size: 3.1 MB (3075289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10424f50f1699c6d61b3cc3d6121e86be95ec58340c0935a916f92784978f475`  
		Last Modified: Thu, 18 Dec 2025 00:28:38 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20251205-alpine3.23` - unknown; unknown

```console
$ docker pull bash@sha256:22674afd308acb41ae7c20719ea90ed8c78ac7fddee93896bfb7afce04b8a291
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.6 KB (134563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5117f17ef9521c72eb9337b70ad7119b0bcbb9755d74a0c15d4bab3eee57116e`

```dockerfile
```

-	Layers:
	-	`sha256:6ea7b824c2e45872b3feb8bcbe0ab6d4bc6c6ef06041893505a96d2a2da21fdd`  
		Last Modified: Thu, 18 Dec 2025 04:03:37 GMT  
		Size: 116.5 KB (116528 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79d0c89513975cb1d048b75c3de43b48473fbf3b24ace5f7c1129a3a4d8ce3d6`  
		Last Modified: Thu, 18 Dec 2025 04:03:38 GMT  
		Size: 18.0 KB (18035 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20251205-alpine3.23` - linux; 386

```console
$ docker pull bash@sha256:c949cf3b90633f4bfc232edbba2e942ff2d6c67989b0a55572a414f7cf5bab49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6623859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6240026b5344c0c34d43367f68bbbdef9c1521530d5411b9335e790f8fd54d3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 18 Dec 2025 00:13:19 GMT
ADD alpine-minirootfs-3.23.2-x86.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:13:19 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:26:30 GMT
ENV _BASH_COMMIT=f27bf94a7927219f96e97e1a21f2ade9dd439a3e
# Thu, 18 Dec 2025 00:26:30 GMT
ENV _BASH_VERSION=devel-20251205
# Thu, 18 Dec 2025 00:26:30 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Thu, 18 Dec 2025 00:27:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Thu, 18 Dec 2025 00:27:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:27:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:27:06 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:c21df6a7383dfce37a4bfe31b291881f55907c419caf5d06cb6d699d290d0718`  
		Last Modified: Thu, 18 Dec 2025 00:13:38 GMT  
		Size: 3.7 MB (3686100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a79e2ac8876236fb1de42a88eaa0b332bfae0e3e680805dd9a9cc63c97278563`  
		Last Modified: Thu, 18 Dec 2025 00:27:19 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31b1860cb57d79b5f2228d4acc2fc1ddce1d2fca09efb13f7155e486364b67ad`  
		Last Modified: Thu, 18 Dec 2025 00:27:19 GMT  
		Size: 2.9 MB (2936970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4852e9a2c38fec98b05c7c8dbe7fa28357dbd3cb444d109ab6226c04033db933`  
		Last Modified: Thu, 18 Dec 2025 00:27:19 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20251205-alpine3.23` - unknown; unknown

```console
$ docker pull bash@sha256:4ec385848690c92b0cc5c444e6d279aab74455b36111867d932d18866234bea2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.0 KB (134997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a22f2f9dabd6f116dd0d7d1bc5a3314379066f5e0f9ef605a9997a5fc2ad218`

```dockerfile
```

-	Layers:
	-	`sha256:f4f509b623519a1c88522e4f1b4899639eeb8677c488fc32f6e71badf65420a8`  
		Last Modified: Thu, 18 Dec 2025 04:03:41 GMT  
		Size: 117.1 KB (117097 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4e83ba71d4e611f2b53214327fa315d66e760fa2f7b1e9de8c3f0505aa16c75`  
		Last Modified: Thu, 18 Dec 2025 04:03:42 GMT  
		Size: 17.9 KB (17900 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20251205-alpine3.23` - linux; ppc64le

```console
$ docker pull bash@sha256:47a52c4a36e6e4719c4e6df5224a7df381629aa37e33a59a8bd49410550bb1a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7139833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:812492a85f95641476b2e31919afc142b77c0b652324af14994ec3d5bea0af1c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:34 GMT
ADD alpine-minirootfs-3.23.2-ppc64le.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:34 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:25:58 GMT
ENV _BASH_COMMIT=f27bf94a7927219f96e97e1a21f2ade9dd439a3e
# Thu, 18 Dec 2025 00:25:58 GMT
ENV _BASH_VERSION=devel-20251205
# Thu, 18 Dec 2025 00:25:58 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Thu, 18 Dec 2025 00:26:57 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Thu, 18 Dec 2025 00:26:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:26:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:26:57 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:2dbbc2b20d556edcc853ddf744c4b2e946f16fba62ed0f0c4526533fdaa56e3b`  
		Last Modified: Thu, 18 Dec 2025 00:11:57 GMT  
		Size: 3.8 MB (3827755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf056449837c26e20456ec1de3d317628e37795775a4fe3956dc4871707fcd71`  
		Last Modified: Thu, 18 Dec 2025 00:27:20 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8d123f11cef3febfe2bbc7c58dbc632044bbd8464b5169c076a79622ee79b59`  
		Last Modified: Thu, 18 Dec 2025 00:27:20 GMT  
		Size: 3.3 MB (3311289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2549ed5d4de4022084268e455b9667d7a56f53f036f20d919ce13f30e1d8677e`  
		Last Modified: Thu, 18 Dec 2025 00:27:20 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20251205-alpine3.23` - unknown; unknown

```console
$ docker pull bash@sha256:fcce29d180b275348aa040f542123eaab40847b53c23d305cf9e3b10e847ab51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.5 KB (134481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22e8a4c46d2f7c346549a12bb7e70d789c3f6e9e4553749700534ba58d17cdcd`

```dockerfile
```

-	Layers:
	-	`sha256:d965cfdf1c8915a475cd5fb8b162f713ff76032f96da5e15f8d8e06e567c7316`  
		Last Modified: Thu, 18 Dec 2025 04:03:45 GMT  
		Size: 116.5 KB (116505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b232669c4732eb9fbc2738b483471eea46188ecaad4254ea52acacb863da6701`  
		Last Modified: Thu, 18 Dec 2025 04:03:46 GMT  
		Size: 18.0 KB (17976 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20251205-alpine3.23` - linux; riscv64

```console
$ docker pull bash@sha256:f7d8383083005e1394480820b3baf83e45d73bfb585f3fa7c4f49b4740e2689b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6782974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9464a6f4d846598458b2135ae5777318a8b11973e34db7d867f5bd4513b158e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:39 GMT
ADD alpine-minirootfs-3.23.0-riscv64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:39 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 23:38:08 GMT
ENV _BASH_COMMIT=f27bf94a7927219f96e97e1a21f2ade9dd439a3e
# Thu, 04 Dec 2025 23:38:08 GMT
ENV _BASH_VERSION=devel-20251205
# Thu, 04 Dec 2025 23:38:08 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Wed, 10 Dec 2025 17:12:23 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Wed, 10 Dec 2025 17:12:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Dec 2025 17:12:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Dec 2025 17:12:23 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:9929557817a4c85b33d6dbeb491f7396ef32added7e77de7ac1b644ed0975313`  
		Last Modified: Wed, 03 Dec 2025 19:30:17 GMT  
		Size: 3.6 MB (3583519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18bbd5abf1031a6f93d3da3bfe7f9bf20c042cf462c6210011f353d874cf8771`  
		Last Modified: Thu, 04 Dec 2025 23:47:28 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5c17981ac70d1ee478787aece2f43c1d972951a92131d20568a08825dd5d830`  
		Last Modified: Wed, 10 Dec 2025 17:13:01 GMT  
		Size: 3.2 MB (3198662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4881ddd9de4d40ae318ead7b66231ceeab8b497d5aed4ead91debfc546d72fbd`  
		Last Modified: Wed, 10 Dec 2025 17:13:01 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20251205-alpine3.23` - unknown; unknown

```console
$ docker pull bash@sha256:1a02246da88e475761b84e20efa1592a694dc23bdfcf373202f3f6f7a9fa29e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.5 KB (134476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23bdbec96731c5911ca9b08d946403abd437f960f74544825110630424d3d2f6`

```dockerfile
```

-	Layers:
	-	`sha256:6379c5720f303f2bf995df2ec9aed5c52405b329601e6f1ee62782700cd7dbd5`  
		Last Modified: Wed, 10 Dec 2025 19:03:01 GMT  
		Size: 116.5 KB (116501 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9e9eb2d23065ab9f72f6677e28840daac0301c1044070a6dabb837a05a9ad35`  
		Last Modified: Wed, 10 Dec 2025 19:03:02 GMT  
		Size: 18.0 KB (17975 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20251205-alpine3.23` - linux; s390x

```console
$ docker pull bash@sha256:acdba2ebcfa1444a8a8e7840f0c9b18d6ec0ac075957d1a4063d1643b571883b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6822854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40536422eed2d20049f8bfd2e4ca7383727d278ffbf0aee8895c085d0f9673eb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:56 GMT
ADD alpine-minirootfs-3.23.2-s390x.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:56 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:26:06 GMT
ENV _BASH_COMMIT=f27bf94a7927219f96e97e1a21f2ade9dd439a3e
# Thu, 18 Dec 2025 00:26:06 GMT
ENV _BASH_VERSION=devel-20251205
# Thu, 18 Dec 2025 00:26:06 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Thu, 18 Dec 2025 00:26:56 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Thu, 18 Dec 2025 00:26:56 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:26:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:26:56 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:3d8fe54ac4e72ef775998241dc95a39f582dbddd5cf822b793130a331db6726f`  
		Last Modified: Thu, 18 Dec 2025 00:12:18 GMT  
		Size: 3.7 MB (3724311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74850a391a16eeee8ef302a64bd78c66b478afe49d8a2b62f922f56037b9d4dd`  
		Last Modified: Thu, 18 Dec 2025 00:27:14 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17563f43cd13eea19c56789178a6e6c5bb1f2e9bc70a5b2f482f85f3b224dd28`  
		Last Modified: Thu, 18 Dec 2025 00:27:15 GMT  
		Size: 3.1 MB (3097755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4df0dbe9376167060bda79614979d87fe76103a346d3ff22a9dfc248b586669a`  
		Last Modified: Thu, 18 Dec 2025 00:27:15 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20251205-alpine3.23` - unknown; unknown

```console
$ docker pull bash@sha256:717256d62f6862e817520124735aac8f4d8249a8a41715ca6d01a3f72707769d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.4 KB (134403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4d5149c31f7e9eb7b617bf55b6d72395314109b90a379b17487ae59c0e8f435`

```dockerfile
```

-	Layers:
	-	`sha256:34b94704e00f8699da0489b790b9d66639b8299e10a1c36f185a6793274e11d7`  
		Last Modified: Thu, 18 Dec 2025 04:03:52 GMT  
		Size: 116.5 KB (116471 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31b22f6ce26241256e0e90434b9748fc9265f492db187b347ed092aa78d466b4`  
		Last Modified: Thu, 18 Dec 2025 04:03:53 GMT  
		Size: 17.9 KB (17932 bytes)  
		MIME: application/vnd.in-toto+json
