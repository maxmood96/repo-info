## `bash:devel-20260608-alpine3.24`

```console
$ docker pull bash@sha256:f29e82395d1856447fce46bedfe0dc8ee77a210aa834148390f52f4299211f81
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

### `bash:devel-20260608-alpine3.24` - linux; amd64

```console
$ docker pull bash@sha256:8d569199bcd406c7ff03ac1658bd1c41223ac727ac2ae9a64c3e463c1bb01550
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6887594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:766bc260b082571451429f6791f17d6e3a6cb97aa7808a47ff10c93d7f7274da`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:29 GMT
ADD alpine-minirootfs-3.24.1-x86_64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:29 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:10:23 GMT
ENV _BASH_COMMIT=8085ee139645391bb392cc06dd25717238b65455
# Tue, 16 Jun 2026 00:10:23 GMT
ENV _BASH_VERSION=devel-20260608
# Tue, 16 Jun 2026 00:10:23 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 16 Jun 2026 00:11:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 16 Jun 2026 00:11:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:11:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 00:11:01 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:55afa1ecc21d2bb5e5045f32dafee56272ffd89860bac26f6c32123439af26a4`  
		Last Modified: Sun, 14 Jun 2026 06:44:06 GMT  
		Size: 3.8 MB (3846391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c2be0e6f3b7549ad60643802d3dc938aa1c6a2f4bd5f57bb1a4ddfcf636a053`  
		Last Modified: Tue, 16 Jun 2026 00:11:06 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:227f16e4aeb9918e327825da03e23cdd0b4fff70b360442a99af37741205edcc`  
		Last Modified: Tue, 16 Jun 2026 00:11:06 GMT  
		Size: 3.0 MB (3040415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df3df0743a1325125dda5fb65d8a3e9f2b33a3ba0215d54e2d77dab103be3bcf`  
		Last Modified: Tue, 16 Jun 2026 00:11:06 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20260608-alpine3.24` - unknown; unknown

```console
$ docker pull bash@sha256:10b7302359643ce6ff4d6653f829b1a9ac22145d6be66387825ba875a1a60e40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.2 KB (135211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec98b81ea3f5d31febeb18ed5f6b85b42f797d5e7917382454965ad79996dbb3`

```dockerfile
```

-	Layers:
	-	`sha256:03e1a56a5a1085ec329a6e90a00e7910dcf76fedd2c52a70eaa3a16f4476fa68`  
		Last Modified: Tue, 16 Jun 2026 00:11:06 GMT  
		Size: 117.1 KB (117128 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:956e135d3357ece52fba54eeb7734dfa76daccf672efc34a380ee5038a17990a`  
		Last Modified: Tue, 16 Jun 2026 00:11:06 GMT  
		Size: 18.1 KB (18083 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20260608-alpine3.24` - linux; arm variant v6

```console
$ docker pull bash@sha256:8971e877268db1859e3bffa04e1187baf2343aca4d291799cedcfe328678e34a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6555234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:659a4c46128f2b5edfbfeaad79f04ebaf30d390c958a5c16f155d85d2e32c604`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:25 GMT
ADD alpine-minirootfs-3.24.1-armhf.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:25 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:09:03 GMT
ENV _BASH_COMMIT=8085ee139645391bb392cc06dd25717238b65455
# Tue, 16 Jun 2026 00:09:03 GMT
ENV _BASH_VERSION=devel-20260608
# Tue, 16 Jun 2026 00:09:03 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 16 Jun 2026 00:09:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 16 Jun 2026 00:09:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:09:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 00:09:47 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:3c4836a46d600cfe9a422adf7a80205cb534097e6213325e0176c51f6e5cc02e`  
		Last Modified: Sun, 14 Jun 2026 06:44:57 GMT  
		Size: 3.6 MB (3553450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2099bf333805b304f2f7a8ebaed683a5344b1056651f19c98faa2d1e36e2daec`  
		Last Modified: Tue, 16 Jun 2026 00:09:51 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aa1182dbcbadb2b51d181947144a8433bfdbe22ad1717833b3b0348e055d56a`  
		Last Modified: Tue, 16 Jun 2026 00:09:51 GMT  
		Size: 3.0 MB (3000996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea6913da964a2b833a3d35f959efb3e0319f05aa566c0390f98a405b62c92237`  
		Last Modified: Tue, 16 Jun 2026 00:09:51 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20260608-alpine3.24` - unknown; unknown

```console
$ docker pull bash@sha256:a06840a34e629a26df4d3545b5ffe2de9f43297d9118940ab022c088f8fd4058
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 KB (17948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02f763e34151c9b7fe5530d208660a3ffde590043542ea5d2bc767b0dabc5694`

```dockerfile
```

-	Layers:
	-	`sha256:eed290fccda07581bcaa36a67c022a0e95f5ab2b1990a60cb702926a2b16c51a`  
		Last Modified: Tue, 16 Jun 2026 00:09:51 GMT  
		Size: 17.9 KB (17948 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20260608-alpine3.24` - linux; arm variant v7

```console
$ docker pull bash@sha256:5f6c4af722cbf866ff410b74e90ae2c6135008307277bf5cdd63469fa79aa049
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6211039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dcd503c5cacd4adcc96d5e2b3768a0592d95d623eeedae3806e24862b278748`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:26 GMT
ADD alpine-minirootfs-3.24.1-armv7.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:26 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:10:28 GMT
ENV _BASH_COMMIT=8085ee139645391bb392cc06dd25717238b65455
# Tue, 16 Jun 2026 00:10:28 GMT
ENV _BASH_VERSION=devel-20260608
# Tue, 16 Jun 2026 00:10:28 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 16 Jun 2026 00:11:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 16 Jun 2026 00:11:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:11:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 00:11:11 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:bc03a9e5b4dd452551f246e199537fe7afc1765f53f510bc81d26df9845e4008`  
		Last Modified: Sun, 14 Jun 2026 06:45:22 GMT  
		Size: 3.3 MB (3260615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c19de53c18f1c1cd8bfe15d57026f1179eb740704a8a4fee59de9035ee50c7a`  
		Last Modified: Tue, 16 Jun 2026 00:11:16 GMT  
		Size: 458.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ad79e3f1bc8382968c8bd335003ada6c1ee4853119ebab97ab9706897ec2549`  
		Last Modified: Tue, 16 Jun 2026 00:11:16 GMT  
		Size: 2.9 MB (2949627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f059ebe590310e3017b1767e06b9c441d4ef243453273badab0d36d55ac224a`  
		Last Modified: Tue, 16 Jun 2026 00:11:16 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20260608-alpine3.24` - unknown; unknown

```console
$ docker pull bash@sha256:f63595b4a4f8e216d945fec9c35398f0c374044533a64ee8b9c18f5bbfc0a142
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 KB (134678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e5f14c8fb0aa64729001d95abc66bee579e8f1ccffec1cdfd99ee09849f3b22`

```dockerfile
```

-	Layers:
	-	`sha256:3844fa3f8bd3e5a696c429f50a08f5662496624607fc3dfc39d3d691147a8d34`  
		Last Modified: Tue, 16 Jun 2026 00:11:16 GMT  
		Size: 116.5 KB (116514 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eab5c3f151cb0177591559adbd7bc6279d342a70786541ecaa0181e28dd832b9`  
		Last Modified: Tue, 16 Jun 2026 00:11:16 GMT  
		Size: 18.2 KB (18164 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20260608-alpine3.24` - linux; arm64 variant v8

```console
$ docker pull bash@sha256:6ca2f1c4f824f280222653394d07c6d18a2e57c17566b34f92bb83f57f02511a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7296509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53fa639098d02ddda0b694ee35ea4201979376a49964bea64d38ded169373493`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:20 GMT
ADD alpine-minirootfs-3.24.1-aarch64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:20 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:11:13 GMT
ENV _BASH_COMMIT=8085ee139645391bb392cc06dd25717238b65455
# Tue, 16 Jun 2026 00:11:13 GMT
ENV _BASH_VERSION=devel-20260608
# Tue, 16 Jun 2026 00:11:13 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 16 Jun 2026 00:11:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 16 Jun 2026 00:11:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:11:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 00:11:55 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:5de55e5ef9c033997441461efe7ba23a986db059c0bb78b38f84ee0d72b99167`  
		Last Modified: Sun, 14 Jun 2026 06:44:31 GMT  
		Size: 4.2 MB (4183037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6b7db940d6cb72e476c8633e7a880b3924c3dc02986a083f8105c83dd0fda30`  
		Last Modified: Tue, 16 Jun 2026 00:12:00 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb0ec0e4bb548308206a22bd3f09d968da873e5e9f813d7cb796818b7838e25e`  
		Last Modified: Tue, 16 Jun 2026 00:12:01 GMT  
		Size: 3.1 MB (3112684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb2fa83475a8a6aec990c0d67da2f92ebe7a436e7578c98539c8222f4e984115`  
		Last Modified: Tue, 16 Jun 2026 00:12:00 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20260608-alpine3.24` - unknown; unknown

```console
$ docker pull bash@sha256:ee5de1b65407929609c85db981a0908a8bdacfd61f178737873d499f60bebe21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 KB (134722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24e3bd15b6530b2fdba04012355c7e6310c0f3e25ce780855c4c957179188297`

```dockerfile
```

-	Layers:
	-	`sha256:d4bc811d65f29fafd634656e369605785131bc1d5ce39f6958b045fa84ad5367`  
		Last Modified: Tue, 16 Jun 2026 00:12:00 GMT  
		Size: 116.5 KB (116534 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8172a0aebe134f1009d5c215ed06c2a7cc003a587f4e811083af5340c0bbd0aa`  
		Last Modified: Tue, 16 Jun 2026 00:12:00 GMT  
		Size: 18.2 KB (18188 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20260608-alpine3.24` - linux; 386

```console
$ docker pull bash@sha256:9372b71bb1a589e82017a61e6fe33cbc83b82eab89d86b4139be00eda0e7cd6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6639079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e77bdbbb55542ede615870f54b760c80ee7fa9f30ac7d9509361f436596aef1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:19 GMT
ADD alpine-minirootfs-3.24.1-x86.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:19 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:10:39 GMT
ENV _BASH_COMMIT=8085ee139645391bb392cc06dd25717238b65455
# Tue, 16 Jun 2026 00:10:39 GMT
ENV _BASH_VERSION=devel-20260608
# Tue, 16 Jun 2026 00:10:39 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 16 Jun 2026 00:11:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 16 Jun 2026 00:11:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:11:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 00:11:16 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:f86df9d778509895efbf9363d8fcb0cbe0b772de536c7218e4c4c947f0be879f`  
		Last Modified: Sun, 14 Jun 2026 06:45:46 GMT  
		Size: 3.7 MB (3670141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b8130322bd9c1fca88be110d797ad4263dca25c73529c98988999bc402e4554`  
		Last Modified: Tue, 16 Jun 2026 00:11:21 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0edc03f952b3e06c691cb08c7eb22529905d295e0a9cfe7db6a922f7ce77a763`  
		Last Modified: Tue, 16 Jun 2026 00:11:21 GMT  
		Size: 3.0 MB (2968149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1ee64ca2a0caa69210a9d5286fc3de5cbf81b8350418eca9f0f3e8db8f06d75`  
		Last Modified: Tue, 16 Jun 2026 00:11:21 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20260608-alpine3.24` - unknown; unknown

```console
$ docker pull bash@sha256:4dab827d53ddc6f987c47f64dfa138c0e8deb52eacd63a419a19c35c6bd43087
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.2 KB (135155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69a97ce2ad116ac3dbb056420d1e291e0b6837f1dc1675dc1030d70465e23115`

```dockerfile
```

-	Layers:
	-	`sha256:bca404d9ca2aa667127815b20cd2ad51f87320043855345ccaaac7dd6a318cfd`  
		Last Modified: Tue, 16 Jun 2026 00:11:21 GMT  
		Size: 117.1 KB (117103 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e3b34059536766582da969dee28e72e9279899838f250e1d15727c44bc2b543`  
		Last Modified: Tue, 16 Jun 2026 00:11:21 GMT  
		Size: 18.1 KB (18052 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20260608-alpine3.24` - linux; ppc64le

```console
$ docker pull bash@sha256:9ce919700ce34b87f3ab6f995a86bd5ecb54a844de6fc60459c6809ac996820d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7168395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e95dc2de5fa2f360e900e83d14b0b3c57c956479abdeeb63076f84fa1613d82`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:15 GMT
ADD alpine-minirootfs-3.24.1-ppc64le.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:15 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:09:37 GMT
ENV _BASH_COMMIT=8085ee139645391bb392cc06dd25717238b65455
# Tue, 16 Jun 2026 00:09:37 GMT
ENV _BASH_VERSION=devel-20260608
# Tue, 16 Jun 2026 00:09:37 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 16 Jun 2026 00:10:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 16 Jun 2026 00:10:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:10:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 00:10:38 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:3ebcdcd395ccee658b9200e4b27d7699e5d6ed9f6c1858dea12781aac519ff59`  
		Last Modified: Sun, 14 Jun 2026 06:46:36 GMT  
		Size: 3.8 MB (3813400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed2fadd4931055b5513649f4ec9a01ac48759a51f5231a582bec3ee960304d32`  
		Last Modified: Tue, 16 Jun 2026 00:10:46 GMT  
		Size: 458.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a24b49de8574599acabd91c11147b8a1725bf52ef0db1d891c59971e1bc6232`  
		Last Modified: Tue, 16 Jun 2026 00:10:47 GMT  
		Size: 3.4 MB (3354200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b23b30c2bf5ff02f6dcf2caf8895e4c9d25893740ba95fde819e32069cd440d`  
		Last Modified: Tue, 16 Jun 2026 00:10:47 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20260608-alpine3.24` - unknown; unknown

```console
$ docker pull bash@sha256:9f4fc94443d53188947852e79e79a0871e62010235d9de244e3675562631df5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.6 KB (134639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a07fb30ac5cee65826b3ecc0cb7c135144031d9b5b2c54ea214c6b80b9c7ede1`

```dockerfile
```

-	Layers:
	-	`sha256:e25aded86fd9ad1a7938258826c1401c74e6c575a2c544be19375b1426f6d21a`  
		Last Modified: Tue, 16 Jun 2026 00:10:46 GMT  
		Size: 116.5 KB (116511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25b415aed20a2f4115a409d98d86f40f8de9461349ad2ef7b876bf951bbfbc05`  
		Last Modified: Tue, 16 Jun 2026 00:10:46 GMT  
		Size: 18.1 KB (18128 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20260608-alpine3.24` - linux; riscv64

```console
$ docker pull bash@sha256:1a7965b5d64f0a9adf0405ddff1a89e5f470947f79d5a13948f30d4b112932a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6808041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47eedcda809c243b9f4f1742ea7e8b437be4a179a9681c5070067ce100ce4737`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 16 Jun 2026 05:59:15 GMT
ADD alpine-minirootfs-3.24.1-riscv64.tar.gz / # buildkit
# Tue, 16 Jun 2026 05:59:15 GMT
CMD ["/bin/sh"]
# Wed, 17 Jun 2026 08:52:36 GMT
ENV _BASH_COMMIT=8085ee139645391bb392cc06dd25717238b65455
# Wed, 17 Jun 2026 08:52:36 GMT
ENV _BASH_VERSION=devel-20260608
# Wed, 17 Jun 2026 08:52:36 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Wed, 17 Jun 2026 09:03:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Wed, 17 Jun 2026 09:03:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Jun 2026 09:03:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jun 2026 09:03:10 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:c34e5222b29b86391cdae95b0473ef789493ff1a0068a3a30b5d66f544bd7cf6`  
		Last Modified: Sun, 14 Jun 2026 06:47:00 GMT  
		Size: 3.6 MB (3574358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:827a35dcfb8db2611034951f6d39e1b26cb62ad8ace0e5a8ca06a90d5908efde`  
		Last Modified: Wed, 17 Jun 2026 09:03:36 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a395e08b933bb3dffd6b2283e851359f0f7ecfb77a1041f7146e4728a3dccd3`  
		Last Modified: Wed, 17 Jun 2026 09:03:37 GMT  
		Size: 3.2 MB (3232887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79c0a73b769800704bb5ec994915d1376cde0dfd7616ae9801e0ecd950836a27`  
		Last Modified: Wed, 17 Jun 2026 09:03:36 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20260608-alpine3.24` - unknown; unknown

```console
$ docker pull bash@sha256:dd66752970009276be46a64c1f6ff8a6e5eef38514297836bc6e34dd641b3c3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.6 KB (134634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ebd4131387f08c0fa774e218a7107ce1f1f39f3d988df569f36bc9754d9cce3`

```dockerfile
```

-	Layers:
	-	`sha256:418c178e9b0ddb95aa5a346c8b9b08464873f3d214d7176a28f7bf8616194cbf`  
		Last Modified: Wed, 17 Jun 2026 09:03:36 GMT  
		Size: 116.5 KB (116507 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a7b9139a4008f07baecf24096c8f5a3d6ffdf5afd8acbb7796218d251a93e10`  
		Last Modified: Wed, 17 Jun 2026 09:03:36 GMT  
		Size: 18.1 KB (18127 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20260608-alpine3.24` - linux; s390x

```console
$ docker pull bash@sha256:1bd99066f49b6772684e20ec038e8f1492620d8067c732a79eafddd9d2593a61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6842774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c1c162835379f325f1f0254a7230a891d44c70b65acbfe391942db0493144b9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:21 GMT
ADD alpine-minirootfs-3.24.1-s390x.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:21 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:10:20 GMT
ENV _BASH_COMMIT=8085ee139645391bb392cc06dd25717238b65455
# Tue, 16 Jun 2026 00:10:20 GMT
ENV _BASH_VERSION=devel-20260608
# Tue, 16 Jun 2026 00:10:20 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 16 Jun 2026 00:11:26 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 16 Jun 2026 00:11:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:11:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 00:11:26 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:da43be6afaaa3ec1b607461ce64380942a6d76c3d52cda4337b0770d9a96fa89`  
		Last Modified: Sun, 14 Jun 2026 06:47:25 GMT  
		Size: 3.7 MB (3709320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b75b9e7625d31f5c6d981003c05141b8f2be60de2afb5f9fe84b32296009b61`  
		Last Modified: Tue, 16 Jun 2026 00:11:39 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7f43b1ce1e68e6147623514051024e7a9b89cb41f8b351f1ae58dee94c668ac`  
		Last Modified: Tue, 16 Jun 2026 00:11:39 GMT  
		Size: 3.1 MB (3132661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44fc5a6908da285f7f727045d3a0cd881c1b672ca6ce4f18962bef2bc9fb3e10`  
		Last Modified: Tue, 16 Jun 2026 00:11:39 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20260608-alpine3.24` - unknown; unknown

```console
$ docker pull bash@sha256:ede980d6a8a34da0786b54d829feb73d6b68e151f4a3da0c06ea15ff966ed6b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.6 KB (134561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:196e7455b311e5d8e843d64925bf75156b17cf42e8ae09ca525005fde4bbe9c1`

```dockerfile
```

-	Layers:
	-	`sha256:0e654fb8a4d558de7e5021a550447eba4cdc19d8b5a132f32cfdeee0707aef3e`  
		Last Modified: Tue, 16 Jun 2026 00:11:39 GMT  
		Size: 116.5 KB (116477 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73aacef40fde8a3124d9dc756ba6f652fe3b5f604477d5e7d6f31292f19f7511`  
		Last Modified: Tue, 16 Jun 2026 00:11:39 GMT  
		Size: 18.1 KB (18084 bytes)  
		MIME: application/vnd.in-toto+json
