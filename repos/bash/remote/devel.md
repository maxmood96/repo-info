## `bash:devel`

```console
$ docker pull bash@sha256:ddec9560dd1194974e89520cb98f0fde86f6c61154f38ff9679b2c6de14b5600
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
$ docker pull bash@sha256:124e25b8719e7ccb1461ecde60779040f383e6c69b23082e093ee210d43d4616
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6591059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c17e978854d0788a945f18e7cacf18f871851fe255c30609247596c96e0719a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Dec 2024 11:18:05 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Tue, 31 Dec 2024 11:18:05 GMT
CMD ["/bin/sh"]
# Tue, 31 Dec 2024 11:18:05 GMT
ENV _BASH_COMMIT=5114e17172276cf5a2f889f8037ae58c4cb05bb9
# Tue, 31 Dec 2024 11:18:05 GMT
ENV _BASH_VERSION=devel-20241230
# Tue, 31 Dec 2024 11:18:05 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 31 Dec 2024 11:18:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 31 Dec 2024 11:18:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 31 Dec 2024 11:18:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 31 Dec 2024 11:18:05 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Tue, 14 Jan 2025 20:33:02 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e139bf3a700d553d463888882c9c3375bd8bfd0026d3a329942c6d740a8be19`  
		Last Modified: Wed, 08 Jan 2025 17:58:44 GMT  
		Size: 458.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:687cffc9f09e5a3c819e61bf0e0b207d9b35d38bbaf3985e59966c86c32b8749`  
		Last Modified: Wed, 08 Jan 2025 17:58:44 GMT  
		Size: 2.9 MB (2948553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92ee62927bf2236c246ddffafc42e7ca7060031ca606b2a9b0386f1120d81a5b`  
		Last Modified: Wed, 08 Jan 2025 17:58:44 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:0efb292f70be7b5621740ef004c0d2ef3051869a42ada71095d683d9e3a7c699
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.7 KB (132727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fc7eaa69205e80304fafab73d047444e0c009f04127ba6a7f895365fd0b4637`

```dockerfile
```

-	Layers:
	-	`sha256:306942103cbdc82a0a2dda17f65de6e53a509d98bb2f0c66b253bfa54c86c7ce`  
		Last Modified: Wed, 08 Jan 2025 17:58:44 GMT  
		Size: 114.9 KB (114922 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7aa0303ae70d6d92c81ba6a69898df9898570ce8f5f632363e3b5f1b25c94b58`  
		Last Modified: Wed, 08 Jan 2025 17:58:44 GMT  
		Size: 17.8 KB (17805 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; arm variant v6

```console
$ docker pull bash@sha256:687544cdbd90833d89ffaaf09768b886634cc5c94407f8add1b95edfc49a7197
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6250549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e70dff1017fd032592d6293c1e8b555bbac7dd54329ac51302a9311b9b8313f1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Dec 2024 11:18:05 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
# Tue, 31 Dec 2024 11:18:05 GMT
CMD ["/bin/sh"]
# Tue, 31 Dec 2024 11:18:05 GMT
ENV _BASH_COMMIT=5114e17172276cf5a2f889f8037ae58c4cb05bb9
# Tue, 31 Dec 2024 11:18:05 GMT
ENV _BASH_VERSION=devel-20241230
# Tue, 31 Dec 2024 11:18:05 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 31 Dec 2024 11:18:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 31 Dec 2024 11:18:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 31 Dec 2024 11:18:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 31 Dec 2024 11:18:05 GMT
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
	-	`sha256:00261d6647148499d3c916712616c5b6b95c43b32d442c487c0e9b6927ebc76b`  
		Last Modified: Wed, 08 Jan 2025 18:07:27 GMT  
		Size: 2.9 MB (2885873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:451243c8b1908f6ef1a287fcb9e07dfe46e7edd2ac0e294df85872c0fded31ba`  
		Last Modified: Wed, 08 Jan 2025 18:07:26 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:016acdab11d6586e0b48f9f17ccd2978b717e88ff20c5a0f87f9a4b899cc55cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 KB (17666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c7da49944cdf767e6c69a2bee72f5f6056d5bdeb2914bad3f28eadc9cfd1425`

```dockerfile
```

-	Layers:
	-	`sha256:f522430e2e943e23c332b4838c2b3808a6d2ebd2b9457c02ae773ae770ebc7c5`  
		Last Modified: Wed, 08 Jan 2025 18:07:26 GMT  
		Size: 17.7 KB (17666 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; arm variant v7

```console
$ docker pull bash@sha256:fc4e41df52470de21c3164a76c683c853a88fca777edf910572a6b0234625709
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5935168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d896b1181580364e9758fe69ae7ecda4af1066de3bae224083b48603f0a3df06`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Dec 2024 11:18:05 GMT
ADD alpine-minirootfs-3.21.2-armv7.tar.gz / # buildkit
# Tue, 31 Dec 2024 11:18:05 GMT
CMD ["/bin/sh"]
# Tue, 31 Dec 2024 11:18:05 GMT
ENV _BASH_COMMIT=5114e17172276cf5a2f889f8037ae58c4cb05bb9
# Tue, 31 Dec 2024 11:18:05 GMT
ENV _BASH_VERSION=devel-20241230
# Tue, 31 Dec 2024 11:18:05 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 31 Dec 2024 11:18:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 31 Dec 2024 11:18:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 31 Dec 2024 11:18:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 31 Dec 2024 11:18:05 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:824bc99f06f2c6bebc1172ff7e39d7a1cdbd077ec44632079a629f69e9db7abf`  
		Last Modified: Tue, 14 Jan 2025 20:33:57 GMT  
		Size: 3.1 MB (3097112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d3d2fdc30c5f6606f38c2be797bae397d151f4f1ee7e78e1ab4868fb463f4a0`  
		Last Modified: Wed, 08 Jan 2025 18:23:46 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c2d8c5249d1c8abf6e3c8a2a802acd768f1c8343545356725b8be2af14b0096`  
		Last Modified: Wed, 08 Jan 2025 18:23:46 GMT  
		Size: 2.8 MB (2837267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1edec46b51c0a4a5bccc26323dd64a0976beedcd047b2a4b141270dd4825ce5c`  
		Last Modified: Wed, 08 Jan 2025 18:23:46 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:a89df3c12a9db5ba7909c490eef2f227c232144c6a069557477b74bbea5ff0ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.8 KB (132838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d6149c943a71fd6c478d1a33d03935b955471ab52fbb23733a74f4b37735bef`

```dockerfile
```

-	Layers:
	-	`sha256:c76635a82b57e336dfeab4f52b18ced7c73f79e3344250dda676216826f74086`  
		Last Modified: Wed, 08 Jan 2025 18:23:46 GMT  
		Size: 115.0 KB (114958 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1372ca4b3b95d4b988bfc31ffc665fe38ac6faf32937c10ebb18f50626e15be8`  
		Last Modified: Wed, 08 Jan 2025 18:23:46 GMT  
		Size: 17.9 KB (17880 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; arm64 variant v8

```console
$ docker pull bash@sha256:3ccad7fbfc7a5219b66417de55c3be943965f2cec856ca03ba0a7a5781aeac7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7026359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55efcf0c01b559eb10fba21d22e960fa7f41041d3a57b739e4b12c8276db1296`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Dec 2024 11:18:05 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Tue, 31 Dec 2024 11:18:05 GMT
CMD ["/bin/sh"]
# Tue, 31 Dec 2024 11:18:05 GMT
ENV _BASH_COMMIT=5114e17172276cf5a2f889f8037ae58c4cb05bb9
# Tue, 31 Dec 2024 11:18:05 GMT
ENV _BASH_VERSION=devel-20241230
# Tue, 31 Dec 2024 11:18:05 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 31 Dec 2024 11:18:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 31 Dec 2024 11:18:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 31 Dec 2024 11:18:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 31 Dec 2024 11:18:05 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02ff78a59743f9f3c485c3ada33acb63dfbed2038973937282a2b4570888dcca`  
		Last Modified: Wed, 08 Jan 2025 18:09:01 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdce7d25dcc6bcfcb6f9b6b9523ecf4b2248b4f39e83baee773d1056c502346e`  
		Last Modified: Wed, 08 Jan 2025 18:09:01 GMT  
		Size: 3.0 MB (3033213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca1f2801e2a98d15bec55f96dbfa0f70bab80be7adb87fbc078e5adab38590f7`  
		Last Modified: Wed, 08 Jan 2025 18:09:01 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:894c46599470374564358e640908ca3b192df97044de9cd368f88604360c76f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.9 KB (132887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d0bc0c38377a2406f5d96e46e63f55b1203f0e9f63aeda70d1d18f77fda7bc4`

```dockerfile
```

-	Layers:
	-	`sha256:c04a1f82fd52f2472129070167ddc30e49e4dc1ab4ce6b61c409717aa9789160`  
		Last Modified: Wed, 08 Jan 2025 18:09:01 GMT  
		Size: 115.0 KB (114978 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1300a90e66f2d174f53e346cd22ac45326fbd7c474e91f9d947d2ef8913a60db`  
		Last Modified: Wed, 08 Jan 2025 18:09:01 GMT  
		Size: 17.9 KB (17909 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; 386

```console
$ docker pull bash@sha256:a34059a32cb4e25d9308d8bb448849c21ea2efe163a84287ddb1604d84283387
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6338998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fab6e9b31e0aae87ca9c3d68e311adab7f0bf42afd9207cadaa8cab92cc2d48`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Dec 2024 11:18:05 GMT
ADD alpine-minirootfs-3.21.2-x86.tar.gz / # buildkit
# Tue, 31 Dec 2024 11:18:05 GMT
CMD ["/bin/sh"]
# Tue, 31 Dec 2024 11:18:05 GMT
ENV _BASH_COMMIT=5114e17172276cf5a2f889f8037ae58c4cb05bb9
# Tue, 31 Dec 2024 11:18:05 GMT
ENV _BASH_VERSION=devel-20241230
# Tue, 31 Dec 2024 11:18:05 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 31 Dec 2024 11:18:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 31 Dec 2024 11:18:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 31 Dec 2024 11:18:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 31 Dec 2024 11:18:05 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:dbaac2331104495e5df0818a1db05c402cfc13af140c75beccf51922d5f37ad5`  
		Last Modified: Tue, 14 Jan 2025 20:33:01 GMT  
		Size: 3.5 MB (3463126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf86af7b3d0812661287b0cf8e7bf4c5b76643a38b98865609b611bfd001a5b5`  
		Last Modified: Wed, 08 Jan 2025 17:58:30 GMT  
		Size: 459.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35b97b25a698a8f845080905a2d0de70e6355d840ad3087e32df4c38e824e8ee`  
		Last Modified: Wed, 08 Jan 2025 17:58:30 GMT  
		Size: 2.9 MB (2875076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:775807b0027857c5e55a1f31fb95f828fa0f75bd2999a2152a1f2c1146a5c1df`  
		Last Modified: Wed, 08 Jan 2025 17:58:30 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:0a821287dc22274e7b14ca605ca7396bb2e9a499a2b6c9a70c554b11f16dfa46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.7 KB (132669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a24c5d25863385306831aa8fe0625854997b6e8b4384a1f5698e8c0c02696bb7`

```dockerfile
```

-	Layers:
	-	`sha256:0892b9b63d6c7d0432a2da6b669b6ebea4c1e5536a924f8f028f2372ae1874e2`  
		Last Modified: Wed, 08 Jan 2025 17:58:30 GMT  
		Size: 114.9 KB (114897 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f78496cea62c7e22dc29e12065479636f39bde17436996bff883ae80221906a8`  
		Last Modified: Wed, 08 Jan 2025 17:58:30 GMT  
		Size: 17.8 KB (17772 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; ppc64le

```console
$ docker pull bash@sha256:64a9fc8af72cc5afb68c8b2413ad9195bf6a7d20e979c9d0cc0ac6e231bc0530
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6791595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a81b4c60a9a2ee0a1c5922c53bd20c1701092ae296aa21b4ae6c74797d28105`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Dec 2024 11:18:05 GMT
ADD alpine-minirootfs-3.21.2-ppc64le.tar.gz / # buildkit
# Tue, 31 Dec 2024 11:18:05 GMT
CMD ["/bin/sh"]
# Tue, 31 Dec 2024 11:18:05 GMT
ENV _BASH_COMMIT=5114e17172276cf5a2f889f8037ae58c4cb05bb9
# Tue, 31 Dec 2024 11:18:05 GMT
ENV _BASH_VERSION=devel-20241230
# Tue, 31 Dec 2024 11:18:05 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 31 Dec 2024 11:18:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 31 Dec 2024 11:18:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 31 Dec 2024 11:18:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 31 Dec 2024 11:18:05 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:244ac55e5ecd413dee99efe3ace7cb84420bfc9a727ec2327dae7805045d7470`  
		Last Modified: Tue, 14 Jan 2025 20:33:45 GMT  
		Size: 3.6 MB (3573601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba2864eb05966c89ecc2f693f15dd35b154f22759821c1d4a8757dec136d82aa`  
		Last Modified: Wed, 08 Jan 2025 17:58:42 GMT  
		Size: 458.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebed39b055bad9a632f56e254a7790d53c032ce9d65f77a175b09832e747ba0a`  
		Last Modified: Wed, 08 Jan 2025 17:58:43 GMT  
		Size: 3.2 MB (3217199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75ae5766834f5cba993fd4d7c1d37996723922281344f039f07a7ad4321ec325`  
		Last Modified: Wed, 08 Jan 2025 17:58:42 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:db5f96f1ebbe41d04a7b8eac5c18d191b6b65235201350247aab14057a01cb1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.9 KB (130853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d2b245b98664c238f98104bfde396438eae3113ef4f27812559b4a517ba19df`

```dockerfile
```

-	Layers:
	-	`sha256:d97cb82eb370e97b677934c89e7b59bb1154e709874cb874fae7ed0109918c5c`  
		Last Modified: Wed, 08 Jan 2025 17:58:42 GMT  
		Size: 113.0 KB (113005 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f2d2594d4ab4194e627676d91a6b61215046ef2c2de23d70756700674585823`  
		Last Modified: Wed, 08 Jan 2025 17:58:42 GMT  
		Size: 17.8 KB (17848 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; riscv64

```console
$ docker pull bash@sha256:85e252a6e6ed5dfbe731a280e2564445bbce0463d0f6977090b666d1ff2ed034
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6250609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e7b0247ec6253ac9b22bb1890cbe0823447f836852ed3e6aaa6182f3cc1a88b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Dec 2024 11:18:05 GMT
ADD alpine-minirootfs-3.21.2-riscv64.tar.gz / # buildkit
# Tue, 31 Dec 2024 11:18:05 GMT
CMD ["/bin/sh"]
# Tue, 31 Dec 2024 11:18:05 GMT
ENV _BASH_COMMIT=5114e17172276cf5a2f889f8037ae58c4cb05bb9
# Tue, 31 Dec 2024 11:18:05 GMT
ENV _BASH_VERSION=devel-20241230
# Tue, 31 Dec 2024 11:18:05 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 31 Dec 2024 11:18:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 31 Dec 2024 11:18:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 31 Dec 2024 11:18:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 31 Dec 2024 11:18:05 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:21a89fc8a7107842fa0935d999d700ca9a9df964110a7076d946b16f07a54de5`  
		Last Modified: Tue, 14 Jan 2025 20:35:37 GMT  
		Size: 3.4 MB (3350256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cee5ec45bdf477db840352ec8979a5377f81b57c5bd134c10ef0dd422448e2c3`  
		Last Modified: Wed, 08 Jan 2025 18:10:13 GMT  
		Size: 459.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d73b91f93bd04f16769f11c72266df411a4c9449e2955de6a4d8e5f02dc21b6`  
		Last Modified: Wed, 08 Jan 2025 18:10:14 GMT  
		Size: 2.9 MB (2899555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f58e0a73005d6ad18c6d29e4df622c1745ac0bc12bef4b39df729d6281ada4d2`  
		Last Modified: Wed, 08 Jan 2025 18:10:13 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:1b18fd28d96a4126b7dd55ff1c74f0208773bc26c2202bbb8e67ebebecf2697a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.8 KB (130850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f166602595751a6b8c57dc22c1b2333ecf14ce8b59be7aa33f94c3363c65a780`

```dockerfile
```

-	Layers:
	-	`sha256:9293ab04a7d461f3f864fae5f71df7265824641e9b9367225b5d3e965c68d706`  
		Last Modified: Wed, 08 Jan 2025 18:10:13 GMT  
		Size: 113.0 KB (113001 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9de573420e8c8f09ecacb6e49bdd5becd4d21de3e575c94572a7e0dd718d2b2c`  
		Last Modified: Wed, 08 Jan 2025 18:10:13 GMT  
		Size: 17.8 KB (17849 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; s390x

```console
$ docker pull bash@sha256:74aa25baa50d8f2b8434bdc166d014f5f77e39a5f404f9d4c42311d56a3ecf0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6511363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad77bb41dcd8005f382b7c52237be71996592a7d96ea1e20fbcdf0c85588c11b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Dec 2024 11:18:05 GMT
ADD alpine-minirootfs-3.21.2-s390x.tar.gz / # buildkit
# Tue, 31 Dec 2024 11:18:05 GMT
CMD ["/bin/sh"]
# Tue, 31 Dec 2024 11:18:05 GMT
ENV _BASH_COMMIT=5114e17172276cf5a2f889f8037ae58c4cb05bb9
# Tue, 31 Dec 2024 11:18:05 GMT
ENV _BASH_VERSION=devel-20241230
# Tue, 31 Dec 2024 11:18:05 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 31 Dec 2024 11:18:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 31 Dec 2024 11:18:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 31 Dec 2024 11:18:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 31 Dec 2024 11:18:05 GMT
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
	-	`sha256:123d9edc85f9023338d8600ffa4a9187c466fdff4eb1f937db0c812090d812da`  
		Last Modified: Wed, 08 Jan 2025 17:58:08 GMT  
		Size: 3.0 MB (3043708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04af29e424200e9bcfa0dc4bfdc6d98643e87a3418ce4cd4d0a0852d0df656e2`  
		Last Modified: Wed, 08 Jan 2025 17:58:08 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:946a35b63d6efc8529a156ca17d77ba2e5b0da85223ee06aad88a4dddb1f2b7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.8 KB (130776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8031aa7957abd0bb1af592449ea3ce39a28e3fc9a339ce73b5855e3bdec41e86`

```dockerfile
```

-	Layers:
	-	`sha256:bec851af77c2e6fa0d9e5bf65c8587de6ecb52984459ecdc43863318bfe2c3d4`  
		Last Modified: Wed, 08 Jan 2025 17:58:08 GMT  
		Size: 113.0 KB (112971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ebe7065b46a2a15da0dcbba8c56e158dff1e4e4b800cfdf1e8ef6d9774d33c5`  
		Last Modified: Wed, 08 Jan 2025 17:58:08 GMT  
		Size: 17.8 KB (17805 bytes)  
		MIME: application/vnd.in-toto+json
