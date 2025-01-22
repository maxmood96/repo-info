## `bash:devel-alpine3.21`

```console
$ docker pull bash@sha256:d8fb728f7355ffc9735ce7441665105c26f5d8cf0aef7cda9a303a77c8ba7377
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

### `bash:devel-alpine3.21` - linux; amd64

```console
$ docker pull bash@sha256:2cb572839b71c9344951fb26504fdd6f9fa2e1a850955b58c95f701f3495c14a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6592048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77f31c276c833e60727d9906204d1762643f2738e5e9551961f0a70d67090f1f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Tue, 21 Jan 2025 23:18:21 GMT
ENV _BASH_COMMIT=42c49d621d9341a530bca9422d7000087593e6bb
# Tue, 21 Jan 2025 23:18:21 GMT
ENV _BASH_VERSION=devel-20250117
# Tue, 21 Jan 2025 23:18:21 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 21 Jan 2025 23:18:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 21 Jan 2025 23:18:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 23:18:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 23:18:21 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9ba7163682f0d6cafa30443930f7cea5b2ef84d6a216ad8a8d8c767f60f7c16`  
		Last Modified: Wed, 22 Jan 2025 03:08:56 GMT  
		Size: 458.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:067a3e65ee519a05df5a3e763fbb9d020980e40eb5bdd8dca60477a0ef05b7ee`  
		Last Modified: Wed, 22 Jan 2025 03:08:56 GMT  
		Size: 2.9 MB (2949538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eeafe3d90545f6377abe09e414f04d2a087510e6a3f374f4ab4783a71056b64`  
		Last Modified: Wed, 22 Jan 2025 03:08:56 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.21` - unknown; unknown

```console
$ docker pull bash@sha256:01e602e0d47bd6b49fa010616df1ad79ee6b4051c0d3b138fd83afab5cbb3725
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.7 KB (132742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d120e85f2138d50843fa2d92dd467fad2e9841db22ba9f05b2926d20adbf861c`

```dockerfile
```

-	Layers:
	-	`sha256:e187b4f18bf0f6d1f94721fbcf31328680cb842c25c4eda824c9ffe8ac9a12b0`  
		Last Modified: Wed, 22 Jan 2025 03:08:56 GMT  
		Size: 114.9 KB (114922 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbc94e72c68b289d0986875473708c41d4be22d185dd2b46671b4d2243199f8f`  
		Last Modified: Wed, 22 Jan 2025 03:08:56 GMT  
		Size: 17.8 KB (17820 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.21` - linux; arm variant v6

```console
$ docker pull bash@sha256:e5fd0964af70b5b5d7f95b1b5bab6ea6e3a0261042052bfe07feee57b7b03f01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6250973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8360ed4b553c061fc2ba17361bce8703357307d9c0016a9b0361b211f31ba26a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Tue, 21 Jan 2025 23:18:21 GMT
ENV _BASH_COMMIT=42c49d621d9341a530bca9422d7000087593e6bb
# Tue, 21 Jan 2025 23:18:21 GMT
ENV _BASH_VERSION=devel-20250117
# Tue, 21 Jan 2025 23:18:21 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 21 Jan 2025 23:18:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 21 Jan 2025 23:18:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 23:18:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 23:18:21 GMT
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
	-	`sha256:53d2548d8d97dd9e466788bb3d694c97aba943a4ef8705b7e1f5623ee3bdf486`  
		Last Modified: Wed, 22 Jan 2025 03:08:30 GMT  
		Size: 2.9 MB (2886300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c34e09fccf5b6b5201fdf003c5e2cc7912b1bbf1c442a7b70003bf5afd153985`  
		Last Modified: Wed, 22 Jan 2025 03:08:29 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.21` - unknown; unknown

```console
$ docker pull bash@sha256:9622e0148e94cbdb7280233db38f2f11b518781dfcf7612569187a890782baf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 KB (17681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89221866cd22d58f73aa35952b25e0c85afaaa78dcfa28e2d75f4cb62087bc91`

```dockerfile
```

-	Layers:
	-	`sha256:a706738b9f90267fca76a6e413142bfc41c52f951d39f243856fd3ec05166263`  
		Last Modified: Wed, 22 Jan 2025 03:08:30 GMT  
		Size: 17.7 KB (17681 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.21` - linux; arm variant v7

```console
$ docker pull bash@sha256:80854da0e43857dfb07ad7704786eb0c543939dfca5daca4b62a74fff210380e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5936616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:493402ea0662639592a07f7ef3b397073dc0b7b9480cbaa8a166daf1ca33bcbb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armv7.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Tue, 21 Jan 2025 23:18:21 GMT
ENV _BASH_COMMIT=42c49d621d9341a530bca9422d7000087593e6bb
# Tue, 21 Jan 2025 23:18:21 GMT
ENV _BASH_VERSION=devel-20250117
# Tue, 21 Jan 2025 23:18:21 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 21 Jan 2025 23:18:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 21 Jan 2025 23:18:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 23:18:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 23:18:21 GMT
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
	-	`sha256:4b7509d56de2876f54547d2ae793437957c8a83718c23b9ac92a2fed1d1b4415`  
		Last Modified: Wed, 22 Jan 2025 03:08:49 GMT  
		Size: 2.8 MB (2838714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8a0686457a14391c022cf8a1d3ae19c419532e4afaa60bee00cb03f1a49162b`  
		Last Modified: Wed, 22 Jan 2025 03:08:49 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.21` - unknown; unknown

```console
$ docker pull bash@sha256:c7b975bd117815ee2b8b477ad993d3b5e527c22ded71102c193ab17c704ac587
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.9 KB (132855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c079d70e8e3ddc8f74607e1ecfa1877ad7cadbe13e735980dc0ab7b669911d7e`

```dockerfile
```

-	Layers:
	-	`sha256:586eee343584bef9f816589417deef3fcaff1e6ca8a091d4cbebf561ee604983`  
		Last Modified: Wed, 22 Jan 2025 03:08:49 GMT  
		Size: 115.0 KB (114958 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed702bfd158195941ad1577a4901dc87369728b6e7f28f189794754a3386679e`  
		Last Modified: Wed, 22 Jan 2025 03:08:49 GMT  
		Size: 17.9 KB (17897 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull bash@sha256:db03258d63c356f228aea1706e35c620ad4264f3dd1031c69db1f32bd6b2f32c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7028225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed902280af0c5935e577fbfb49627acf40cbc6b476ffdbf23d731414bb711bf8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Tue, 21 Jan 2025 23:18:21 GMT
ENV _BASH_COMMIT=42c49d621d9341a530bca9422d7000087593e6bb
# Tue, 21 Jan 2025 23:18:21 GMT
ENV _BASH_VERSION=devel-20250117
# Tue, 21 Jan 2025 23:18:21 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 21 Jan 2025 23:18:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 21 Jan 2025 23:18:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 23:18:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 23:18:21 GMT
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
	-	`sha256:7c7de47028dfa9b156b6aab983259bf3209cba2cff10f40526464236fd3109bf`  
		Last Modified: Wed, 22 Jan 2025 03:08:51 GMT  
		Size: 3.0 MB (3035074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe945c683e4f356fd9f230e939216183a1f736a53ff41233349666366235da7c`  
		Last Modified: Wed, 22 Jan 2025 03:08:50 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.21` - unknown; unknown

```console
$ docker pull bash@sha256:8d6393207f17580e98a104263ff8fe4806072eaf2256cfceb5e28e4bc9230721
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.9 KB (132902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:446813d6fa77d67012e58e1348c811b82f9248cad3109f41936822227e4f9389`

```dockerfile
```

-	Layers:
	-	`sha256:60f74138b700578baaab9bc324e4e1b428dd2c87550f61c4c009d53b752f0d8a`  
		Last Modified: Wed, 22 Jan 2025 03:08:51 GMT  
		Size: 115.0 KB (114978 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d094becab358c9c226c62f88f60de8ff1d26d2992f618dfce24e0adaf68c26d`  
		Last Modified: Wed, 22 Jan 2025 03:08:50 GMT  
		Size: 17.9 KB (17924 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.21` - linux; 386

```console
$ docker pull bash@sha256:1741cc3c285ab8dcdccc25fcf77503ef65043bd9a4dd75fc283c06e473f152c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6340928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52cdb7673dc84d2aa414c82dc0bbcf6f6a8da3fd976ff8d4058a27fb5b7b54f9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Tue, 21 Jan 2025 23:18:21 GMT
ENV _BASH_COMMIT=42c49d621d9341a530bca9422d7000087593e6bb
# Tue, 21 Jan 2025 23:18:21 GMT
ENV _BASH_VERSION=devel-20250117
# Tue, 21 Jan 2025 23:18:21 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 21 Jan 2025 23:18:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 21 Jan 2025 23:18:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 23:18:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 23:18:21 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:dbaac2331104495e5df0818a1db05c402cfc13af140c75beccf51922d5f37ad5`  
		Last Modified: Wed, 08 Jan 2025 17:23:36 GMT  
		Size: 3.5 MB (3463126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bf57fc3896c6b4267b89b4741263c013b6723ad914e040f5ba8b45992c02e4b`  
		Last Modified: Wed, 22 Jan 2025 03:09:14 GMT  
		Size: 458.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9df2f778a5efc9f71449ca6851eb6793cb62e27aab48a35cd9b2fe3c5bd412f`  
		Last Modified: Wed, 22 Jan 2025 03:09:14 GMT  
		Size: 2.9 MB (2877007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfbdf82f54a5a257068829b1a9a808f0661e1d66c9a613a80c1151cc2b5f47d1`  
		Last Modified: Wed, 22 Jan 2025 03:09:14 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.21` - unknown; unknown

```console
$ docker pull bash@sha256:b0dc09a26fd6a5f9c2fb4c1dc8ef80e76cb26ba6613fcabd4f20c0f11c0664b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.7 KB (132686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf7f9912bbfc89d547e702bece1fba6ca153fa3193cb04df4e9ca0971e4cccf0`

```dockerfile
```

-	Layers:
	-	`sha256:4f816fe7f52f7ce9fb2160d236b1fd4f99611477b3ef5a300a15699f12c7e7c5`  
		Last Modified: Wed, 22 Jan 2025 03:09:14 GMT  
		Size: 114.9 KB (114897 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6dc39d67c3f50bfa27c3bed5db4aeeb2c02309387cc0b3b7a18b5236e90dc97`  
		Last Modified: Wed, 22 Jan 2025 03:09:14 GMT  
		Size: 17.8 KB (17789 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.21` - linux; ppc64le

```console
$ docker pull bash@sha256:cc6937a1db684fdeac30e71e2815e42995e5b637464874cc8cc621f5d2d64e9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6793205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3efa42c66a73ea616e27fc81d08c7a287257be6b44e3ce992fe6f3beec846f64`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Tue, 21 Jan 2025 23:18:21 GMT
ENV _BASH_COMMIT=42c49d621d9341a530bca9422d7000087593e6bb
# Tue, 21 Jan 2025 23:18:21 GMT
ENV _BASH_VERSION=devel-20250117
# Tue, 21 Jan 2025 23:18:21 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 21 Jan 2025 23:18:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 21 Jan 2025 23:18:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 23:18:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 23:18:21 GMT
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
	-	`sha256:f9011025ba1c291dfcdca50359d35f53ec9c28235256e3362d026ea0bde3d872`  
		Last Modified: Wed, 22 Jan 2025 03:08:49 GMT  
		Size: 3.2 MB (3218807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e975d10408974806fab354e47451575b438b7bfa7fb987dae80c001c1ea0960`  
		Last Modified: Wed, 22 Jan 2025 03:08:49 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.21` - unknown; unknown

```console
$ docker pull bash@sha256:09d09640dfc0712ed3c8269230802eb452b18531732795d07673249c0612705e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.9 KB (130870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f5e495d0e94de40a35069faa58a40b7f9d33e1789b2a424f7ac661dda4fa77d`

```dockerfile
```

-	Layers:
	-	`sha256:c184ac50f630fe312f9c967aff554b5150b143995197a88b6b60c3097009a369`  
		Last Modified: Wed, 22 Jan 2025 03:08:49 GMT  
		Size: 113.0 KB (113005 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f1758b06bfbc770f925c9980e69245b84784b0f41a8ffa944b1f0374b9c0d1f`  
		Last Modified: Wed, 22 Jan 2025 03:08:49 GMT  
		Size: 17.9 KB (17865 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.21` - linux; riscv64

```console
$ docker pull bash@sha256:226debefcabbac424ca5129b862435ef222d585097402144068db25e8d449fba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6251713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04c1054fe4066e210882deeeebcf53f8c68e9d1b70166d8a64bc74cd37b9b284`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-riscv64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Tue, 21 Jan 2025 23:18:21 GMT
ENV _BASH_COMMIT=42c49d621d9341a530bca9422d7000087593e6bb
# Tue, 21 Jan 2025 23:18:21 GMT
ENV _BASH_VERSION=devel-20250117
# Tue, 21 Jan 2025 23:18:21 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 21 Jan 2025 23:18:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 21 Jan 2025 23:18:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 23:18:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 23:18:21 GMT
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
	-	`sha256:feadf652221b7f0713e2f25b447c9ce5711dbaa0e0f9571fe8727c2ceed40af1`  
		Last Modified: Wed, 22 Jan 2025 03:16:54 GMT  
		Size: 2.9 MB (2900658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2db15b404872424a742cda417a37adbb329dc24a8c9a3268f64b5431342dc5e`  
		Last Modified: Wed, 22 Jan 2025 03:16:53 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.21` - unknown; unknown

```console
$ docker pull bash@sha256:8ec3e2dbf6405b1b352b6e550ffb260f734e5778664fa31e041ba413552912c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.9 KB (130866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fe27a245044b3dba6378b6eb91348c66ca040c9e2d86ae4a8f8a7ddc9d5cc19`

```dockerfile
```

-	Layers:
	-	`sha256:78afa340755b743e7d78b77109fa85a9fe63365eff6596d8ea3c2077a5e6d3ec`  
		Last Modified: Wed, 22 Jan 2025 03:16:53 GMT  
		Size: 113.0 KB (113001 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:297fc362610c6b4fed80c614f5e6639025a5c76cd835e22f1adfb2182d863505`  
		Last Modified: Wed, 22 Jan 2025 03:16:53 GMT  
		Size: 17.9 KB (17865 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.21` - linux; s390x

```console
$ docker pull bash@sha256:f1f794cbd0e34708b3eaf0d1e6633c690e0579a2739d05ed6c21acebaf73d4a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6512608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:924d714024974e4d9182b6f82f9908b0d79763da577fce6d94d7cdc2f620d58c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-s390x.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Tue, 21 Jan 2025 23:18:21 GMT
ENV _BASH_COMMIT=42c49d621d9341a530bca9422d7000087593e6bb
# Tue, 21 Jan 2025 23:18:21 GMT
ENV _BASH_VERSION=devel-20250117
# Tue, 21 Jan 2025 23:18:21 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 21 Jan 2025 23:18:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 21 Jan 2025 23:18:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 23:18:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 23:18:21 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:b2af93686f9384c40cfe861d7173877bb2ee1675c3ee70181799693c34c8722f`  
		Last Modified: Wed, 08 Jan 2025 17:25:12 GMT  
		Size: 3.5 MB (3466867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5a540196e840d845bf43b1d53eef177cb5b4cb8a0d8c3c3d0ed9a38955a9f84`  
		Last Modified: Wed, 08 Jan 2025 17:58:08 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00033bc02e16fbfd728db726b4a823f655a0e9a1fa0e7a4cead588e6bf9e8c68`  
		Last Modified: Wed, 22 Jan 2025 03:08:26 GMT  
		Size: 3.0 MB (3044951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:515fbf174f5e984fd71c2d93c485b6559d004999030ab334c2b573875c8c2505`  
		Last Modified: Wed, 22 Jan 2025 03:08:25 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.21` - unknown; unknown

```console
$ docker pull bash@sha256:d7c0c0a132afd4d84ffc884b74c464068b43c21d260282049026f140627d7512
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.8 KB (130792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a86ca1dc273934aa225e543d22194a1d2cd2d5e9127fbbb3ebc17786b1e52e5d`

```dockerfile
```

-	Layers:
	-	`sha256:912ecbd9f03f71ded7d2775716c3cc7eb5a5dca088717184182582231ce01af8`  
		Last Modified: Wed, 22 Jan 2025 03:08:25 GMT  
		Size: 113.0 KB (112971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ecf582500194d728c1b193564fa6fa02744e49ca1edba4822a8c9cd6bf7cd36`  
		Last Modified: Wed, 22 Jan 2025 03:08:25 GMT  
		Size: 17.8 KB (17821 bytes)  
		MIME: application/vnd.in-toto+json
