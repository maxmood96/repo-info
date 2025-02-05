## `bash:devel`

```console
$ docker pull bash@sha256:cd86eab21f24faf47565cc336b915122f35ebd1d650389717657df87d4fab5c0
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
$ docker pull bash@sha256:d825de4e7c45951aad0976e90dc2407954b9b39e13de130111ebde2a7d539eb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6593084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c4139bad1bd3c935b28b0e655c2c723f96f5364b9fa6bd212d43b839fa038cf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
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
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:252b0dc1743bddd0a6608c1882e7d57a244cb5be9b11b74cd3435e6dd98690b2`  
		Last Modified: Tue, 04 Feb 2025 20:31:41 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:482fa2c63cef8ebe0ea80251b7af5f525bf433d958b81b88325cccbc3ad0c38b`  
		Last Modified: Tue, 04 Feb 2025 20:31:42 GMT  
		Size: 3.0 MB (2950574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0d8610825eb5583f8ed61f9170ce440d64e8e51653ac87ab9cfd56211863d87`  
		Last Modified: Tue, 04 Feb 2025 20:31:41 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:ae42a771dcaa3eba902c4ac3da57ae472711a9fcdd5ed16dc032b7893f9fda9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.6 KB (132573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:907a0356bd9842be125f2184caf96cb2e0f341fba35037c053875428ca2842dc`

```dockerfile
```

-	Layers:
	-	`sha256:1a68422755ebac206656c6300afddbd0303aacbb0b7c4e5532b6f4d2523d1173`  
		Last Modified: Tue, 04 Feb 2025 20:31:41 GMT  
		Size: 114.9 KB (114922 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07047bb8388084675398e78e10f19405e22343e047c0a96d34c15ab8248926ba`  
		Last Modified: Tue, 04 Feb 2025 20:31:41 GMT  
		Size: 17.7 KB (17651 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; arm variant v6

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

### `bash:devel` - unknown; unknown

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

### `bash:devel` - linux; arm variant v7

```console
$ docker pull bash@sha256:3d2cc66b9ed75107c23a1e6649a1b0cb05737161eba9a404b5641aa3e86f61eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5937474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97999c503665345f5d902a61c648f600d73ac9c693d14007c717c16ee6dc4d1b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armv7.tar.gz / # buildkit
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
	-	`sha256:824bc99f06f2c6bebc1172ff7e39d7a1cdbd077ec44632079a629f69e9db7abf`  
		Last Modified: Wed, 08 Jan 2025 17:34:01 GMT  
		Size: 3.1 MB (3097112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d3d2fdc30c5f6606f38c2be797bae397d151f4f1ee7e78e1ab4868fb463f4a0`  
		Last Modified: Wed, 08 Jan 2025 18:23:46 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:130e32b784fa835cb56b02cbc83af4a9f778d535ae49160fd88c1f4dfe0838b3`  
		Last Modified: Tue, 04 Feb 2025 22:51:48 GMT  
		Size: 2.8 MB (2839574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23bbc5cf603dfb45f9fe0d781cf1dfe82c9afb4f67c4947c1d0ec9ca49ccaf99`  
		Last Modified: Tue, 04 Feb 2025 22:51:48 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:aa08fba93b5a7668ca73d8d3f7fa8474503c0f5002d367a2a9ccbb088322ef83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.7 KB (132687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c09e89f4fc9344974e5cf67dd7707ba07ff493599e8acfe0e7cec2ae36d08238`

```dockerfile
```

-	Layers:
	-	`sha256:a33e15910c67e8c0c2cfdea5f9c4bda340cac4c1f92be22d872fa2a2cc20c264`  
		Last Modified: Tue, 04 Feb 2025 22:51:48 GMT  
		Size: 115.0 KB (114958 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:767b284e6cb2a95647eba6156d8738a2406356b9bd68c8b9f9e906b118d48305`  
		Last Modified: Tue, 04 Feb 2025 22:51:48 GMT  
		Size: 17.7 KB (17729 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; arm64 variant v8

```console
$ docker pull bash@sha256:f2fe6e6da581509fa9fa12d397afd50a9e83a70897486f21e8328501edbf0bb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7028589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d572d596be6793cd040ce1b82be692480ebd337fc1ae238b437cdf99d28fbf1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Tue, 28 Jan 2025 07:24:49 GMT
ENV _BASH_COMMIT=25e213a551dc808c7f29360075bad4806fb9fec5
# Tue, 28 Jan 2025 07:24:49 GMT
ENV _BASH_VERSION=devel-20250124
# Tue, 28 Jan 2025 07:24:49 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 28 Jan 2025 07:24:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 28 Jan 2025 07:24:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 28 Jan 2025 07:24:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Jan 2025 07:24:49 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c609346feefd24f529f25fd37883c8f54483d60d36f9cf7bc7e058e6699b4437`  
		Last Modified: Wed, 15 Jan 2025 01:24:58 GMT  
		Size: 458.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2297d5c0364e1892d6627c2fa1a7854b174617e500849c17c84d655752fa2d42`  
		Last Modified: Tue, 28 Jan 2025 23:28:29 GMT  
		Size: 3.0 MB (3035437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22b4ff28e21cc1c930865f7063dfde9f3cd0958e5e0f8d8ec668b941bfa7251`  
		Last Modified: Tue, 28 Jan 2025 23:28:28 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:a24b66bfde21a8dbb1197bef2ccba024a4f5c68aa28c97fd1798730ce4721ed2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.9 KB (132923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1735acda04402ca14cafa9200ea61fa7f77dc5de41c1ba3d9fd7bf9f338c34af`

```dockerfile
```

-	Layers:
	-	`sha256:ddc4963a252ff36a320267ea8b258f095d8d7e8294cfceb714626ecf70bfaaa9`  
		Last Modified: Tue, 28 Jan 2025 23:28:28 GMT  
		Size: 115.0 KB (114978 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd4977c135cceb3275e3f1db5eab382868d5f85e38ceda8a71083120e2d5456e`  
		Last Modified: Tue, 28 Jan 2025 23:28:28 GMT  
		Size: 17.9 KB (17945 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; 386

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

### `bash:devel` - unknown; unknown

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

### `bash:devel` - linux; ppc64le

```console
$ docker pull bash@sha256:170bbb3dfe6245d8d18442dd560e14797d62004b65ffbc6d4bcddaf80cbeeacf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6795083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:665bc6d3b1c0b0596c1f7b6e7113f7a6963bb1fd902db85a3c728ff5453e607c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-ppc64le.tar.gz / # buildkit
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
	-	`sha256:244ac55e5ecd413dee99efe3ace7cb84420bfc9a727ec2327dae7805045d7470`  
		Last Modified: Wed, 08 Jan 2025 17:24:16 GMT  
		Size: 3.6 MB (3573601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba2864eb05966c89ecc2f693f15dd35b154f22759821c1d4a8757dec136d82aa`  
		Last Modified: Wed, 08 Jan 2025 17:58:42 GMT  
		Size: 458.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7515fe6c2b530880e8c3d3d85e2db6a3e3d091e1ad0e8d9e3f831df50959a440`  
		Last Modified: Tue, 04 Feb 2025 21:11:03 GMT  
		Size: 3.2 MB (3220688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1f32a639037f99e44480c4c365c6e75ecf4550abfe608738640005d0fe8f652`  
		Last Modified: Tue, 04 Feb 2025 21:11:02 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:a2197b74878c7d145d99716c901797df6c9b833621a7691489dee0f682b92078
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.7 KB (130702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03b1425e9b0cf7f24d7267a0fed864325730b39d8449ac66429f22d719d45b05`

```dockerfile
```

-	Layers:
	-	`sha256:079d9b0115d67b8c7ac6b8ce6a05b68701ec45988f8b12be08f21ea1c68fd022`  
		Last Modified: Tue, 04 Feb 2025 21:11:02 GMT  
		Size: 113.0 KB (113005 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7d90ff0d42634a1c0851c2554dd1c7bd1036a89323d20167973b253804fb239`  
		Last Modified: Tue, 04 Feb 2025 21:11:02 GMT  
		Size: 17.7 KB (17697 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; riscv64

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

### `bash:devel` - unknown; unknown

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

### `bash:devel` - linux; s390x

```console
$ docker pull bash@sha256:0e05a1f38d0748d4d3db4b3139e7ae4db6a73d0e5aaac36a0521cc6740115b31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6513979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:566394a373caec64ae805c877aacc1449be3b942571cc0dc5558f5892491dcf5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-s390x.tar.gz / # buildkit
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
	-	`sha256:b2af93686f9384c40cfe861d7173877bb2ee1675c3ee70181799693c34c8722f`  
		Last Modified: Wed, 08 Jan 2025 17:25:12 GMT  
		Size: 3.5 MB (3466867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:801d5c182a40dcba7a22ab88171e05f46debad239e6d3bf47d7bcb7112b2fd86`  
		Last Modified: Tue, 04 Feb 2025 21:35:30 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51ab37f3872fc3d26e7fd4c461c0a8add07d20658f508d73f7ce78b63d0b14f0`  
		Last Modified: Tue, 04 Feb 2025 21:35:30 GMT  
		Size: 3.0 MB (3046319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7114710733aa3d07d18c991007156130d5faa165ecbbdd8eb034dd70f6756e38`  
		Last Modified: Tue, 04 Feb 2025 21:35:30 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:23d668eb434ebf7743cd79bfd7fa922afaa595aeb9b193abd6619494556da7ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.6 KB (130624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a6c58f67898a52bfc3cd1cf8147ac5c408f62e3f02d5e5490c351780ba2f9fb`

```dockerfile
```

-	Layers:
	-	`sha256:503efa9e1a1caabce398cfdfba8e44b9f2c9f7c62b76ba318c65f8217e479332`  
		Last Modified: Tue, 04 Feb 2025 21:35:30 GMT  
		Size: 113.0 KB (112971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e05796bef2389cceab2df7d130ee65b55844b10791e3cf5747932add684e07f`  
		Last Modified: Tue, 04 Feb 2025 21:35:30 GMT  
		Size: 17.7 KB (17653 bytes)  
		MIME: application/vnd.in-toto+json
